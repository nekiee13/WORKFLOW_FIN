# Manual for the Axiom Evaluation Framework v3.0

> **PRECEDENCE (HARD):** This manual is explanatory commentary. The single
> normative source for the evaluation rubric is `72_AXIOM` (Axiom Evaluation
> Framework v3.0). If this manual and 72 disagree on any rule, threshold,
> deduction, or format, **72 wins**. Rule changes are made in 72 first; this
> manual is then updated to match.

## 1. Purpose of the Framework

The **Axiom Evaluation Framework v3.0** is a structured method used to judge market forecast reports.

The framework checks whether a report is:

* Complete
* Logical
* Consistent
* Well supported by evidence
* Clear enough for decision use
* Honest about uncertainty
* Stable across tables, claims, and final forecasts

The framework does not reward long text by itself. A report must show clear reasoning, valid numbers, and traceable evidence.

***

## 2. Core Evaluation Principles

### 2.1 Text-First Review

The report is judged mainly from its written content.

Charts may help, but missing charts are not penalized when the rule says **chart-absence neutral**.

**Purpose:**  
This prevents a report from being punished only because visuals are absent. The focus stays on logic, claims, numbers, and evidence.

***

### 2.2 Deterministic Review

The same rules are applied to each report.

The evaluator should avoid personal preference. Each report is checked against the same benchmark objects.

**Purpose:**  
This keeps scoring fair across all reports.

***

### 2.3 Evidence-Based Review

Each important claim should be linked to text evidence.

Strong reports make it clear where a claim came from. Weak reports may include claims without proof, broken references, or vague source names.

**Purpose:**  
This allows each forecast, bias, and risk statement to be checked.

***

### 2.4 Bias and Exact Forecast Alignment

A directional bias should match the forecast number unless a clear rule explains the conflict.

Example:

* Current VIX = 18.06
* Forecast exact = 17.85
* Bias = Higher

This creates a conflict because the exact value is below current while the label says Higher.

**Purpose:**  
This test checks whether the report’s direction label agrees with its own numbers.

***

### 2.5 Scope Discipline

The report must stay inside the stated forecast window.

For a 3-day forecast, medium-term events should not drive the base case unless clearly marked as background risk.

**Purpose:**  
This prevents June events from being used as direct support for a May 20–22 forecast.

***

## 3. Main Report Objects Checked

Each report is treated as an object made of parts.

The key objects are:

1. Header
2. Executive Summary
3. Current Environment
4. Cross-Asset Themes
5. Scenario Analysis
6. Ticker Sections
7. Forecast Tables
8. Technical Tables
9. ML and Model Notes
10. Event Calendar
11. Risk Management
12. References
13. Final Forecast Table
14. QA or Audit Summary

A strong report does not need perfect prose. It needs a complete and logical structure.

***

# 4. Benchmark Tests W1–W15

## W1. Report Map

### What Is Checked

The Report Map checks which required sections are present.

Typical sections include:

* Header
* Executive Summary
* Current Environment
* Cross-Asset Themes
* Scenario Analysis
* SPX section
* DJI section
* QQQ section
* VIX section
* TNX section
* AAPL section
* Final Forecasts
* References

### How the Test Works

Each section is marked as:

* **Found**
* **Partial**
* **Missing**

A note is added when a section exists but is weak.

### Purpose

The Report Map answers a basic question:

> Does the report contain the required parts?

A report cannot be strong if required sections are absent or only claimed to exist.

### Common Failure Types

* Missing ticker sections
* Partial ticker sections
* Final table absent
* References present but unusable
* Sections stated as complete but not shown

***

## W2. CER Ledger

CER means:

* **Claim**
* **Evidence**
* **Reasoning**

### What Is Checked

The CER Ledger checks selected claims from each report.

Each claim is reviewed by fields such as:

* Claim ID
* Claim text
* Claim type
* Evidence
* Reasoning link
* Assumptions
* Status
* Evidence pointer

### Claim Types

Common claim types include:

* **Predictive:** A forecast or bias claim  
  Example: “SPX bias is Lower.”

* **Descriptive:** A statement about report content or market state  
  Example: “R2 is incomplete.”

