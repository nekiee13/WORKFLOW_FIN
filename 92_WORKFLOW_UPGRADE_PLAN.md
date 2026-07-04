# 92 — WORKFLOW UPGRADE PLAN (Master)

**Prepared:** 2026-07-04
**Evidence base:** 20_GUIDE, 10/13/14/15 (inputs), 16/17 (sentiment prompt+template), 18 (sentiment deliverable), 28/29 (query+template), 61–66 (reports), 70/71/72/73/75/77/80/81/82/83/85 (evaluation machinery), 90/91, 99_2026-06-16, 99_2026-06-23, 99_2026-06-30 (evaluation results).
**Goal:** mitigate the weakness clusters that recur across ALL models in ALL three weekly evaluations, by upgrading three processing stages:

| Track | Stage upgraded | Measured by |
|---|---|---|
| 1 | 16_Sentiment_prompt processing | Quality of 18_Sentiment_Report |
| 2 | 28_QUERY (via 29_QUERY_Template) processing | Quality of reports 61–66 |
| 3 | Report evaluation (70–77, 80/82/85, 90) | Quality of 99_Report_Evaluation docs |

**Design principle — hard constraint: prompt-only.** Every fix must be achievable by editing the workflow's prompt/markdown documents. No scripts, no pipeline code, no changes to how upstream data files are generated. The available levers are:
1. Make contracts unambiguous and exhaustive (no undefined score gaps, no format mismatches between stages).
2. Remove LLM arithmetic entirely (user directive 2026-07-04: *no computing — LLMs use only user-provided input data*): every derived number arrives as user-prepared ground-truth data (the `27_DERIVED_METRICS` block, filled by the user outside the LLM and pasted into 28, same as 10/13/14/15); LLMs quote and interpret only.
3. Convert implicit conditional rules ("only if X ≠ Y") into unconditional mandatory tables — models fail conditionals; they rarely fail table fills.
4. Embed authoritative reference data (NYSE holiday calendar, indicator band lookup tables) verbatim in the prompts, and require rules to quote it.

Models fail on the same spots because those spots are underspecified or uncomputable — not because models are careless.

---

## 0. Diagnosis Summary (recurrence across weeks)

| # | Weakness (as seen in 99* docs) | Weeks seen | Root cause | Where to fix | Track |
|---|---|---|---|---|---|
| W1 | Calendar/horizon ambiguity (Juneteenth 06-19, Independence Day observed 07-03) | 06-16, 06-30 | Pipeline injects non-trading Day+3 dates (FH table contains 2026-07-03; NYSE closed). Models improvise: truncate, shift, or ignore | 16 + 29: embedded NYSE calendar block + Calendar Gate | 1+2 |
| W2 | Bias / Exact positioning tension (SPX, DJI, QQQ, AAPL, VIX, TNX) | all 3 weeks | AXIOM 2 Bias hierarchy has coverage gaps: scores in (3,4) and (6,7) undefined. Week 06-30 actual scores: AAPL 3.2, TNX 6.2, DJI 6.3, VIX 6.4 — all in gaps. Plus no canonical rule for "bearish sentiment but ML range floor above Current" | 28/29 AXIOM 2 | 2 |
| W3 | TDA handling (treated as unavailable, flip-risk overstated, cap misapplied) | all 3 weeks | Rule Set B requires 10-window `Persistence_Sequence` that 14_TDA never supplies; H1_NONE (available-but-weak) conflated with TDA unavailable — by generators AND by evaluator Phase 0 | 28/29 TDA rules (rewritten to the fields 14_TDA actually contains) + 72 Phase 0 | 2+3 |
| W4 | MAD/outlier arithmetic errors; loose range construction; technical-band misclassification (e.g., Williams %R −25.90 called overbought) | all 3 weeks | LLMs asked to do inline median/MAD/percentile/band arithmetic inside a ~97 KB prompt | User-prepared 27_DERIVED_METRICS ground-truth block + quote-don't-compute rules in 29 | 2 |
| W5 | Missing / incomplete Discrepancy Notes | 06-23, 06-30 | Rule is conditional ("only if Yahoo ≠ Investing") — models must detect the condition themselves across 6 tickers | 28/29: inject explicit checklist | 2 |
| W6 | Traceability penalized ("citation-style rather than EvidencePointer") | 06-23 esp. | Evaluator (72 A3) grades reports against EvidencePointer format that 28 never requires — contract mismatch between generator and evaluator | 72 + 70 (or 28) | 3 |
| W7 | Step-1 sentiment fields missing downstream (MISSING_USER_INPUT noise; AAPL bias artifact debates) | all 3 weeks | 18 delivers only Final Score/Bias/Confidence/Main Risk per ticker and is a **+2-day** report; 28 requires Base_Sentiment, Structural_Adjustment, Adjusted_Sentiment_Score, Drivers, Catalyst_Flip_Map per ticker over 3 days | 16/17 output contract | 1 |
| W8 | Density / merged tables & prose / audit friction | all 3 weeks | Conflicting instructions (expand depth for parity vs FK≤9 vs word caps) with no layout rules | 28/29 output requirements | 2 |
| W9 | Cross-batch ranking incoherence risk; 90 prompt hardcodes R1–R6 | structural | 80/82/85 scored in separate uncalibrated sessions, then merged by 90 | 90 + eval process | 3 |

