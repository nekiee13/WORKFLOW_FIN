# 93 — CLAUDE SETUP (Documentation)

**Scope:** how Claude Code is configured on this machine for the WORKFLOW_FIN project —
global instructions, project-level configuration, the MCP tool suite ("skills"), and
the prompt techniques developed inside this project.
**Snapshot date:** 2026-07-04.

---

## 1. Global CLAUDE.md (`~/.claude/CLAUDE.md`)

Private global instructions applied to **all** projects. ~5 KB, four policy sections,
all governing the j\*munch MCP suite:

| Policy | What it mandates |
|---|---|
| **Structured Retrieval Policy** | Route by content type: `jcodemunch` for source-code questions, `jdocmunch` for documentation, `jdatamunch` for tabular data. Never load raw source/Markdown/CSV/Excel/JSONL/Parquet into the conversation when a structured query can answer — search sections / outlines / filtered rows / aggregations first, retrieve only the needed slice. |
| **Code Exploration Policy** | Code navigation goes through jCodemunch tools (symbol search, outlines, references, blast radius, dead code, class hierarchy) — never raw `Read`/`Grep`/`Glob`/`Bash` for exploration. Exception: `Read` is allowed immediately before an `Edit`/`Write` (the harness requires it). Sessions open with `resolve_repo`, unfamiliar repos with `suggest_queries`. |
| **Session-Aware Routing** | Every task opens with `plan_turn(repo, query, model)`; the returned confidence gates exploration depth (high → ≤2 supplementary reads; medium → ≤5; low → report the gap, do NOT keep searching). `negative_evidence` verdicts are respected as "feature does not exist". After edits, `register_edit` keeps the index fresh; `budget_warning` in `_meta` stops further exploration. |
| **Model-Driven Tool Tiering** | `plan_turn` carries a `model=` parameter so the MCP server narrows the exposed tool list to the active model's tier at zero extra requests; `announce_model` is the fallback for non-code tasks. |

A backup of a previous version exists at `~/.claude/CLAUDE.md.bak`.

---

## 2. Global settings (`~/.claude/settings.json`)

| Setting | Value |
|---|---|
| Model | `claude-fable-5[1m]` (Fable 5, 1M context) |
| Effort level | `xhigh` |
| Theme | dark |

**Hooks** — all seven lifecycle hooks call the `jcodemunch-mcp` binary, keeping its
index and session telemetry synchronized with what Claude actually does:

| Hook | Matcher | Purpose |
|---|---|---|
| `PreToolUse` | `Read` | Intercepts raw reads (nudges structured retrieval / records access) |
| `PostToolUse` | `Edit\|Write` | Auto-reindexes edited files (no manual `register_edit` needed in Claude Code) |
| `PreCompact` | — | Emits a session snapshot before context compaction |
| `TaskCompleted` | — | Task-completion telemetry |
| `SubagentStart` | — | Propagates index context to subagents |
| `WorktreeCreate` / `WorktreeRemove` | — | Index lifecycle for isolated worktrees |

---

## 3. MCP servers — the tool suite (`~/.claude.json` → `mcpServers`)

Three structured-retrieval servers (the "skills" of this setup in the tooling sense),
all launched via `uvx` (stdio transport), all with `*_SHARE_SAVINGS=0`:

| Server | Version / source | Role in this project |
|---|---|---|
| **jdocmunch** | `jdocmunch-mcp==0.1.1` (PyPI) | Primary tool for WORKFLOW_FIN: indexed the whole doc corpus as repo `local/WORKFLOW_FIN` (45 files, ~1,350 sections). All workflow analysis ran through `get_document_outline` / `get_section(s)` / `search_sections` instead of raw file loads. |
| **jdatamunch** | `jdatamunch-mcp==0.1.1` (PyPI) | Tabular-data questions (describe → filtered rows → aggregation). Not needed heavily here — the workflow's tables are small and embedded in Markdown. |
| **jcodemunch** | `jcodemunch-mcp==1.108.27` (wheel from github.com/jgravelle/jcodemunch-mcp releases) | Code navigation + the hook suite above. WORKFLOW_FIN is a docs-only repo, so its main contribution here is the hooks (auto-reindex, compaction snapshots). |

**Project permission allow-list** (`WORKFLOW_FIN/.claude/settings.local.json`) pre-approves
the three jdocmunch calls used constantly in this project:
`get_document_outline`, `get_sections`, `search_sections`.

---

## 4. Project-level configuration (`WORKFLOW_FIN/.claude/`)

| Item | Status |
|---|---|
| Project `CLAUDE.md` | **Not present.** Project conventions currently live in Claude's auto-memory (see below) and in `92_WORKFLOW_UPGRADE_PLAN.md`. See §6 for a recommended minimal file. |
| `settings.local.json` | jdocmunch permission allow-list (above) |
| `memory/` | Versioned **snapshot** of Claude's session memory (mirrored into the repo on 2026-07-04): `MEMORY.md` index, `workflow-fin-bottleneck-diagnosis.md` (diagnosis + final workflow state), `workflow-fin-prompt-only-constraint.md` (working rules) |