* **Causal:** A cause-and-effect claim  
  Example: “Higher TNX pressures QQQ.”

### Status Labels

Common status labels include:

* **ASSERTED:** The report states the claim.
* **CONDITIONAL:** The claim depends on a condition.
* **PARTIAL:** The report partly supports the claim.
* **UNSUPPORTED:** Evidence is weak or missing.

### Purpose

The CER Ledger checks whether important claims are supported by evidence and reasoning.

A forecast is not enough by itself. The report must show why the forecast was made.

### Common Failure Types

* Claim has no local evidence
* Reasoning does not follow from evidence
* Hidden assumptions are not named
* Exact forecast and bias conflict
* Causal claim is too strong

***

## W3. Detailed Scorecard

### What Is Checked

The report is scored across four major sections:

1. **Reasoning Quality** — 35 points
2. **Synthesis & Interlinking** — 25 points
3. **Coherence, Completeness, Consistency** — 25 points
4. **Communication** — 15 points

Total score = 100 points.

***

## W3-A. Reasoning Quality

### What Is Checked

This section checks whether the report reasons correctly.

Key checks include:

* Does the conclusion follow from the data?
* Are counterarguments included?
* Are uncertainty and risk handled well?
* Are causal claims stated with care?
* Are model outliers used correctly?

### Purpose

This test checks the thinking quality of the report.

### Common Deductions

* **Invalid inference:** A conclusion does not follow from the evidence.
* **Missing counterargument:** A major opposing case is not discussed.
* **Unjustified certainty:** The report sounds too sure.
* **Causal overreach:** A relationship is stated as certain when it is only possible.
* **Scope leap:** A claim uses evidence outside the forecast window.

***

## W3-B. Synthesis & Interlinking

### What Is Checked

This section checks whether the report connects separate signals well.

For market reports, key links often include:

* TNX and equities
* VIX and risk appetite
* QQQ and rate sensitivity
* AAPL and supply-chain risk
* Event risk and volatility
* ML divergence and risk sizing

### Purpose

Markets are connected. This test checks whether the report explains those links.

### Common Deductions

* Missing cross-asset links
* Weak triangulation
* Conceptual model gap
* Transferability confusion
* Unclear link between event risk and forecasts

***

## W3-C. Coherence, Completeness, Consistency

### What Is Checked

This section checks whether the report is internally stable.

Important checks include:

* Are all required sections present?
* Do executive forecasts match final forecasts?
* Do bias labels match exact forecasts?
* Are definitions used consistently?
* Are ranges built in the same way?
* Are dates inside the forecast window?

### Purpose

This test checks whether the report holds together as one object.

### Common Deductions

* Schema omission
* Numeric inconsistency
* Inconsistent definitions
* Traceability gap
* Temporal logic failure
* Range-definition inconsistency

***

## W3-D. Communication

### What Is Checked

This section checks whether the report is clear and useful.

Key checks include:

* Is the structure easy to follow?
* Are tables readable?
* Are labels clear?
* Is precision reasonable?
* Is guidance tied to evidence?
* Are limits stated?

### Purpose

A report can contain good analysis but still fail if the structure is confusing.

### Common Deductions

* Structure jump
* Broken table
* False precision
* Detached decision guidance
* Missing limitation statement
* Objective narration violation

***

## W3B. Final Model Scorecard

### What Is Checked

The Final Model Scorecard gives the main score summary.

It usually shows:

* Weighted total score
* Reasoning score
* Synthesis score
* Coherence score
* Communication score

### Purpose

This table makes ranking simple and transparent.

### Example Format

| Report | Total /100 | Reasoning /35 | Synthesis /25 | Coherence /25 | Communication /15 |
| ------ | ---------: | ------------: | ------------: | ------------: | ----------------: |
| R3     |      90.00 |         30.50 |         23.50 |         22.00 |             14.00 |

### Common Failure Types

This section usually records results rather than creates new failures.

However, score mismatches must be corrected if labels are wrong.

***

## W3D. Section Error Summary

### What Is Checked

This test groups errors by score category.

Each report receives a short list of errors in:

* A: Reasoning
* B: Synthesis
* C: Coherence
* D: Communication