---

## TRACK 1 — Sentiment stage (16 → 18)

### 1.1 Define a machine-readable Step-1 output contract (`SENTIMENT_PACKAGE`)
**Problem:** 28_QUERY §SENTIMENT_CONTEXT names 9 per-ticker fields it consumes. 18 supplies ~4 of them, in prose/table form that downstream models must scrape. This is the single largest source of MISSING_USER_INPUT noise and of the AAPL/SPX bias debates.
**Change (edit 16 + 17):** append to the Terminal Condition a mandatory final block, emitted verbatim as fenced YAML, one entry per ticker:

```yaml
SENTIMENT_PACKAGE:
  ASOF: 2026-06-30
  EFFECTIVE_TRADING_DAYS: [2026-07-01, 2026-07-02]   # holiday-aware; see 1.2
  MSC: {score: 4.4, state: Mixed/Divergent, confidence: Medium}
  tickers:
    SPX:
      Base_Sentiment: 4.5
      Structural_Adjustment: -0.5
      Soft_Adjustment: 0.0
      Adjusted_Sentiment_Score: 4.0
      CoherenceScore: 1          # now REQUIRED (deterministic from SVL; formula in 28 Stage 4)
      Confidence: Medium
      Mechanical_Drivers: ["below-pivot close", "RSI neutral"]
      Fundamental_Drivers: ["jobs-report repricing risk"]
      Catalyst_Flip_Map: "Soft NFP print (<150k) flips bias constructive"
      Sentiment_Rationale: "one sentence"
```

Rules: numbers only in the numeric fields; every field mandatory; `MISSING:` prefix allowed only with a stated reason. The narrative report remains, but the package is the authoritative hand-off artifact.
**Acceptance:** Step 2 runs produce **zero** `MISSING_USER_INPUT: <sentiment field>` flags; 28's pass-through arithmetic (Base + Structural = Adjusted) validates for all 6 tickers.

