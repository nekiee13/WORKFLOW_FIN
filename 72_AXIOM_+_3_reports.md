I'm providing the evaluation framework. Acknowledge receipt and confirm you're ready for Phase 0.

"""
# AXIOM EVALUATION FRAMEWORK v3.0
# 3-Report Logic Evaluation
# Single Inference Call Architecture
# Ready for Phase 0 → Phase 1 execution
#
# NORMATIVE AUTHORITY: this document is the single source of truth for the
# evaluation rubric. 70_REPORT_REVIEW_MANUAL is explanatory commentary only;
# on any disagreement, THIS document wins. Deductions must additionally map to
# a 28_QUERY requirement per the Grading Contract (70 §7.4).

=================================================================
# CORE AXIOMS
=================================================================

## A1. CHART ABSENCE NEUTRALITY

Claims are evaluated on reasoning discipline only. No penalties are applied for missing visuals.

## A2. OBJECTIVE NARRATION

Third-person perspective is required. Personal pronouns are avoided. Sentences remain short.

## A3. TRACEABILITY

SCOPE (HARD): the EvidencePointer format binds the EVALUATOR'S OWN claims only
(CER ledger entries, issues, stress tests, contradiction analyses).

Every non-user claim made BY THE EVALUATOR requires an EvidencePointer in the format:
\[Rk|Sec="..."|Span=START:END|Quote="first 8-12 words"]

Generated reports (R1..RN) are NOT required to use EvidencePointer format.
Reports are graded only against the citation rules of 28\_QUERY (local \[^n]
footnotes; issuer-first sourcing; footnote list resolution). A traceability\_gap
deduction may be charged ONLY for a violation of 28\_QUERY's own citation rules,
per the Grading Contract (70\_REPORT\_REVIEW\_MANUAL). Never deduct because a
report's citations are "citation-style rather than EvidencePointer".

## A4. DETERMINISM

Same inputs produce same outputs. Thresholds are numeric. Algorithms are explicit.

## A5. USER DATA PRIMACY

User-supplied values are treated as ground truth.
No recomputation is allowed unless an explicit formula is stated.

=================================================================
# SYSTEM ROLE
=================================================================

Chief Logic Evaluator and Research Auditor operating under strict temporal,
citation, and structural constraints.

=================================================================
# OBJECTIVE
=================================================================

Three reports, R1-R3, on an identical subject and structure must be evaluated
and ranked by reasoning maturity and epistemic quality.

Primary focus:

* inductive and deductive rigor
* synthesis quality
* causal discipline
* coherence and completeness
* internal contradictions
* cross-report contradictions

Numerical exactness is secondary. Internal numerical inconsistency remains
diagnostic of reasoning errors.

=================================================================
# EVALUATION AXIOM
=================================================================

AXIOM: max(DecisionQuality(Ranking, ContradictionCoverage, Explainability, Reproducibility))

subject to ∀report r ∈ {R1..R3}:
(
ReasoningQuality(r) ∧
SynthesisInterlinking(r) ∧
CoherenceCompleteness(r) ∧
EpistemicCalibration(r) ∧
Traceability(r) ∧
FallacyDetection(r)
)

and subject to ∀pair (ri, rj), i≠j:
(
CrossReportIntegrity(ri, rj) ∧
ContradictionResolution(ri, rj)
)

=================================================================
# CLAIM MODEL
=================================================================

Each claim entry MUST include:

* ClaimID: unique within report, e.g. R2-C07
* ClaimText: short, testable statement
* ClaimType: descriptive | predictive | causal | normative | prescriptive
* Modality: TEXT\_VERIFIABLE | CHART\_DEPENDENT | HYBRID
* EpistemicStatus: ASSERTED | CONDITIONAL | HYPOTHETICAL
* Evidence: brief description of support
* ReasoningLink: how evidence supports claim
* Assumptions: required premises, at least one
* EvidencePointer: \[Rk|Sec="..."|Span=START:END|Quote="..."]

Modality definitions:

* TEXT\_VERIFIABLE: evaluable from text alone
* CHART\_DEPENDENT: requires visual interpretation
* HYBRID: partially text, materially visual

EpistemicStatus definitions:

* ASSERTED: stated as fact with no conditions
* CONDITIONAL: explicitly depends on conditions
* HYPOTHETICAL: framed as scenario or possibility

=================================================================
# SCORING RUBRIC
=================================================================

Use 0-4 per criterion:
0 = absent
1 = weak
2 = adequate
3 = strong
4 = exceptional

A) Reasoning Quality, 35%
A1. Deductive Validity
A2. Inductive Strength
A3. Causal Discipline
A4. Inferential Transparency
A5. Counterargument Handling

B) Synthesis & Interlinking, 25%
B6. Cross-section Integration
B7. Triangulation
B8. Conceptual Model Quality
B9. Insight Density
B10. Transferability

C) Coherence, Completeness, Consistency, 25%
C11. Internal Consistency
C12. Scope Completeness
C13. Assumption Management
C14. Operationalization
C15. Traceability Depth

D) Communication as Reasoning Support, 15%
D16. Structure Supports Reasoning
D17. Quant/Qual Clarity
D18. Limitations & Uncertainty
D19. Decision Usefulness

=================================================================
# DETERMINISTIC POINT DEDUCTION TABLE
=================================================================

Section A Errors:

* causal\_overreach: -2.5 points
* invalid\_inference: -3.0 points
* missing\_counterargument: -1.5 points
* scope\_leap: -2.0 points
* unjustified\_certainty: -1.5 points

Section B Errors:

* missing\_cross\_link: -2.0 points
* missing\_triangulation: -1.5 points
* conceptual\_model\_gap: -1.5 points
* low\_insight\_density: -1.0 points
* transferability\_confusion: -1.0 points

Section C Errors:

* numeric\_inconsistency: -2.0 points
* inconsistent\_definitions: -1.5 points
* schema\_omission: -3.0 points
* undeclared\_assumption: -1.5 points
* traceability\_gap: -1.5 points (chargeable ONLY for violations of 28\_QUERY's citation rules; see A3 SCOPE)

Section D Errors:

* structure\_jump: -1.0 points
* false\_precision: -1.0 points
* missing\_limitations: -1.5 points
* decision\_guidance\_detached: -1.5 points

Self-Audit Credit (STRICT):
The × 0.5 credit applies ONLY IF the report both (a) explicitly acknowledges the
error AND (b) adjusts the affected conclusion/output accordingly.
Disclosure WITHOUT resolution (error acknowledged but conclusion left unchanged)
takes the FULL deduction, plus a note: "disclosed-unresolved". Transparency about
an unfixed error must never outrank a report that fixed it.

Scoring Formula:
section\_score = MAX(section\_max - Σ(error\_count × deduction), 0.2 × section\_max)

Section maximums:

* A = 35
* B = 25
* C = 25
* D = 15

weighted\_total = A + B + C + D

=================================================================
# W0: FACT_CHECK WORKSHEET (MANDATORY; PRODUCE BEFORE ANY DECISION TREE)
=================================================================

Purpose: numeric violations get missed when extraction and judgment happen in one
interleaved pass. Split them. W0 is produced FIRST, before the CER ledger.

PASS 1 — TRANSCRIPTION ONLY (no judgment, no commentary):
For each report × ticker, copy values EXACTLY as printed in the report:

| Report | Ticker | Range\_Lo | Range\_Hi | Exact | Bias | Current | Band claims (verbatim) | Forecast dates |

Do not round, correct, or interpret during Pass 1. Missing value = "ABSENT".

PASS 2 — MECHANICAL CHECKS (row by row; one question at a time):
Append per row:

* RANGE\_OK: Exact ∈ \[Range\_Lo, Range\_Hi\]? (Y/N)
* BIAS\_OK: Bias sign consistent with (Exact − Current)? (Y/N; respect documented
  RANGE\_CONSTRAINED\_BIAS / BOUNDARY\_CONSTRAINED exemptions)
* BAND\_OK: each band claim matches the deterministic band definitions? (Y/N per claim)
* CALENDAR\_OK: forecast dates comply with the CALENDAR STANDARD (Phase 0)? (Y/N)

RULES:

* Tree 3 and Tree 4 findings may ONLY be triggered from W0 rows; no numeric
  finding may bypass the worksheet, and every numeric issue in the final output
  must cite its W0 row.
* Every N in Pass 2 must produce a corresponding Issue Log entry.
* If transcription is uncertain, mark the row TRANSCRIPTION\_UNCERTAIN and charge
  no deduction from it.

=================================================================
# ERROR RECOGNITION DECISION TREES
=================================================================

## Tree 1: Causal Overreach

TRIGGER, all must be true:

1. Claim contains: "causes", "drives", "leads to", "results in"
2. Evidence is correlation-only: r-value, co-movement, alignment
3. No mechanism explanation of at least 8 words
4. No temporality check

EXCEPTION:

* Claim is conditional, e.g. "may cause", "likely drives"
* Claim cites an external causal study

SEVERITY:

* S4 if it drives the primary forecast
* S3 if it drives a secondary recommendation
* S2 otherwise

## Tree 2: Missing Counterargument

TRIGGER:

1. Claim is prescriptive or confident predictive
2. Material impact affects more than 20% of forecast range
3. No nearby counterargument, risk, condition, or alternative within 50 words

EXCEPTION:

* Claim is hedge-qualified, e.g. likely, probable, under current conditions

SEVERITY:

* S3 if it affects the primary ticker forecast
* S2 if it affects a cross-asset theme
* S1 otherwise

## Tree 3: Numeric Inconsistency

TRIGGER (from W0 worksheet rows ONLY; never from ad-hoc recomputation):

1. W0 row has RANGE\_OK = N, or
2. W0 row has BIAS\_OK = N without a documented exemption, or
3. W0 row has BAND\_OK = N

SEVERITY:

* S4 if it affects Executive Summary forecast
* S3 if it affects ticker section forecast
* S2 otherwise

## Tree 4: Schema Omission

TRIGGER:

1. Required subsection missing from ticker section
2. Required table missing from Executive Summary or Final Forecasts
   (confirm numeric-table absences against W0 "ABSENT" entries)

SEVERITY:

* S3 always

## Tree 5: Invalid Inference

TRIGGER:

1. Conclusion C is stated as fact
2. Evidence E is provided
3. C does not logically follow from E
4. The gap is greater than two inference steps

SEVERITY:

* S4 if C is the primary forecast
* S3 if C is a key recommendation
* S2 otherwise

=================================================================
# CONTRADICTION MATERIALITY THRESHOLD
=================================================================

Log contradiction IF:

Impact\_Ri + Impact\_Rj >= 2.0

WHERE Impact = max of:

* Forecast range affected: |Range\_Ri.mid - Range\_Rj.mid| / ATR
* Bias flip: +3 if one = Higher and other = Lower
* Severity: S1 = 1, S2 = 2, S3 = 4, S4 = 8

=================================================================
# CONTRADICTION RESOLUTION RULES
=================================================================

Type A: TEXT\_CONTRADICTION

* Prefer side with stronger traceability.
* Traceability = avg(evidence\_depth) + internal\_consistency\_score.

Type B: CHART\_INTERPRETATION\_DIVERGENCE

* Do not claim chart truth.
* Resolve by reasoning discipline:
  1. epistemic calibration
  2. inferential transparency
  3. alternatives acknowledged
  4. internal coherence

Type C: MIXED\_SUPPORT

* Prefer TEXT\_VERIFIABLE side for factual resolution.
* Still score CHART\_DEPENDENT side for reasoning discipline.

=================================================================
# STRESS TESTS

=================================================================

Apply to each report:

T1. Premise Check
T2. Hidden Assumption Hunt
T3. Alternative Explanation Test
T4. Confounder / Selection Bias Test
T5. Temporal Logic Test
T6. Sensitivity Test
T7. Scope Integrity Test
T8. Consistency Scan

Each test is PASS or FAIL and requires an EvidencePointer.

=================================================================
# DETERMINISTIC GRADE MAPPING
=================================================================

Grade bands:

* Exceptional: ≥90%
* Strong: 80-89%
* Adequate: 70-79%
* Weak: 60-69%
* Poor: 50-59%
* Failing: <50%

grade(category) = band(category\_total / category\_max)

=================================================================
# REQUIRED WORK PRODUCTS FOR 3 REPORTS
=================================================================

W0. FACT\_CHECK Worksheet (transcription + mechanical checks; produced FIRST)
W1. Report Map for R1-R3
W2. CER Ledger, 10-25 claims per report
W3. Detailed Scorecards for R1-R3
W3B. Final Model Scorecard Overview for R1-R3
W3D. Section Error Summary for R1-R3
W4. Issue Log, severity-indexed
W5. Canonical Claim List, 25-30 claims
W6. Cross-Report Claim Matrix, 90 entries if 30 canonical claims are used
W7. Contradiction Matrix, typed and resolved
W8. Final Ranking, #1-#3
W9. Strengths Table
W10. Weaknesses Table
W11. Plain-Language Conclusions
W12. Executive Contradiction Brief
W13. Reasoning Hierarchy Summary
W14. Super-Truth Synthesis
W15. Trace Appendix

=================================================================
# PHASE 0: PREPARATION
=================================================================

## Step 0.1: Validation Pre-Flight

INPUT: Original query and user-supplied data.

Extract required fields:

* FH table: \[TNX, DJI, SPX, VIX, QQQ, AAPL] × \[Day1, Day2, Day3]
* STRUCTURAL\_CONTEXT: \[H20\_current, Regime\_current, Trend10D, WilliamsFractals] × 6 tickers
* TDA\_CONTEXT: \[H1\_MaxPersistence, H1\_CountAbove, H1\_Entropy] × 6 tickers, optional
* Indicators: \[RSI, ADX, ATR, Classic Pivot, ...] × 6 tickers
* Forecast tables: \[PyCaret, ARIMAX, PCE, LSTM, GARCH, VAR, RW, ETS] × 6 tickers

FOR each required field:
IF missing:
OUTPUT: MISSING\_USER\_INPUT: \<field\_name>
SET field\_value = NULL

TDA availability is a 3-STATE decision (HARD; must match 29\_QUERY\_Template):

IF TDA\_CONTEXT block is absent or blank:
STATE = TDA\_UNAVAILABLE; SET TDA\_AVAILABLE = false
OUTPUT: "TDA analysis disabled; StructuralAdjustment capped at ±1"

ELSE IF TDA\_CONTEXT is present but H1\_label = H1\_NONE:
STATE = TDA\_WEAK; SET TDA\_AVAILABLE = true
OUTPUT: "TDA available but weak (H1\_NONE); expected report behavior:
NEUTRAL\_STRUCTURE unless entropy rule fires; NO StructuralAdjustment cap;
TDA citations permitted."
Rule of interpretation (verbatim): "H1\_NONE means available but weak — never unavailable."
Do NOT penalize a report for citing TDA in this state; DO penalize a report
that declares TDA "unavailable/missing/disabled" in this state.

ELSE:
STATE = TDA\_ACTIVE; SET TDA\_AVAILABLE = true

ADDITIONALLY (any state): IF Persistence\_Sequence / Count\_Sequence (Last10) are
absent from TDA\_CONTEXT, the correct report behavior for Rule Set B is
"TDA\_Flip\_Risk: INDETERMINATE (sequence data not provided)." — grade flip-risk
handling against THAT standard, not against the full Rule Set B computation.

CALENDAR STANDARD (HARD; must match 29\_QUERY\_Template):
IF FH\_Date3 is a non-trading day (NYSE holiday or weekend), the CORRECT report
behavior is: Day+3 cells read "N/A (market closed)" AND the DAY+2 FALLBACK is
applied — anchors (ML\_Reference, FH\_sign, final-day projections) use FH\_Day2;
the outlier/divergence rules and Range Builder keep the provided Day-3 model set,
re-labeled as applying to the last effective session (per-model Day-2 values do
not exist in the input and must not be invented or rescaled).
Do NOT penalize a report for the fallback itself; DO penalize a report that emits
numeric Day+3 forecasts for a closed day, silently truncates the horizon, mixes
Day+3 anchors with Day+2 projections, or fabricates per-model Day-2 forecasts.

OUTPUT:
validation\_summary.json

## Step 0.2: Generate Canonical Claim List

INPUT:

* FH table
* STRUCTURAL\_CONTEXT

FOR each ticker in \[TNX, DJI, SPX, VIX, QQQ, AAPL]:

ADD:

* C\_{ticker}\_01: "{ticker} bias is Higher/Lower/Flat for Day+3"
* C\_{ticker}\_02: "{ticker} regime is PERSISTENT/RANDOM/MEAN\_REVERT"
* C\_{ticker}\_03: "{ticker} forecast range width is narrow/medium/wide"
* C\_{ticker}\_04: "{ticker} forecast confidence is Low/Moderate/High"

ADD cross-asset claims:

* C\_XA\_01: "VIX persistence creates equity downside risk"
* C\_XA\_02: "TNX up-yields increase QQQ/AAPL rate sensitivity"
* C\_XA\_03: "SPX forecast aligns with VIX persistence assessment"
* C\_XA\_04: "Event risk is properly integrated into forecasts"

Continue until 25-30 total canonical claims are created.

OUTPUT:
canonical\_claims.json

## Step 0.3: Initialize State Container

OUTPUT:
{
"schema\_version": "3.0",
"mode": "single\_call\_3\_reports",
"reports": \[],
"claims": \[],
"stress\_tests": \[],
"issues": \[],
"canonical\_claims": \[],
"crcm": \[],
"contradictions": \[],
"scorecards": \[],
"ranking": \[]
}

=================================================================
# PHASE 1: SINGLE-CALL EVALUATION OF R1-R3

=================================================================

## Step 1.1: Per-Report Structural Extraction

FOR each report Rk in \[R1, R2, R3]:

Extract sections:

* Executive Summary
* Current Environment
* Cross-Asset Themes
* Scenario Analysis
* TNX
* DJI
* SPX
* VIX
* QQQ
* AAPL
* Final Forecasts

For each section:

* store text
* char\_start
* char\_end
* word\_count

OUTPUT:
report\_map for R1-R3

## Step 1.2: Claim Extraction

FOR each report Rk in \[R1, R2, R3]:

Extract 10-25 claims.

For each ticker in \[TNX, DJI, SPX, VIX, QQQ, AAPL], extract:

1. Bias Claim

* ClaimID: R{k}-{ticker}-BIAS
* ClaimType: predictive
* Modality: TEXT\_VERIFIABLE
* EpistemicStatus: ASSERTED or CONDITIONAL
* EvidencePointer required

2. Regime Claim

* ClaimID: R{k}-{ticker}-REGIME
* ClaimType: descriptive
* Modality: TEXT\_VERIFIABLE
* EpistemicStatus: ASSERTED
* EvidencePointer required

3. Forecast Range Claim

* ClaimID: R{k}-{ticker}-RANGE
* ClaimType: predictive
* Modality: TEXT\_VERIFIABLE
* EpistemicStatus: ASSERTED or CONDITIONAL
* EvidencePointer required

Also extract cross-asset claims from:

* Cross-Asset Themes
* Scenario Analysis
* Final Forecasts

OUTPUT:
CER Ledger for R1-R3

## Step 1.3: Stress Test Battery

FOR each report Rk in \[R1, R2, R3]:

Apply:

* T1 Premise Check
* T2 Hidden Assumption Hunt
* T3 Alternative Explanation Test
* T4 Confounder / Selection Bias Test
* T5 Temporal Logic Test
* T6 Sensitivity Test
* T7 Scope Integrity Test
* T8 Consistency Scan

Each result must include:

* report
* test
* result: PASS or FAIL
* notes
* EvidencePointer

OUTPUT:
stress\_tests array

## Step 1.4: Error Detection

FOR each report Rk in \[R1, R2, R3]:

Apply:

* Tree 1: Causal Overreach
* Tree 2: Missing Counterargument
* Tree 3: Numeric Inconsistency
* Tree 4: Schema Omission
* Tree 5: Invalid Inference

Also detect:

* missing\_cross\_link
* missing\_triangulation
* conceptual\_model\_gap
* low\_insight\_density
* transferability\_confusion
* inconsistent\_definitions
* undeclared\_assumption
* traceability\_gap
* structure\_jump
* false\_precision
* missing\_limitations
* decision\_guidance\_detached

Each issue must include:

* report
* severity
* category
* description
* impact
* EvidencePointer

OUTPUT:
Issue Log for R1-R3

## Step 1.5: Section Error Accounting

FOR each report Rk in \[R1, R2, R3]:

Map issue categories to sections:

A:

* causal\_overreach
* invalid\_inference
* missing\_counterargument
* scope\_leap
* unjustified\_certainty

B:

* missing\_cross\_link
* missing\_triangulation
* conceptual\_model\_gap
* low\_insight\_density
* transferability\_confusion

C:

* numeric\_inconsistency
* inconsistent\_definitions
* schema\_omission
* undeclared\_assumption
* traceability\_gap

D:

* structure\_jump
* false\_precision
* missing\_limitations
* decision\_guidance\_detached

Deduplicate repeated errors.

OUTPUT:
Section Error Summary for R1-R3

## Step 1.6: Deterministic Scoring

FOR each report Rk in \[R1, R2, R3]:

Use:

* A max = 35
* B max = 25
* C max = 25
* D max = 15

Compute:
section\_score = MAX(section\_max - Σ(error\_count × deduction), 0.2 × section\_max)

Compute:
weighted\_total = A + B + C + D

Assign grade for each section.

OUTPUT:
Detailed Scorecard for each report.

## Step 1.7: Cross-Report Claim Matrix

FOR each canonical\_claim in canonical\_claims:

FOR each report in \[R1, R2, R3]:

```
IF matching claim exists:
  record:
  - canonical_claim_id
  - report
  - stance: agrees | disagrees | partially_agrees | not_addressed
  - support_modality
  - epistemic_status
  - EvidencePointer

ELSE:
  record:
  - stance: not_addressed
```

OUTPUT:
CRCM with 75-90 entries depending on canonical claim count.
If 30 canonical claims are used, output exactly 90 entries.

## Step 1.8: Contradiction Detection

FOR each canonical claim:

Compare all report pairs:

* R1 vs R2
* R1 vs R3
* R2 vs R3

IF disagreement is material under the contradiction materiality threshold:
log contradiction.

Each contradiction must include:

* contradiction\_id
* canonical\_claim\_id
* reports\_in\_conflict
* conflict\_statements
* EvidencePointers
* modality\_pair
* type: Type A, Type B, or Type C
* impact
* resolution\_note initially null

OUTPUT:
Contradiction Matrix

## Step 1.9: Contradiction Resolution

FOR each contradiction:

IF Type A:

* prefer the side with stronger traceability.

IF Type B:

* resolve by reasoning discipline, not chart truth.

IF Type C:

* prefer TEXT\_VERIFIABLE side for factual resolution.

OUTPUT:
Resolved Contradiction Matrix

## Step 1.10: Final Ranking

Rank R1-R3 by weighted\_total descending.

Tie rule:
IF score gap between adjacent reports is less than 3%:
mark as tie-band.

OUTPUT:
Final Ranking #1-#3 with differentiators.

## Step 1.11: Generate User-Facing Outputs

Produce the following in order:

1. W1 Report Map
2. W2 CER Ledger
3. W3 Detailed Scorecards
4. W3B Final Model Scorecard Overview
5. W3D Section Error Summary
6. W4 Issue Log
7. W5 Canonical Claim List
8. W6 Cross-Report Claim Matrix
9. W7 Contradiction Matrix
10. W8 Final Ranking
11. W9 Strengths Table
12. W10 Weaknesses Table
13. W11 Plain-Language Conclusions
14. W12 Executive Contradiction Brief
15. W13 Reasoning Hierarchy Summary
16. W14 Super-Truth Synthesis
17. W15 Trace Appendix

====================================================================
# FINAL MODEL SCORECARD FORMAT
====================================================================

# Final Model Scorecard

| Model | Weighted Total /100 | Reasoning Quality /35 | Synthesis & Interlinking /25 | Coherence, Completeness, Consistency /25 | Communication /15 |
| ----- | ------------------: | --------------------: | ---------------------------: | ---------------------------------------: | ----------------: |
| R1    |                 ... |                   ... |                          ... |                                      ... |               ... |
| R2    |                 ... |                   ... |                          ... |                                      ... |               ... |
| R3    |                 ... |                   ... |                          ... |                                      ... |               ... |

====================================================================
# FINAL RANKING FORMAT
====================================================================

# Final Ranking Summary

\#1: R{k} ({score}/100)
\#2: R{k} ({score}/100)
\#3: R{k} ({score}/100)

Key Insights:

* Top performer: R{k}
* Bottom performer: R{k}
* Most common error: {MOST\_COMMON\_ERROR}
* Most impactful contradiction: {HIGHEST\_IMPACT\_CONTRADICTION}

====================================================================
# VALIDATION CHECKLIST
====================================================================

Before completion, verify:

* [ ] W1 Report Map exists for R1-R3
* [ ] W2 CER Ledger contains 10-25 claims per report
* [ ] W3 Detailed Scorecards exist for R1-R3
* [ ] W3B Final Model Scorecard Overview exists
* [ ] W3D Section Error Summaries exist for R1-R3
* [ ] W4 Issue Log exists
* [ ] W5 Canonical Claim List contains 25-30 claims
* [ ] W6 CRCM contains 75-90 entries
* [ ] W7 Contradiction Matrix is typed and resolved
* [ ] W8 Final Ranking ranks #1-#3
* [ ] W9 Strengths Table exists
* [ ] W10 Weaknesses Table exists
* [ ] W11 Plain-Language Conclusions exist
* [ ] W12 Executive Contradiction Brief exists
* [ ] W13 Reasoning Hierarchy Summary exists
* [ ] W14 Super-Truth Synthesis exists
* [ ] W15 Trace Appendix exists
* [ ] All EvidencePointers are well-formed
* [ ] No chart-absence penalties were applied

IF all checks pass:
OUTPUT:

# VALIDATION: PASSED

# EVALUATION COMPLETE

```
IF any check fails:
OUTPUT:

# VALIDATION: FAILED

List missing or defective items.
```

====================================================================
# TERMINAL CONDITIONS
====================================================================

Evaluation is complete when:

1. All required work products W1-W15 are delivered.
2. All 3 reports are scored with deterministic rubric.
3. All contradictions are logged, typed, and resolved.
4. Final ranking #1-#3 is produced.
5. Validation checklist passes.

====================================================================
# END AXIOM EVALUATION FRAMEWORK v3.0
====================================================================
"""

Let me know when you're ready to continue.