### Purpose

This summary shows why a report lost points.

It helps distinguish a report with one major flaw from a report with many small flaws.

### Common Error Groups

* Reasoning errors
* Cross-asset gaps
* Schema failures
* Table and structure issues
* Numeric contradictions
* Weak source handling

***

## W4. Issue Log

### What Is Checked

The Issue Log records specific defects.

Each issue usually includes:

* Issue ID
* Report ID
* Severity
* Category
* Description
* Impact
* Evidence pointer

### Severity Scale

A simple severity scale can be used:

* **S1:** Minor issue
* **S2:** Moderate issue
* **S3:** Serious issue
* **S4:** Major or critical issue

### Purpose

The Issue Log makes errors auditable.

Instead of saying “the report is weak,” the log shows exactly where and why.

### Common Issue Categories

* Schema omission
* Numeric inconsistency
* Invalid inference
* Traceability gap
* Temporal logic failure
* Inconsistent definitions
* False precision
* Causal overreach
* Structure jump

***

## W5. Canonical Claim List

### What Is Checked

The Canonical Claim List defines the standard claims used for comparison.

For example:

* SPX Day+3 bias
* DJI regime
* QQQ range width
* VIX confidence
* TNX direction
* AAPL bias
* Cross-asset risk claims

### Purpose

This creates a common claim set for all reports.

Without a shared list, each report might be judged on different topics.

### Typical Claim Families

#### Ticker-Level Claims

For each ticker:

* Bias
* Regime
* Range width
* Confidence

#### Cross-Asset Claims

Examples:

* VIX upside creates equity risk.
* TNX up-yields increase QQQ and AAPL rate sensitivity.
* Event risk is integrated.
* TDA should limit conviction.
* ML divergence should trigger risk control.

***

## W6. Cross-Report Claim Matrix

### What Is Checked

The Cross-Report Claim Matrix compares each report against each canonical claim.

Entries may include:

* Agrees
* Disagrees
* Partially agrees
* Mixed
* Not addressed

### Purpose

This test finds where reports agree and where they diverge.

It also reveals whether one report is an outlier.

### Example

| Canonical Claim    | R1     | R2     | R3     |
| ------------------ | ------ | ------ | ------ |
| VIX bias is Higher | agrees | agrees | agrees |
| DJI bias           | Higher | Lower  | Higher |
| AAPL bias          | Higher | Lower  | Lower  |

### Common Findings

* Strong shared conclusions
* Main contradiction zones
* Weak or missing claims
* Report-specific deviations

***

## W7. Contradiction Matrix

### What Is Checked

The Contradiction Matrix records conflicts between reports or within a report.

Each contradiction usually includes:

* ID
* Claim area
* Reports involved
* Type
* Conflict
* Impact
* Resolution

### Contradiction Types

#### Type A: Direct Claim Conflict

Two reports state different outcomes.

Example:

* R1 says DJI Higher.
* R2 says DJI Lower.

#### Type B: Method Conflict

Two reports use different rules or methods.

Example:

* One report uses interquartile range.
* Another uses full min/max range.

#### Type C: Scope or Timing Conflict

A report uses evidence outside the forecast window.

Example:

* A June event is used for a May 20–22 forecast.

### Purpose

This test identifies the most important disagreements and chooses the more reliable side.

### Resolution Rules

A preferred report or claim should be chosen based on:

* Better numeric logic
* Better evidence support
* Better schema completeness
* Better source traceability
* Fewer internal contradictions

***

## W8. Final Ranking

### What Is Checked

The Final Ranking orders reports from strongest to weakest.

The ranking is based mainly on:

* Total score
* Severity of errors
* Completeness
* Internal consistency
* Traceability
* Decision usefulness

### Purpose

This gives a final, simple outcome.

### Ranking Logic

A report with a lower score can sometimes still contain useful parts.  
However, the final rank reflects total reliability.

### Common Placement Drivers

* Strong terminal QA improves rank.
* Incomplete delivery lowers rank.
* Major numeric contradictions lower rank.
* Strong traceability improves rank.
* Temporal logic failure can sharply lower rank.

***

## W9. Strengths Table