### 1.2 Holiday-aware horizon (kills W1 at the source)
**Problem:** 16 injects "FH: 3 business days — 2026-07-01, 07-02, 07-03" while NYSE is closed 07-03; 18 self-corrected into a "+2-Day" report, so Step 1 and Step 2 disagree about the horizon.
**Change (edit 16 only):** embed a `NYSE_CALENDAR_2026` block (the full-year holiday + early-close list; maintained by hand once per year) and add a mandatory Stage-0 **Calendar Gate**: cross-check every FH date against the list, then emit `EFFECTIVE_TRADING_DAYS` and a `CALENDAR_NOTE` line (e.g., "2026-07-03: closed — Independence Day observed; horizon = 2 sessions"). Non-trading FH dates are marked `CALENDAR_SUPERSEDED`, never silently dropped. Step 1 must produce sentiment **for each effective day**, never silently retarget to a single day.
**Acceptance:** 18's target dates == 28's forecast dates == EFFECTIVE_TRADING_DAYS, exactly.

### 1.3 Right-size the demanded output
**Problem:** 16 (67 KB) demands GeneralSections + 7 per-ticker sections; the actual deliverable was 8.5 KB and skipped most blocks — the contract is over-specified relative to what Step 2 consumes, so models triage arbitrarily.
**Change (edit 16):** split requirements into **CORE (hard)** — the SENTIMENT_PACKAGE, MSC block, per-ticker Sentiment blocks, Events tables — and **EXTENDED (soft)** — geopolitical overlay, soft-indicator essays. End with a mandatory self-audit checklist table (`block | present Y/N`) so omissions are visible instead of silent.
**Acceptance:** all CORE blocks present in the next 18; checklist emitted.

---

## TRACK 2 — Forecast stage (28/29 → 61–66)

### 2.1 Calendar authority block (W1)
**Change (29 template only):** paste the same `NYSE_CALENDAR_2026` block + Calendar Gate as 1.2. Add one deterministic rule: *if FH_Date3 is a non-trading day, Day+3 forecast is marked `N/A (market closed)` in every table; ranges/exacts are produced only for effective days; FH table values for closed days are ignored and flagged `CALENDAR_SUPERSEDED`.* Plus the named **DAY+2 FALLBACK** rule: anchors (ML_Reference, FH_sign, final-day projections) fall back to FH_Day2 — projections must align with Day+2 forecasting; the outlier/divergence/Range Builder rules keep the provided Day-3 model set re-labeled to the last effective session, because per-model Day-2 forecasts do not exist in the input and must never be invented or rescaled (that would recreate the uncomputable-rule trap). 15_fh3_table stays as-is (it is generated upstream and out of scope); the Calendar Gate deterministically supersedes it inside the prompt, so the conflict is neutralized even when a closed day ships in the data.
**Acceptance:** zero calendar-related weaknesses in next 99 eval; all 6 reports agree on the horizon.

### 2.2 Close the Bias hierarchy gaps + canonical conflict rule (W2)
**Change (29, AXIOM 2 Bias Determination):**
- Make Level 1 buckets exhaustive: `≥ 6.5 → Higher`, `≤ 3.5 → Lower`, `(3.5, 6.5) → Level 2`. (No score can fall between buckets; aligns with the Exact-positioning zones.)
- Add the **Range-Constrained Bias rule** (the recurring AAPL artifact): *if Sentiment ≤ 3.5 but Range_Lo > Current (or ≥ 7 but Range_Hi < Current), then Bias = direction of (Exact − Current), annotated `RANGE_CONSTRAINED_BIAS: <ticker>` with one fixed-format explanation sentence.* One canonical outcome, identical across models — ends the per-model improvisation.
**Acceptance:** zero BIAS_POSITIONING_CONFLICT / bias-tension findings in next 99 eval; all models produce identical Bias per ticker.