**Live auto-memory** (read by Claude at session start, outside the repo):
`~/.claude/projects/-home-nekiee-WORKFLOW-FIN/memory/` — same three files; the repo
copy is a point-in-time mirror and must be re-copied after memory updates.

Persistent working rules stored there (they survive across sessions):
1. All workflow upgrades are **prompt-only** — no scripts, no pipeline code.
2. LLM computation is allowed **only for data missing from the inputs** (the list is `26_MISSING_DATA_LIST.md`); everything present in 10/13/14/15 is quoted.
3. Edits go to **templates** (17, 29, 70-series, 90) — never to user-prepared instances (16, 28).
4. Reports 61–66 and the 90/91/99\* docs are **illustrative examples**, not live artifacts.
5. The evaluation stage measures reasoning quality / instruction-following (anti-hallucination), **not** forecast accuracy — by design.

---

## 5. Skills developed inside this project (prompt techniques)

No `.claude/skills/` files exist — these "skills" are reusable prompt-engineering
patterns built into the workflow templates during the 2026-07-04 upgrade
(full detail: `92_WORKFLOW_UPGRADE_PLAN.md`):

| # | Technique | Where it lives | What it solves |
|---|---|---|---|
| 1 | **Calendar Gate + embedded authority table** (`NYSE_CALENDAR_2026`) | 17, 29 | Reference data embedded verbatim in the prompt beats data-injection bugs (holiday shipped as a forecast date) |
| 2 | **Named fallback rule** (`DAY+2 FALLBACK`) | 17, 29, 72 | One named, citable rule for a recurring edge case → identical behavior across models |
| 3 | **Exhaustive buckets** (bias thresholds 6.5/3.5) | 29 | Closing undefined gaps in decision hierarchies — every input maps to exactly one branch |
| 4 | **Canonical conflict resolution** (`RANGE_CONSTRAINED_BIAS`) | 29 | A fixed-format outcome sentence for a contradiction models used to improvise around |
| 5 | **3-state availability machine** (TDA UNAVAILABLE/WEAK/ACTIVE) + **data pre-flight** | 29, 72 | "Weak" ≠ "missing"; rules demanding absent data degrade to a fixed `INDETERMINATE` sentence instead of hallucination |
| 6 | **Unconditional sweep table** (Discrepancy Sweep) | 29 | Converting an implicit conditional ("note only if X≠Y") into a mandatory table fill — models fail conditionals, not tables |
| 7 | **CALC WORKSHEET: compute-only-missing-data, once, show work, quote elsewhere** + pinned nearest-rank percentiles | 29 (block 9), 26 | Arithmetic reliability without external computation; kills silent cross-model divergence from undefined conventions |
| 8 | **Machine-readable hand-off contract** (`SENTIMENT_PACKAGE` YAML) + CORE/EXTENDED priority classes + self-audit checklist | 17, 29 | Lossless Step1→Step2 hand-off; silent triage becomes visible `SKIPPED:` lines |
| 9 | **Transcription→verification split** (evaluator W0 FACT_CHECK) | 72 | Copy all numbers first (no judgment), then check row-by-row — numeric violations can't hide |
| 10 | **Grading Contract + precedence clauses** (72 is law, 70 is commentary; every deduction maps to a 28 requirement) | 70, 72 | Stops rubric/contract drift between documents |
| 11 | **Cross-batch calibration anchors** (re-read prior W3B/W10; justify >10-pt deviations) | 81, 83_1, 83_2 | Comparable scores across separately-scored evaluation batches |
| 12 | **QA fact-locks** (CALENDAR_GATE / DISCREPANCY_SWEEP / ROW_ORDER / FINAL_TABLE / WORKSHEET_CONSISTENCY locks) | 29 Stage 7 | Deterministic self-QA pass with named, greppable failure flags |

---

## 6. Recommended (optional): minimal project CLAUDE.md

If a `WORKFLOW_FIN/CLAUDE.md` is ever wanted, this captures the standing rules:

```markdown
# WORKFLOW_FIN — project rules
- Upgrades are PROMPT-ONLY: edit markdown templates, never write scripts/pipeline code.
- Edit TEMPLATES (17, 29, 70-series, 90) — never user-prepared instances (16, 28).
- LLM computation only for missing data per 26_MISSING_DATA_LIST.md; quote everything in 10/13/14/15.
- Reports 61–66 and 90/91/99* are illustrative examples, not live artifacts.
- Rubric authority: 72 > 70; generator contract authority: 28 (29 template).
- Master plan + status: 92_WORKFLOW_UPGRADE_PLAN.md.
```