### What Is Checked

This table lists the strongest parts of each report.

Strengths may include:

* Full ticker coverage
* Strong cross-asset framing
* Clear executive table
* Good ML notes
* Strong self-audit
* Useful risk triggers
* Complete final forecasts

### Purpose

This prevents the review from focusing only on errors.

A weak report may still have useful sections.

### Good Strength Statements

Strong statements should be specific.

Weak form:

* “Good report.”

Better form:

* “Full six-ticker coverage is present, with a final forecast table and cross-asset TNX/VIX framing.”

***

## W10. Weaknesses Table

### What Is Checked

This table lists the main weaknesses of each report.

Weaknesses may include:

* Incomplete sections
* Bias conflicts
* Broken references
* Weak event support
* Numeric errors
* False precision
* Table formatting issues

### Purpose

This gives a quick view of report risk.

### Good Weakness Statements

Weak form:

* “Bad logic.”

Better form:

* “VIX is labeled Higher while the exact forecast is below current, creating a direct bias-exact conflict.”

***

## W11. Plain-Language Conclusions

### What Is Checked

This section converts technical findings into simple conclusions.

### Purpose

This makes the evaluation easy to understand.

### Good Plain-Language Output

Example:

* “R3 is the strongest report because it is complete, clear, and well audited.”
* “R2 ranks low because it stops early and misses required sections.”

### Common Failure

A conclusion becomes weak when it is vague or not tied to earlier evidence.

***

## W12. Executive Contradiction Brief

### What Is Checked

This section explains the biggest contradictions in a short form.

It focuses on high-impact conflicts, such as:

* DJI bias conflict
* VIX bias-exact conflict
* Range construction conflict
* Temporal logic conflict
* Missing final table conflict

### Purpose

This gives senior readers the key risks quickly.

### Required Features

A good brief should include:

* The contradiction
* Why it matters
* Which side is preferred
* Why that side is preferred

***

## W13. Reasoning Hierarchy Summary

### What Is Checked

This section describes how the report seems to reason.

A strong hierarchy may look like this:

1. Ground truth
2. Sentiment band
3. Range builder
4. Bias gate
5. Conflict flag
6. Risk management
7. Final forecast

A weak hierarchy may look like this:

1. Partial data
2. Unsupported calculation
3. Incomplete report
4. Unresolved claims

### Purpose

This test shows whether the report follows a stable decision path.

### Common Findings

* Strong reports use a clean reasoning chain.
* Weak reports jump between ideas.
* Some reports use bias labels without clear gates.
* Some reports rely too much on one model tail.

***

## W14. Super-Truth Synthesis

### What Is Checked

This section combines the most reliable conclusions across reports.

It gives a “best supported” view after contradictions are resolved.

### Purpose

The goal is not to average all reports.  
The goal is to extract the most reliable shared conclusions.

### Typical Super-Truth Objects

Examples:

* VIX risk is elevated.
* QQQ is defensive.
* SPX is fragile.
* TNX is a key equity constraint.
* DJI is a major contradiction.
* AAPL is cautious.
* ML divergence should reduce conviction.

### Rule

Consensus is useful, but clean logic matters more than vote count.

If three weak claims agree but one strong claim proves a rule conflict, the strong claim may be preferred.

***

## W15. Trace Appendix

### What Is Checked

The Trace Appendix lists the key evidence pointers used in the evaluation.

A pointer may include:

* Report ID
* Section
* Span
* Quote
* Source file

### Purpose

This allows another evaluator to find the evidence.

### Good Trace Entry

A strong trace entry points to a precise part of the report.

Example:

```text
[R3 | Sec="Executive Summary" | Span=520:2290 | Quote="SPX 7,353.61 6681 7501 7091 Lower"]
```

### Common Failure Types

* Missing span
* Broken source link
* Quote too vague
* Pointer not tied to a claim
* Placeholder reference only

***

# 5. Phase 0 Validation Tests

Phase 0 checks whether the report can be evaluated at all.

## 5.1 Schema Version Check

### What Is Checked

The report should match the required evaluation format.

### Purpose

This confirms that the right framework version is being used.

***

## 5.2 Required Ticker Check

