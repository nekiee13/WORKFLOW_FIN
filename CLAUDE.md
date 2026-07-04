# WORKFLOW_FIN — project rules

3-stage LLM market-forecast workflow. Step 1 sentiment (17 template → 16 filled → 18 report),
Step 2 forecast (29 template → 28 filled QUERY → reports by multiple LLMs), Step 3 evaluation
(70 manual, 72 normative framework, 73–77 plan/execute, 81/83 batch continuations, 90 merge → 99 results).
Inputs: 00–06 aggregate into 10_Calculations; 13_SVL, 14_TDA, 15_fh3 feed Steps 1–2.

## Hard rules

- Upgrades are **PROMPT-ONLY**: edit markdown templates, never write scripts or pipeline code,
  never change how upstream data files (13/14/15) are generated.
- Edit **TEMPLATES** (17, 29, 70-series, 90) — never user-prepared instances (16, 28).
  Input DATA is user-prepared.
- LLM computation is allowed **only for data missing from the inputs** — the definitive list is
  `26_MISSING_DATA_LIST.md`. Everything present in 10/13/14/15 is quoted verbatim, never recomputed.
  Missing quantities are computed once, in 29's CALC WORKSHEET (global block 9), work shown.
- Do **not** propose new user-prepared data files or LLM "computation worksheet" prompts —
  both designs were explicitly rejected.
- Reports 61–66 and 90/91/99\* are **illustrative examples**, not live artifacts.
  Never treat their file-level quirks (empty files, duplicates, naming) as workflow issues.
- The evaluation stage measures reasoning quality / instruction-following (anti-hallucination),
  **not** forecast accuracy — by design. Outcome scoring, if ever added, stays a separate axis
  and never merges into the rankings.

## Authority chain

- Generator contract: **28** (from 29 template) defines what reports must do.
- Rubric: **72** is the law; 70 is commentary — on disagreement, 72 wins.
- Every evaluator deduction must map to a 28 requirement (Grading Contract, 70 §7.4).
- Calendar: the `NYSE_CALENDAR_2026` block in 17/29/72 supersedes any injected date
  (hand-maintained; refresh each January).

## Key documents

- `92_WORKFLOW_UPGRADE_PLAN.md` — master plan + per-fix status (complete as of 2026-07-04).
- `26_MISSING_DATA_LIST.md` — what LLMs may compute vs must quote.
- `93_CLAUDE_SETUP.md` — Claude configuration + the 12 prompt techniques used here.
- `20_GUIDE.md` — how the staged Step-2 prompt is assembled.

## Working style

- Use jdocmunch for reading these documents (repo `local/WORKFLOW_FIN`): outlines and
  targeted sections, not whole-file loads. Most are 30–100 KB.
- Approach enhancements in small steps; huge information volume — context economy matters.