### 2.3 Eliminate LLM arithmetic — derived numbers become user-prepared input data (W4) — ✅ APPLIED 2026-07-04
**Design (user directive: no LLM computing; LLMs use only user-provided input data):** `27_DERIVED_METRICS_Template.md` is a **user-filled ground-truth template**, computed by the user outside the LLM and pasted into 28 alongside 10/13/14/15. Per ticker it carries: N_models, min/max/median(P), MAD, MAD_floor, outlier list, dispersion trigger (+ which rule), Range_Lo/Range_Hi + branch fired, precomputed placement-zone markers P20–P80 (so Exact positioning and the 40/50/60% consistency checks need no percentage arithmetic), Classic_Pivot, 0.10×ATR, 0.25×ATR, pivot proximity, ATR%, and indicator Zone classifications matching 29's deterministic bands.
**29 consumption rules (applied):** AXIOM 0 gained the DERIVED_METRICS Contract with the NO-COMPUTE RULE; Rules 13–14, the Range Builder, Step-3 placement, the Consistency Check, the SENTIMENT_CONSISTENCY_LOCK, the indicator table and ATR% all changed from "compute" to "quote"; former formulas remain as *definitions of record* (documentation of how the user computes the values); a new Stage-7 `DERIVED_METRICS_LOCK` fails any value that deviates from the injected block; the input-context appendix gained the DERIVED_METRICS insertion marker. Graceful degradation: an ABSENT field → `MISSING_USER_INPUT` + legacy flagged-formula fallback (branch D of the Range Builder is inherently such a case).
**Acceptance:** zero MAD/outlier arithmetic findings and zero band-misclassification findings in next 99 eval; Range values identical across all 6 reports.

### 2.4 Rewrite TDA rules to match what 14_TDA actually contains (W3)
**Change (29 only — 14_TDA stays as-is, it is generated upstream and out of scope):**
- Rule Set B currently demands a 10-window `Persistence_Sequence` that 14_TDA never supplies — an uncomputable rule, and the single biggest source of cross-model improvisation. Make it conditional: *IF the sequence fields are present in TDA_CONTEXT → apply the existing flip-risk logic. ELSE → emit the fixed verbatim sentence `TDA_Flip_Risk: INDETERMINATE (sequence data not provided)`; no StructuralAdjustment cap applied; no improvised flip-risk narrative.*
- 29 defines a 3-state machine: `TDA_UNAVAILABLE` (block absent/blank) / `TDA_WEAK` (present, H1_label = H1_NONE → Structure_Signal = NEUTRAL_STRUCTURE unless entropy rule fires; **no** StructuralAdjustment cap; TDA may be cited) / `TDA_ACTIVE`. Explicit sentence: *"H1_NONE means available but weak — never unavailable."*
**Acceptance:** zero TDA-handling findings in next 99 eval (was present in all three weeks for nearly every model); all 6 reports emit the identical INDETERMINATE sentence while sequences are absent.

### 2.5 Discrepancy Sweep — make the conditional rule unconditional (W5)
**Change (29 only):** replace the conditional rule ("note only if Yahoo ≠ Investing") with a mandatory **Discrepancy Sweep table** emitted early in the report: one row per ticker × compared field — Yahoo value | Investing value | `EQUAL Y/N` | `NOTE_REQUIRED Y/N`. Then the rule becomes mechanical: every `NOTE_REQUIRED=Y` row must have a Discrepancy Note; every `N` row must not. QA Stage 7 gains the matching lock. Models fail implicit condition detection across 6 tickers; they rarely fail filling a required table.
**Acceptance:** discrepancy-note coverage 100% in next run (was a top-2 weakness for the best report, R3/Opus, on 06-30).

### 2.6 Traceability format — align generator with evaluator (W6, with 3.1)
**Change (29):** keep `[^n]` footnotes but require each event-table row and each externally-sourced prose claim to carry its own local footnote (no grouped citations). Add the machine-checkable form the evaluator already looks for: footnote list entries as `[^n]: Publisher — Title — (section where used)`.
**Acceptance:** no "grouped citations"/"traceability gap" deductions attributable to format alone.

### 2.7 Layout rules (W8)
**Change (29, Output Requirements):** three lines: tables never embedded inside sentences; one blank line between any table and prose; per-ticker prose stays within 450–550 words with the existing three plain-English notes. Drop no content rules — this is presentation only.
**Acceptance:** "density/merged structure" findings decline in next 99 eval.