### What Is Checked

The six required tickers are checked:

* SPX
* DJI
* QQQ
* VIX
* TNX
* AAPL

### Purpose

A market forecast report is incomplete if required tickers are missing.

***

## 5.3 Forecast Table Check

### What Is Checked

The report should include forecast ranges, exact forecasts, and bias labels.

### Purpose

This confirms that the report gives usable outputs.

***

## 5.4 Indicator Table Check

### What Is Checked

Technical indicator tables should be present when required.

Typical rows may include:

* Pivot levels
* Moving averages
* RSI
* Stochastic
* ATR
* ADX
* ROC
* BullBear

### Purpose

This checks whether the technical layer exists.

***

## 5.5 Event Calendar Check

### What Is Checked

The report should list relevant events and their timing.

### Purpose

Forecasts often depend on events. Event timing must be visible and within scope.

***

## 5.6 Reference Check

### What Is Checked

References should be resolvable and tied to claims.

### Purpose

This supports auditability.

Placeholder links or empty links reduce confidence.

***

## 5.7 Validation Result

Possible outcomes include:

* **PASSED**
* **PASSED\_WITH\_ISSUES**
* **FAILED**

### Purpose

This result shows whether the report is fit for full scoring.

***

# 6. Stress Tests

Stress tests are deeper checks used when a report appears complete but may still be unstable.

## T1. Premise Check

### What Is Checked

This test asks whether the report’s starting facts are valid.

Examples:

* Are event dates correct?
* Are current values correct?
* Are official sources shown?
* Are reference links usable?

### Purpose

Bad premises can break the whole report.

### Common Failure

A report uses event claims without clear source support.

***

## T2. Hidden Assumption Hunt

### What Is Checked

This test searches for assumptions that are used but not declared.

Examples:

* Range builder method is not explained.
* Sentiment is treated as dominant without a rule.
* A model tail is used as base case without justification.
* TDA signal is applied across tickers without ticker-level proof.

### Purpose

Hidden assumptions reduce trust.

A good report states its assumptions clearly.

***

## T3. Alternative Explanation Test

### What Is Checked

This test checks whether the report includes opposing explanations.

Examples:

* TNX can rise from inflation fear.
* TNX can fall from safe-haven demand.
* VIX can rise from event risk.
* VIX can fall from mean reversion.
* QQQ can fall from rate pressure.
* QQQ can rise from risk appetite.

### Purpose

Forecasts are stronger when reasonable alternatives are considered.

### Common Failure

Only the main thesis is discussed.

***

## T4. Confounder / Selection Bias Test

### What Is Checked

This test checks whether one unusual input is given too much power.

Examples:

* LSTM tail dominates SPX.
* A wide model outlier controls QQQ.
* One event headline drives all tickers.
* A single technical indicator overrides the full setup.

### Purpose

This protects the report from biased evidence selection.

***

## T5. Temporal Logic Test

### What Is Checked

This test checks whether all evidence fits the forecast window.

For a 3-day forecast, near-term events matter most.

### Purpose

This prevents long-term catalysts from being used as short-term proof.

### Common Failure

A June catalyst is used to support a May 20–22 forecast.

***

## T6. Sensitivity Test

### What Is Checked

This test checks whether the report explains what could change the forecast.

Examples:

* A close above pivot changes bias.
* TNX breakout changes QQQ risk.
* VIX spike lowers equity conviction.
* AAPL below support increases downside risk.

### Purpose

Forecasts should not be static.  
A good report explains trigger points.

***

## T7. Scope Integrity Test

### What Is Checked

This test checks whether each section contains the right type of content.

Examples:

* SPX visual section should focus on SPX visual logic.
* Cross-asset themes should not be buried inside one ticker table.
* Event discussion should not replace forecast logic.
* References should not act as analysis.

### Purpose

This keeps the report organized and easy to audit.

***

## T8. Consistency Scan

### What Is Checked

This test scans for internal contradictions.

Examples:

* Bias says Higher, exact is lower.
* Table says Above, number is below.
* Executive summary differs from final table.
* TDA label changes without explanation.
* Range method changes across tickers.

### Purpose

