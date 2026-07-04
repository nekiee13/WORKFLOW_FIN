---
name: workflow-fin-bottleneck-diagnosis
description: WORKFLOW_FIN forecast pipeline — root-cause diagnosis and FINAL upgraded state (plan 92 complete, all changes pushed as of 2026-07-04)
metadata:
  type: project
  originSessionId: c0fe27a1-20bf-43c4-a4d1-9f53775d4a06
---

WORKFLOW_FIN is a 3-stage LLM market-forecast workflow: Step 1 sentiment (17 template → 16 filled instance → 18 report), Step 2 forecast reports (29 template → 28 filled QUERY → reports by multiple LLMs), Step 3 evaluation (70 manual / 72 normative framework / 73-77 plan+execute, batched ≤3 reports via 81/83 continuations, merged by 90 → weekly 99 docs). Inputs: 00–06 aggregate into 10_Calculations; 13_SVL, 14_TDA, 15_fh3 feed 16/28. Reports 61–66 and 90/91/99* in the repo are ILLUSTRATIVE EXAMPLES only. The eval deliberately measures reasoning quality / instruction-following (anti-hallucination), NOT forecast accuracy — user considers this a critical design property.

Diagnosed root causes (verified against three weekly evals, 2026-06-16/23/30): (1) non-trading days injected as forecast dates; (2) AXIOM 2 bias-bucket gaps at scores (3,4) and (6,7); (3) TDA Rule Set B demanded Last10 sequences 14_TDA never supplies + H1_NONE conflated with "unavailable"; (4) inline LLM arithmetic (median/MAD/percentiles/bands) fails, and the percentile method was never defined (hidden cross-model divergence); (5) Step1→Step2 contract broken (18 lacked required fields, wrong horizon); (6) evaluator graded against a format the generator never saw; uncalibrated batch merging.

FINAL STATE (2026-07-04, plan 92 COMPLETE, repo in sync at commit 79043ad):
- 17 (Step 1 template): NYSE_CALENDAR_2026 + Calendar Gate (never silently retarget horizon); DAY+2 FALLBACK in Executive Summary; PRIORITY CLASSES (CORE may never be omitted / EXTENDED needs explicit SKIPPED lines); mandatory final SENTIMENT_PACKAGE fenced-YAML block (Base/Structural/Soft/Adjusted scores, CoherenceScore, Confidence, Drivers, Catalyst_Flip_Map, Rationale per ticker + ASOF/EFFECTIVE_TRADING_DAYS/CALENDAR_NOTE/MSC); SELF-AUDIT CHECKLIST; Terminal Condition enforces all three.
- 26 (new): MISSING_DATA_LIST — the 11 quantities absent from inputs (and therefore the ONLY things LLMs may compute) vs the quote-only inventory; single doc to update if input data ever changes.
- 29 (Step 2 template): exhaustive 6.5/3.5 bias buckets + Range-Constrained Bias rule (canonical sentiment-vs-range resolution); TDA 3-state machine (UNAVAILABLE/WEAK/ACTIVE; H1_NONE = available-but-weak) + Rule Set B data pre-flight (fixed "TDA_Flip_Risk: INDETERMINATE" sentence when sequences absent); unconditional Discrepancy Sweep table (block 2b); Calendar Gate + DAY+2 FALLBACK (anchors ML_Reference/FH_sign/projections → FH_Day2; outlier/divergence/Range keep the provided Day-3 model set re-labeled — never invent per-model Day-2 values); CALC WORKSHEET (global block 9, fixed 15-row QUOTE/COMPUTE schema, operands shown, pinned nearest-rank percentiles ceil(k·n/100)); SENTIMENT_CONTEXT parses SENTIMENT_PACKAGE as authoritative (NARRATIVE_FALLBACK, HORIZON_MISMATCH); layout rules; Stage-7 locks: CALENDAR_GATE, DISCREPANCY_SWEEP, ROW_ORDER, FINAL_TABLE, WORKSHEET_CONSISTENCY, SENTIMENT_CONSISTENCY at 6.5/3.5 via P50.
- 70: precedence clause (72 is the law, 70 is commentary) + Grading Contract table in §7.4 (no deduction without a mapped 28 requirement).
- 72: normative-authority header; A3 EvidencePointer scoped to the evaluator's own claims; strict self-audit credit (×0.5 only if conclusion adjusted); Phase 0 has the 3-state TDA machine + CALENDAR STANDARD matching 29; W0 FACT_CHECK worksheet (transcription pass then mechanical checks; Trees 3/4 may fire ONLY from W0 rows; WORKSHEET_OK cross-check).
- 81 / 83_1 / 83_2: cross-batch calibration anchors (re-read previous batches' W3B+W10; justify >10-pt section-score deviations from anchors of similar completeness).
- 90: parameterized R1..RN + mandatory reconciliation sentence per adjacent cross-batch ranking pair.
- Not done, by decision: C3 accuracy postmortem (optional separate axis only — must never merge into rankings); housekeeping (removed as non-issue — example files).

Acceptance test pending: the next weekly run. KPIs in 92 §5–6: zero MISSING_USER_INPUT sentiment flags, exact Step1/Step2 horizon match, identical Ranges across all reports, zero bias-tension/TDA/arithmetic/band findings in the next 99 eval; baseline mean W3B 82.4 (2026-06-30), target +5 in 2 weeks.

Working rules for future sessions: see [[workflow-fin-prompt-only-constraint]] (prompt-only; compute only missing data; templates not instances; examples are examples).