### 2.8 Order & schema locks
**Change (29, QA Stage 7):** add two cheap locks: Executive Summary row order == SPX→DJI→QQQ→VIX→TNX→AAPL (Qwen violated on 06-23); Final Forecasts table presence (LeChat missed on 06-16).

---

## TRACK 3 — Evaluation stage (70–77, 80/82/85, 90 → 99*)

### 3.1 Scope the EvidencePointer axiom correctly (W6)
**Change (72 A3 + 70 §7.4):** state explicitly: *EvidencePointer format is required for the **evaluator's own** claims (CER ledger, issues, stress tests). Generated reports are graded only against the citation rules of 28_QUERY (local `[^n]` footnotes). `traceability_gap` may be charged only for violations of 28's rules.* Add a **Grading Contract table** to 70: each deduction category ↦ the exact 28 requirement it tests. No deduction without a mapped requirement.
**Acceptance:** zero weaknesses of the form "citations not in EvidencePointer format" in next 99 eval.

### 3.2 Fix evaluator's TDA pre-flight (W3)
**Change (72 Phase 0, Step 0.1):** replace "IF TDA_CONTEXT missing **or blank** → TDA disabled" with the same 3-state machine as 2.4, so the evaluator grades TDA handling against the correct standard.

### 3.3 Fact-check as a transcription→verification worksheet
**Why prompt-only works here:** the evaluator misses numeric violations because extraction and judgment happen in one interleaved pass. Split them.
**Change (72 — new mandatory W-step before the Decision Trees; optionally runnable as a tiny standalone pre-pass prompt per batch, same pattern as 77, with its output pasted into the eval prompt):** a two-pass `FACT_CHECK` worksheet. **Pass 1 — transcription only, no judgment:** per report × ticker, copy Range_Lo, Range_Hi, Exact, Bias, Current, and every band claim into a table. **Pass 2 — mechanical row-by-row checks:** Exact ∈ [Range_Lo, Range_Hi]? Bias consistent with (Exact − Current) sign? Band claim matches the embedded lookup table? Forecast dates calendar-compliant? Decision Trees 3 & 4 then consume this worksheet instead of re-deriving numbers from the PDFs; LLM effort concentrates on reasoning quality (Trees 1, 2, 5), where it adds value.
**Acceptance:** numeric findings in 80/82/85 match the worksheet 1:1; no missed range violations (the R4/LeChat QQQ 730 ∉ [738, 749] case is exactly what row-by-row transcription catches every time).

### 3.4 Cross-batch calibration (W9)
**Change (process + 90):**
- Batch evals stay ≤3 reports (context limit is real), but every batch after the first receives the previous batches' **W3B scorecards + W10 weakness tables only** (~2 KB) as calibration anchors, with the instruction: *"score on the same scale; justify any section score that deviates >10 points from an anchor report of similar completeness."*
- Rewrite 90 to take `R1..RN` (N injected), require the merged ranking to state, for each adjacent pair from different batches, one sentence justifying the order (forces active reconciliation instead of naive concatenation).
**Acceptance:** re-running 90 on the same inputs reproduces the same ranking; no cross-batch score anomalies (e.g., a "broadly complete" report scoring below a "materially compressed" one from another batch).

### 3.5 Tighten self-audit credit
**Change (72 Deduction Table):** credit (×0.5) applies **only if the conclusion was adjusted**; disclosure without resolution takes the full deduction plus a note. (06-16 showed disclosure-heavy reports outranking resolved ones — the incentive is currently backwards.)

### 3.6 Add outcome scoring (new signal, low cost)
**Change (new small prompt doc, 78_ACCURACY_POSTMORTEM.md):** after each week closes, the user pastes the realized closes plus each report's Final Forecasts table into this short prompt; it produces the hit-rate table (Exact error, Range hit Y/N, Bias correct Y/N per report × ticker × day) using the same transcription→comparison worksheet pattern as 3.3, appended to the weekly 99. Report quality (process) and forecast accuracy (outcome) become separate, trackable axes; over weeks this shows whether "better reports" actually forecast better.