This is one of the most important tests.

A report may be complete but still unreliable if its own parts disagree.

***

# 7. Key Error Categories

## 7.1 Invalid Inference

### Meaning

The conclusion does not follow from the evidence.

### Example

A report says DJI is Lower even though the forecast exact and range are above current, with no clear override rule.

### Purpose of Detection

This protects against wrong logic.

***

## 7.2 Numeric Inconsistency

### Meaning

Numbers conflict with labels, formulas, or conclusions.

### Example

A table says “Above” while the value is below the comparison level.

### Purpose of Detection

This protects against arithmetic and comparison errors.

***

## 7.3 Schema Omission

### Meaning

A required section or table is missing.

### Example

A report stops after DJI and omits SPX, QQQ, VIX, and AAPL sections.

### Purpose of Detection

This protects completeness.

***

## 7.4 Traceability Gap

### Meaning

A claim has weak or missing evidence support.

### Example

References are listed, but links are empty placeholders.

### Scope (HARD)

Reports are graded only against the citation rules that 28\_QUERY itself imposes
(local \[^n] footnotes; issuer-first sourcing; resolved footnote list). The
EvidencePointer format binds the evaluator's own claims, never the reports.
"Citations are citation-style rather than EvidencePointer" is NOT a deductible
finding.

### Grading Contract (no deduction without a mapped generator requirement)

Every deduction category must test an explicit requirement of 28\_QUERY. If a
candidate finding cannot be mapped to a row below, it is not chargeable:

| Deduction category | 28\_QUERY requirement it tests |
|---|---|
| traceability\_gap | Local \[^n] footnotes on event rows and externally sourced claims; footnote list resolved |
| numeric\_inconsistency | Range–Exact constraint; median+MAD divergence rule; user data primacy (AXIOM 0) |
| schema\_omission | AXIOM 1 global blocks (1)–(8) and per-ticker subsections (a)–(m) |
| inconsistent\_definitions | Deterministic definitions in AXIOM 2 / TDA Translation Rules |
| undeclared\_assumption | Derived metrics permitted only with stated formula (DERIVED\_METRIC flag) |
| structure\_jump | AXIOM 1 fixed section order; Stage 7 schema-order QA |
| false\_precision | Numeric formatting rules; confidence fields from Step 1 package |
| missing\_limitations | Required flags (BOUNDARY\_CONSTRAINED, RANGE\_CONSTRAINED\_BIAS, INDETERMINATE flip risk, etc.) |
| decision\_guidance\_detached | Risk Management subsection mapping to pivots + ATR/ADX posture |

### Purpose of Detection

This protects audit quality and keeps the evaluator aligned with the generator's
actual contract.

***

## 7.5 Inconsistent Definitions

### Meaning

The same term or method is used in different ways.

### Example

TDA is called DISTRIBUTED\_CYCLES in one section and NEUTRAL\_STRUCTURE in another without explanation.

### Purpose of Detection

This protects model clarity.

***

## 7.6 Temporal Logic Failure

### Meaning

Evidence falls outside the forecast window.

### Example

A June event is used as a direct driver for a May 3-day forecast.

### Purpose of Detection

This protects time discipline.

***

## 7.7 Causal Overreach

### Meaning

A possible relationship is stated as certain.

### Example

Oil shocks are said to “inevitably” raise volatility.

### Purpose of Detection

This protects uncertainty handling.

***

## 7.8 False Precision

### Meaning

Forecasts use exact numbers that appear too precise for the evidence.

### Example

A report gives exact decimal forecasts while the reasoning contains unresolved conflicts.

### Purpose of Detection

This protects decision users from overconfidence.

***

## 7.9 Missing Counterargument

### Meaning

A major opposing view is not discussed.

### Example

A severe QQQ downside forecast is given without a nearby upside or stabilization case.

### Purpose of Detection

This protects balance.

***

## 7.10 Structure Jump

### Meaning

Content appears in the wrong section.

### Example

Cross-asset theme text appears inside an SPX visual table.

### Purpose of Detection

This protects readability and traceability.

***

# 8. Forecast-Specific Benchmarks

## 8.1 Bias Gate Test

### What Is Checked

The bias label must match the exact forecast or a stated override rule.

### Basic Rule

* Exact above current → Higher
* Exact below current → Lower
* Exact near current → Flat or Mixed

### Exception

A report may override this rule only if the override is explicit and justified.

### Purpose

This keeps directional calls consistent.

***

## 8.2 Range Builder Test

### What Is Checked

Forecast ranges should be built by a consistent method.

Possible methods include:

* Interquartile range
* Point-forecast cluster
* Model consensus band
* Approved risk-adjusted range

### Failure Example

A report uses full min/max model extremes for one ticker and narrow range-builder output for another without explanation.

### Purpose

This keeps range width meaningful.

***

## 8.3 ML Divergence Test

### What Is Checked

Model forecasts are checked for spread and outliers.

### Strong Handling

A strong report:

* Identifies outliers
* Explains the method
* Reduces conviction when models diverge
* Avoids letting one tail dominate the base case

### Purpose

This prevents model noise from becoming false certainty.

***

## 8.4 Sentiment Alignment Test

### What Is Checked

Forecasts should align with the sentiment package unless a clear reason is given.

### Example

If sentiment is cautious, a strong bullish bias needs extra support.

### Purpose

This checks whether the forecast respects the supplied sentiment backbone.

***

## 8.5 Event Integration Test

### What Is Checked

Events must be:

* Timely
* Relevant
* Source-supported
* Properly weighted
* Not overused

### Purpose

This prevents event lists from becoming unsupported forecast drivers.

***

## 8.6 TDA Discipline Test

### What Is Checked

TDA labels should be used consistently and with proper limits.

### Common TDA Concepts

* H1\_NONE
* DISTRIBUTED\_CYCLES
* NEUTRAL\_STRUCTURE
* Flip risk
* Persistence

### Purpose

This prevents topology terms from adding false confidence.

***

# 9. Scoring Method

## 9.1 Base Point Structure

The total score is 100.

| Section                              | Max Points | Purpose                                |
| ------------------------------------ | ---------: | -------------------------------------- |
| Reasoning Quality                    |         35 | Tests logic and inference              |
| Synthesis & Interlinking             |         25 | Tests cross-signal integration         |
| Coherence, Completeness, Consistency |         25 | Tests structure and internal stability |
| Communication                        |         15 | Tests clarity and usefulness           |

***

## 9.2 Deduction Logic

Points are deducted for errors.

Larger errors receive larger deductions.

Examples:

* Minor wording issue: small deduction
* Broken table: small to medium deduction
* Missing ticker section: large deduction
* False numeric comparison: large deduction
* Incomplete report: very large deduction

***

## 9.3 Score Floor Rule

Some evaluations use a floor rule:

```text
section_score = MAX(section_max - deductions, 0.2 × section_max)
```

### Meaning

A section cannot fall below 20% of its maximum score.

### Purpose

This prevents one category from becoming negative or mathematically distorted.

***

## 9.4 Grade Bands

A simple grade system may be used:

| Score Range | Grade Meaning |
| ----------: | ------------- |
|      90–100 | Exceptional   |
|       80–89 | Strong        |
|       70–79 | Adequate      |
|       60–69 | Weak          |
|       50–59 | Poor          |
|    Below 50 | Failing       |

### Purpose

The grade band makes the score easier to read.

***

# 10. Ranking Method

## 10.1 Primary Ranking Rule

Reports are ranked by total score.

### Purpose

This gives a clear final order.

***

## 10.2 Tie-Breakers

If scores are close, these tie-breakers can be used:

1. Fewer critical issues
2. Better completeness
3. Better bias-exact consistency
4. Better traceability
5. Better final forecast table
6. Better handling of contradictions
7. Better terminal QA

### Purpose

This avoids unfair ranking when scores are similar.

***

## 10.3 Red-Flag Overrides

A report may be pushed lower if it has a major red flag.

Examples:

* Report is incomplete
* Final forecast table is missing
* Temporal window is broken
* Bias labels repeatedly conflict with exact forecasts
* Source links are unusable
* Major numeric inequality is wrong

### Purpose

This protects the final ranking from being distorted by surface detail.

***