---

## 4. Scope note on example artifacts

Reports 61–66, 90/91 and the 99* documents in this repo are **illustrative examples** supplied so bottlenecks could be identified — not live artifacts of this repo. File-level observations about them (empty 65, 91≡99 duplication, naming) are non-issues and out of scope. The single calendar authority (`NYSE_CALENDAR_2026` in 17/29/72) was applied via Phase A.

---

## 5. Phased rollout (small steps, each independently testable — all phases are prompt edits only)

**Phase A — targeted edits to existing prompts — ✅ APPLIED 2026-07-04 to the templates (17, 29, 70, 72, 90); user-prepared data instances (16, 28) untouched and pick up the changes at next assembly:**
A1. Bias bucket closure + Range-Constrained Bias rule (2.2)
A2. TDA conditional Rule Set B + 3-state wording in 29 and 72 (2.4, 3.2)
A3. Discrepancy Sweep table (2.5)
A4. NYSE_CALENDAR_2026 block + Calendar Gate + Day+3-closed rule in 16/29 (1.2, 2.1)
A5. EvidencePointer scoping + Grading Contract (3.1); self-audit credit fix (3.5); 90 → R1..RN (3.4 text part)
A6. Layout rules + order/schema locks (2.7, 2.8)
*Expected effect: eliminates W1, W2, W3, W5, W6, W8 — well over half of all weakness findings across the three weeks.*

**Phase B — new input-data contract + hand-off contract:**
B1. `27_DERIVED_METRICS_Template.md` (user-filled ground-truth block) + quote-don't-compute rules in 29 (2.3) — ✅ APPLIED 2026-07-04
B2. SENTIMENT_PACKAGE contract in 17 + consumption wording in 29 (1.1, 1.3) — ⬜ pending
*Expected effect: eliminates W4 and W7; Step 1 → Step 2 hand-off becomes lossless.*

**Phase C — evaluation quality (prompt/process only):**
C1. FACT_CHECK transcription→verification worksheet in 72 (or as a tiny pre-pass prompt) (3.3) — ✅ APPLIED 2026-07-04 as mandatory work product W0; Trees 3 & 4 now trigger only from W0 rows
C2. Cross-batch calibration anchors pasted between batches (3.4)
C3. `78_ACCURACY_POSTMORTEM.md` prompt (3.6) — downgraded to OPTIONAL: user confirmed the 70-series intentionally measures reasoning quality / instruction-following, not forecast accuracy; outcome scoring would be a separate optional axis, never merged into the rankings

**Drift guard — ✅ APPLIED 2026-07-04:** precedence clauses added: 70 header declares 72 the single normative source (72 wins on any disagreement); 72 header declares its authority and requires deductions to map to 28 via the Grading Contract.

## 6. Measurement (per track, per week)

| Track | KPI | Baseline (06-30) | Target |
|---|---|---|---|
| 1 | MISSING_USER_INPUT (sentiment fields) across 6 reports | recurring | 0 |
| 1 | Step1/Step2 horizon agreement | disagree (+2d vs 3d) | exact match |
| 2 | Bias-tension + range-violation findings in 99 | 4 of 6 reports | 0 |
| 2 | TDA-handling findings in 99 | ~5 of 6 reports | 0 |
| 2 | Arithmetic/band findings in 99 | 3+ reports | 0 |
| 2 | Discrepancy-note coverage | incomplete | 100% |
| 3 | Format-mismatch deductions (EvidencePointer) | present | 0 |
| 3 | Ranking reproducibility on re-run | untested | identical |
| all | Mean W3B weighted total across models | 82.4 | +5 pts in 2 weeks |