# 11. Beginner-Friendly Evaluation Workflow

## Step 1: Confirm Structure

Check whether all required sections exist.

If sections are missing, mark schema omissions.

***

## Step 2: Extract Main Forecasts

Record for each ticker:

* Current value
* Forecast range
* Exact forecast
* Bias
* Confidence
* Regime

***

## Step 3: Test Bias Against Exact Forecast

Compare current value with exact forecast.

Mark conflicts.

***

## Step 4: Check Range Logic

Ask whether the range looks narrow, medium, or wide.

Check whether the same method is used across tickers.

***

## Step 5: Review Evidence

For each major claim, find supporting text.

If support is missing, mark a traceability gap.

***

## Step 6: Review Reasoning

Ask whether the claim follows from the evidence.

If not, mark invalid inference.

***

## Step 7: Check Cross-Asset Links

Look for links between:

* TNX and equities
* VIX and risk appetite
* QQQ/AAPL and rates
* Events and forecast changes

***

## Step 8: Check Time Window

Make sure event evidence fits the forecast horizon.

Flag future or medium-term events if used as short-term proof.

***

## Step 9: Build Issue Log

Record each major flaw with:

* Category
* Severity
* Impact
* Evidence pointer

***

## Step 10: Score the Report

Apply deductions across the four score categories.

***

## Step 11: Compare Claims Across Reports

Use the canonical claim matrix.

Find agreement, disagreement, and partial agreement.

***

## Step 12: Resolve Contradictions

Choose the stronger claim based on evidence and logic.

***

## Step 13: Rank Reports

Use total scores and red-flag checks.

***

## Step 14: Write Final Conclusions

Include:

* Final ranking
* Key weaknesses
* Major contradictions
* Best-supported synthesis

***

# 12. Quality Checklist

A final evaluation should pass these checks:

* Report map exists.
* CER Ledger exists.
* Scorecard exists.
* Issue Log exists.
* Canonical claims are listed.
* Cross-report matrix exists.
* Contradictions are resolved.
* Final ranking is clear.
* Strengths and weaknesses are stated.
* Plain-language conclusions are included.
* Trace appendix is present.
* Evidence pointers are well formed.
* No chart-absence penalty is applied when neutrality is required.
* Major numeric claims are sanity-checked.
* Bias and exact forecast labels are checked.
* Forecast-window discipline is checked.

***

# 13. Best-Practice Rules for Evaluators

## Rule 1: Favor Clear Logic Over Length

A short but complete report can beat a long unstable report.

***

## Rule 2: Treat Contradictions as High Risk

A report that says two different things needs correction before decision use.

***

## Rule 3: Do Not Reward Unsupported Precision

Exact values should not imply confidence when reasoning is weak.

***

## Rule 4: Keep Time Windows Strict

Only use near-term catalysts for near-term forecasts unless the report clearly labels background context.

***

## Rule 5: Separate Evidence From Interpretation

A fact, a model output, and a conclusion are different objects.

***

## Rule 6: Require Local Proof

A reference list is not enough. A claim should be tied to a specific section, span, or quote.

***

## Rule 7: Discount Incomplete Reports

Missing ticker sections or final forecasts should lower rank sharply.

***

## Rule 8: Prefer Reports That Self-Audit and Resolve Issues

A conflict flag is useful.  
A resolved conflict is better.

***

## Rule 9: Penalize Broken Math

Wrong comparisons and bad inequality logic reduce trust in the full report.

***

## Rule 10: Use Super-Truth Carefully

Consensus matters, but clean reasoning matters more.

***

# 14. Final Framework Summary

The Axiom Evaluation Framework v3.0 is a full audit system for market forecast reports.

It tests five main qualities:

1. **Completeness**  
   Required sections and tickers must be present.

2. **Reasoning quality**  
   Conclusions must follow from evidence.

3. **Consistency**  
   Bias labels, exact forecasts, ranges, and final tables must agree.

4. **Traceability**  
   Claims must point to usable evidence.

5. **Decision usefulness**  
   The report must be clear, balanced, and honest about risk.

The strongest reports are not just detailed. They are complete, consistent, well sourced, and careful with uncertainty.
