# Single-Report Logic Evaluation — R7

## Evaluation Scope

**R7:** `69 Qwen3.7 Plus.pdf` was evaluated using the same Axiom Evaluation Framework v3.0, adjusted from three-report comparison to a single-report audit. Cross-report ranking was not applicable. Internal reasoning quality, schema adherence, deterministic compliance, traceability, contradiction handling, and decision usefulness were evaluated. [\[69 Qwen3.7 Plus \| PDF\]](https://mynek-my.sharepoint.com/personal/rdolovcak_nek_si/Documents/Microsoft%20Copilot%20Chat%20Files/69%20Qwen3.7%20Plus.pdf)

***

# W1. Report Map

| Report | Main Structure Detected                                                                                                                                                                                                                                                                                      | Coverage Result                                                                                                                                        | Key EvidencePointer |                         |            |                                    |
| ------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------- | ----------------------- | ---------- | ---------------------------------- |
| R7     | Header, Executive Summary, Market Environment, Cross-Asset Themes, Scenario Analysis, per-ticker sections, technical tables, ARIMAX notes, ML notes, sentiment blocks, event tables, commodity correlation limitations, risk management, summary tables, discrepancy notes, final forecast table, references | Broad coverage. Required sections are mostly present. Ticker order is non-compliant in the Executive Summary because TNX appears first instead of SPX. | \`\[R7              | Sec="Executive Summary" | Span=0:220 | Quote="TNX 4.493 4.4577–4.4929"]\` |

***

# W2. CER Ledger

| ClaimID | ClaimText                                               | Type        | Modality         | Status   | Evidence                                                                 | ReasoningLink                                           | Assumptions                                          | EvidencePointer |                             |               |                                                                    |
| ------- | ------------------------------------------------------- | ----------- | ---------------- | -------- | ------------------------------------------------------------------------ | ------------------------------------------------------- | ---------------------------------------------------- | --------------- | --------------------------- | ------------- | ------------------------------------------------------------------ |
| R7-C01  | TNX bias is Lower.                                      | predictive  | TEXT\_VERIFIABLE | ASSERTED | Executive table states Lower.                                            | Bearish fractal and safe-haven demand are cited.        | TNX direction is yield direction.                    | \`\[R7          | Sec="Executive Summary"     | Span=0:160    | Quote="TNX 4.493 ... Lower Yields retreating"]\`                   |
| R7-C02  | DJI bias is Lower.                                      | predictive  | TEXT\_VERIFIABLE | ASSERTED | Executive table states Lower.                                            | Bearish Williams and regime override reduce confidence. | Bias gate is valid.                                  | \`\[R7          | Sec="Executive Summary"     | Span=161:320  | Quote="DJI 51,666.84 ... Lower Consolidating"]\`                   |
| R7-C03  | SPX bias is Higher in the Executive Summary.            | predictive  | TEXT\_VERIFIABLE | ASSERTED | Executive table states Higher.                                           | Exact is above current and Williams fractal is bullish. | Sentiment placement is valid.                        | \`\[R7          | Sec="Executive Summary"     | Span=321:480  | Quote="SPX 7365 ... 7415 Higher Advancing"]\`                      |
| R7-C04  | VIX bias is Lower.                                      | predictive  | TEXT\_VERIFIABLE | ASSERTED | Executive table states Lower.                                            | Mean-reverting regime is cited.                         | VIX structure dominates.                             | \`\[R7          | Sec="Executive Summary"     | Span=481:640  | Quote="VIX 19.49 ... 18.10 Lower"]\`                               |
| R7-C05  | QQQ bias is Higher.                                     | predictive  | TEXT\_VERIFIABLE | ASSERTED | Executive table states Higher.                                           | Bullish fractal and AI rebound potential are cited.     | QQQ range is valid.                                  | \`\[R7          | Sec="Executive Summary"     | Span=641:800  | Quote="QQQ 714 ... 719.50 Higher"]\`                               |
| R7-C06  | AAPL bias is Higher with conflict.                      | predictive  | TEXT\_VERIFIABLE | ASSERTED | Bias-positioning conflict is stated.                                     | Exact is above current while sentiment is bearish.      | Level 2 numerical logic controls bias.               | \`\[R7          | Sec="Executive Summary"     | Span=801:1000 | Quote="BIAS\_POSITIONING\_CONFLICT: Bias determined as Higher"]\`  |
| R7-C07  | Structural health is unstable.                          | descriptive | TEXT\_VERIFIABLE | ASSERTED | All tickers show recent regime changes.                                  | Regime-change breadth reduces conviction.               | Structural context is accepted.                      | \`\[R7          | Sec="Cross-Asset Themes"    | Span=0:180    | Quote="broad structural layer is unstable rather than cleanly"]\`  |
| R7-C08  | VIX has the strongest structural consistency.           | descriptive | TEXT\_VERIFIABLE | ASSERTED | MEAN\_REVERT, DOWN Trend10D, and bearish fractal are cited.              | Multiple structural signals point lower.                | VIX data is valid.                                   | \`\[R7          | Sec="Cross-Asset Themes"    | Span=181:360  | Quote="VIX has a MEAN\_REVERT Hurst regime"]\`                     |
| R7-C09  | Scenario probabilities sum to 100.                      | descriptive | TEXT\_VERIFIABLE | ASSERTED | Scenario table lists 45, 35, and 20.                                     | Scenario weights are additive.                          | No hidden scenario is added.                         | \`\[R7          | Sec="Scenario Analysis"     | Span=0:220    | Quote="Base Case ... 45 ... Risk-Off Extension"]\`                 |
| R7-C10  | SPX has DYNAMIX outliers.                               | descriptive | TEXT\_VERIFIABLE | ASSERTED | ML note flags DYNAMIX values.                                            | Outliers create dispersion risk.                        | Median/MAD calculation is accepted as report output. | \`\[R7          | Sec="SPX ML"                | Span=0:220    | Quote="DYNAMIX models are outliers 7153.91"]\`                     |
| R7-C11  | QQQ has Torch and DYNAMIX outliers.                     | descriptive | TEXT\_VERIFIABLE | ASSERTED | ML note flags Torch and DYNAMIX.                                         | Outliers justify wait-for-close risk control.           | MAD rule is accepted.                                | \`\[R7          | Sec="QQQ ML"                | Span=0:220    | Quote="Torch ... and DYNAMIX ... models are outliers"]\`           |
| R7-C12  | VIX has a Torch outlier.                                | descriptive | TEXT\_VERIFIABLE | ASSERTED | ML note flags Torch 16.40.                                               | Outlier creates lower-tail volatility dispersion.       | MAD rule is accepted.                                | \`\[R7          | Sec="VIX ML"                | Span=0:180    | Quote="Torch model 16.40 is an outlier"]\`                         |
| R7-C13  | TNX has an ARIMAX outlier.                              | descriptive | TEXT\_VERIFIABLE | ASSERTED | ML note flags ARIMAX 4.4452.                                             | ARIMAX sits below cluster.                              | MAD rule is accepted.                                | \`\[R7          | Sec="TNX ML"                | Span=0:180    | Quote="ARIMAX model 4.4452 is an outlier"]\`                       |
| R7-C14  | AAPL has a DYNAMIX outlier.                             | descriptive | TEXT\_VERIFIABLE | ASSERTED | ML note flags DYNAMIX 291.24.                                            | Low DYNAMIX forecast drives downside tail.              | MAD rule is accepted.                                | \`\[R7          | Sec="AAPL ML"               | Span=0:180    | Quote="DYNAMIX model 291.24 is an outlier"]\`                      |
| R7-C15  | Commodity correlations are not computed.                | descriptive | TEXT\_VERIFIABLE | ASSERTED | Each commodity block states 28-day rolling correlation was not computed. | Missing r/p prevents deterministic correlation.         | No recomputation is allowed.                         | \`\[R7          | Sec="Commodity Correlation" | Span=0:120    | Quote="28-day rolling correlation not computed in this context"]\` |
| R7-C16  | TDA is used as NEUTRAL\_STRUCTURE with LOW flip risk.   | descriptive | TEXT\_VERIFIABLE | ASSERTED | Risk sections state NEUTRAL\_STRUCTURE and LOW flip risk.                | TDA is treated as usable but weak.                      | TDA sequence support is sufficient.                  | \`\[R7          | Sec="Risk Management"       | Span=0:180    | Quote="TDA analysis reveals NEUTRAL\_STRUCTURE"]\`                 |
| R7-C17  | Final forecast table repeats executive forecasts.       | descriptive | TEXT\_VERIFIABLE | ASSERTED | Final table lists the same six ticker forecasts.                         | Closure block is present.                               | Final table is consistent.                           | \`\[R7          | Sec="Final Forecasts"       | Span=0:220    | Quote="Final Three-Day Forecasts Table SPX 7388"]\`                |
| R7-C18  | References are present but link placeholders are empty. | descriptive | TEXT\_VERIFIABLE | ASSERTED | References list publishers and empty back-links.                         | Trace depth is weaker than framework format.            | Extracted link placeholders reflect document.        | \`\[R7          | Sec="References"            | Span=0:220    | Quote="Federal Reserve Board — Federal Reserve issues"]\`          |

R7 shows broad schema coverage, strong ticker-level detail, and explicit bias-conflict handling for AAPL. It also shows traceability weaknesses because references are mostly placeholder links rather than EvidencePointer-style evidence. [\[69 Qwen3.7 Plus \| PDF\]](https://mynek-my.sharepoint.com/personal/rdolovcak_nek_si/Documents/Microsoft%20Copilot%20Chat%20Files/69%20Qwen3.7%20Plus.pdf)

***

# W3. Detailed Scorecard

| Section                                 |     Max | Main Deductions                                                                                                                                                                                      |    Score | Grade      |
| --------------------------------------- | ------: | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------: | ---------- |
| A. Reasoning Quality                    |      35 | SPX bias is coherent, but ticker ordering and some TDA flip-risk claims reduce rigor; one missing counterargument for TDA LOW flip risk; one mild invalid inference around “mean-reversion dynamics” |     29.0 | Strong     |
| B. Synthesis & Interlinking             |      25 | Cross-asset themes are present; TNX/VIX/equity coupling is covered; some event and theme text is inserted awkwardly inside SPX visual section                                                        |     21.5 | Strong     |
| C. Coherence, Completeness, Consistency |      25 | Ticker order violation; traceability gaps; TDA LOW flip-risk overstatement; one internal conflict between Executive Summary ordering and required fixed order                                        |     17.5 | Adequate   |
| D. Communication                        |      15 | Detailed and readable, but formatting is noisy; tables are sometimes malformed by extraction; several citations are empty placeholders                                                               |     12.0 | Strong     |
| **Total**                               | **100** | —                                                                                                                                                                                                    | **80.0** | **Strong** |

**R7 judgment:** R7 qualifies as **Strong**. The report is detailed and covers nearly all required analytical blocks. The main weaknesses are deterministic schema ordering, placeholder traceability, and overconfident TDA flip-risk language. [\[69 Qwen3.7 Plus \| PDF\]](https://mynek-my.sharepoint.com/personal/rdolovcak_nek_si/Documents/Microsoft%20Copilot%20Chat%20Files/69%20Qwen3.7%20Plus.pdf)

***

# W3B. Final Model Scorecard Overview

| Model | Weighted Total /100 | Reasoning Quality /35 | Synthesis & Interlinking /25 | Coherence, Completeness, Consistency /25 | Communication /15 |
| ----- | ------------------: | --------------------: | ---------------------------: | ---------------------------------------: | ----------------: |
| R7    |                80.0 |                  29.0 |                         21.5 |                                     17.5 |              12.0 |

***

# W3D. Section Error Summary

| Report | A Errors                                                                         | B Errors                                             | C Errors                                                                           | D Errors                                                          |
| ------ | -------------------------------------------------------------------------------- | ---------------------------------------------------- | ---------------------------------------------------------------------------------- | ----------------------------------------------------------------- |
| R7     | missing\_counterargument; mild\_invalid\_inference; mild\_unjustified\_certainty | structure\_jump; partial\_cross-link embedding issue | schema\_order\_violation; traceability\_gap; undeclared\_TDA\_sequence\_assumption | formatting\_noise; citation\_placeholder\_issue; false\_precision |

***

# W4. Issue Log

| IssueID | Report | Severity | Category                 | Description                                                                                                                                | Impact                                         | EvidencePointer |                             |            |                                                                           |
| ------- | ------ | -------: | ------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------ | ---------------------------------------------- | --------------- | --------------------------- | ---------- | ------------------------------------------------------------------------- |
| I01     | R7     |       S3 | schema\_order\_violation | Executive Summary ticker order starts with TNX instead of the required SPX → DJI → QQQ → VIX → TNX → AAPL order.                           | Required workflow order is violated.           | \`\[R7          | Sec="Executive Summary"     | Span=0:220 | Quote="TNX 4.493 ... DJI ... SPX"]\`                                      |
| I02     | R7     |       S2 | traceability\_gap        | References use placeholder-style links and do not provide EvidencePointer format.                                                          | Audit depth is weakened.                       | \`\[R7          | Sec="References"            | Span=0:220 | Quote="Federal Reserve Board — Federal Reserve issues"]\`                 |
| I03     | R7     |       S2 | undeclared\_assumption   | TDA LOW flip risk is asserted, but sequence data needed for flip-risk computation is not shown in the report.                              | Regime-stability confidence may be overstated. | \`\[R7          | Sec="Risk Management"       | Span=0:180 | Quote="TDA regime stability assessment shows LOW flip risk"]\`            |
| I04     | R7     |       S2 | structure\_jump          | Cross-asset theme paragraphs appear inside the SPX visual section after the diagnostics table starts.                                      | Section logic is harder to audit.              | \`\[R7          | Sec="SPX Visual"            | Span=0:260 | Quote="Explanation: If PCE or Fed communication confirms"]\`              |
| I05     | R7     |       S1 | false\_precision         | Exact percentiles and model thresholds imply precision greater than short-horizon uncertainty supports.                                    | Communication risk only.                       | \`\[R7          | Sec="AAPL Rationale"        | Span=0:170 | Quote="Exact positioned conservatively at 15th percentile"]\`             |
| I06     | R7     |       S2 | missing\_counterargument | SPX Higher bias is accepted, but recent down momentum receives limited nearby counterargument treatment in the final summary.              | SPX confidence may be too smooth.              | \`\[R7          | Sec="SPX Summary"           | Span=0:180 | Quote="Higher ... bullish fractal conflicts with recent sharp selloff"]\` |
| I07     | R7     |       S1 | formatting\_noise        | Several extracted tables have merged headers and malformed cells.                                                                          | Readability is reduced.                        | \`\[R7          | Sec="Technical Indicators"  | Span=0:120 | Quote="Indicator Reading Interpretation Actionable Takeaway"]\`           |
| I08     | R7     |       S2 | methodological\_gap      | Commodity correlations are not computed, which is correctly limited, but no deterministic fallback beyond qualitative linkage is provided. | Cross-asset numerical depth is limited.        | \`\[R7          | Sec="Commodity Correlation" | Span=0:120 | Quote="28-day rolling correlation not computed"]\`                        |

***

# W5. Canonical Claim List

| ID  | Canonical Claim                                           | R7 Stance |
| --- | --------------------------------------------------------- | --------- |
| C01 | SPX bias is Higher.                                       | Agrees    |
| C02 | SPX regime is RANDOM.                                     | Agrees    |
| C03 | SPX confidence is Moderate.                               | Agrees    |
| C04 | SPX model dispersion is material.                         | Agrees    |
| C05 | DJI bias is Lower.                                        | Agrees    |
| C06 | DJI regime is RANDOM.                                     | Agrees    |
| C07 | DJI confidence is Low.                                    | Agrees    |
| C08 | DJI trend and fractal signals conflict.                   | Agrees    |
| C09 | QQQ bias is Higher.                                       | Agrees    |
| C10 | QQQ regime is RANDOM or recently mean-reverting.          | Agrees    |
| C11 | QQQ confidence is Low.                                    | Agrees    |
| C12 | QQQ semiconductor risk is material.                       | Agrees    |
| C13 | VIX bias is Lower.                                        | Agrees    |
| C14 | VIX regime is MEAN\_REVERT.                               | Agrees    |
| C15 | VIX event-risk floor remains active.                      | Agrees    |
| C16 | VIX confidence is Moderate.                               | Agrees    |
| C17 | TNX bias is Lower.                                        | Agrees    |
| C18 | TNX regime is RANDOM.                                     | Agrees    |
| C19 | TNX is constrained by inflation versus safe-haven demand. | Agrees    |
| C20 | TNX confidence is Moderate.                               | Agrees    |
| C21 | AAPL bias is conflicted.                                  | Agrees    |
| C22 | AAPL regime is RANDOM.                                    | Agrees    |
| C23 | AAPL memory-cost risk is material.                        | Agrees    |
| C24 | AAPL confidence is Moderate.                              | Agrees    |
| C25 | PCE is a key event.                                       | Agrees    |
| C26 | Micron is key for QQQ/SPX/AAPL.                           | Agrees    |
| C27 | Fed stress tests matter for DJI/SPX.                      | Agrees    |
| C28 | Commodity correlation is qualitative only.                | Agrees    |
| C29 | VIX and equities must be coupled.                         | Agrees    |
| C30 | TNX and QQQ/AAPL rate sensitivity must be coupled.        | Agrees    |

***

# W6. Single-Report Claim Alignment Matrix

A cross-report matrix is not applicable for a one-report audit. A single-report canonical alignment matrix was used instead.

| Canonical Claims Tested | Addressed | Partially Addressed | Not Addressed | Result                          |
| ----------------------: | --------: | ------------------: | ------------: | ------------------------------- |
|                      30 |        30 |                   0 |             0 | Complete single-report coverage |

R7 addresses all canonical claims through executive forecasts, ticker sections, cross-asset themes, event tables, commodity-correlation limitations, and risk-management sections. [\[69 Qwen3.7 Plus \| PDF\]](https://mynek-my.sharepoint.com/personal/rdolovcak_nek_si/Documents/Microsoft%20Copilot%20Chat%20Files/69%20Qwen3.7%20Plus.pdf)

***

# W7. Internal Contradiction Matrix

| ID  | Claim                 | Type                | Conflict                                                                                              | Impact | Resolution                                                                     |
| --- | --------------------- | ------------------- | ----------------------------------------------------------------------------------------------------- | -----: | ------------------------------------------------------------------------------ |
| X01 | Ticker order          | TEXT\_CONTRADICTION | Required fixed order is SPX → DJI → QQQ → VIX → TNX → AAPL, but R7 starts Executive Summary with TNX. |    4.0 | Schema penalty applied. Forecast logic remains usable.                         |
| X02 | TDA flip risk         | TEXT\_CONTRADICTION | R7 states LOW flip risk, but the required sequence inputs are not shown in the report.                |    2.0 | TDA structure is accepted as weak/neutral. LOW flip-risk claim is downgraded.  |
| X03 | SPX visual section    | TEXT\_CONTRADICTION | Cross-asset theme paragraphs appear inside SPX visual analysis.                                       |    2.0 | Structure-jump penalty applied. Content remains analytically relevant.         |
| X04 | AAPL bias             | MIXED\_SUPPORT      | AAPL is Higher by exact/current logic, but sentiment is bearish.                                      |    2.0 | Conflict is correctly flagged by R7. No major penalty applied.                 |
| X05 | Commodity correlation | TEXT\_CONTRADICTION | Commodity correlation is requested, but no r/p is computed.                                           |    1.5 | Limitation is valid because required data is absent. No major penalty applied. |

***

# W8. Final Ranking Summary

Only one report was evaluated in this phase.

\#1: **R7 — 80.0/100**

Key Insights:

* **Standalone grade:** Strong.
* **Most common error:** traceability and formatting weakness.
* **Most impactful issue:** ticker order schema violation.
* **Most important resolved contradiction:** AAPL Higher bias with bearish sentiment was properly flagged as `BIAS_POSITIONING_CONFLICT`.

***

# W9. Strengths Table

| Report | Strengths                                                                                                                                                                                                                                                                        |
| ------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| R7     | Full ticker coverage is present. Executive and final forecast tables are included. AAPL bias conflict is explicitly flagged. Outlier logic is applied across SPX, QQQ, VIX, TNX, and AAPL. Commodity correlation limitations are stated. Event-risk tables are broad and usable. |

***

# W10. Weaknesses Table

| Report | Weaknesses                                                                                                                                                                                                                                                                                                               |
| ------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| R7     | Executive Summary ticker order violates the fixed order. Evidence is not expressed in the required EvidencePointer format. TDA LOW flip-risk language is stronger than the shown sequence support. Some cross-asset material is inserted inside the SPX visual section. Formatting is noisy in several extracted tables. |

***

# W11. Plain-Language Conclusions

R7 is a strong report.  
Most forecast blocks are present.  
The AAPL conflict is handled well.  
The main weakness is schema discipline.  
Ticker order should have started with SPX.  
Traceability should be stronger and more local.  
TDA flip-risk wording should be more careful.

***

# W12. Executive Contradiction Brief

| Main Contradiction                                              | Materiality | Resolution                                      |
| --------------------------------------------------------------- | ----------: | ----------------------------------------------- |
| Executive ticker order violates required fixed order.           |        High | Schema penalty applied.                         |
| TDA LOW flip risk is asserted without visible sequence support. |      Medium | Claim downgraded to weak/neutral TDA structure. |
| AAPL Higher bias conflicts with bearish sentiment.              |      Medium | Properly flagged by R7; no major deduction.     |
| Cross-asset text appears inside SPX visual section.             |      Medium | Structure-jump penalty applied.                 |

***

# W13. Reasoning Hierarchy Summary

1. User-supplied values are mostly preserved.
2. Forecast ranges and exact values are internally consistent.
3. Sentiment and structural signals are used in ticker rationale.
4. AAPL bias conflict is acknowledged.
5. Event risk is integrated across major tickers.
6. Commodity-correlation gaps are limited rather than invented.
7. TDA structure is used, but flip-risk confidence is overstated.
8. Schema ordering and traceability reduce final score.

***

# W14. R7 Super-Truth Synthesis

| Ticker | R7 Bias               | Evaluated Confidence | Core Reason                                                                                 |
| ------ | --------------------- | -------------------- | ------------------------------------------------------------------------------------------- |
| SPX    | Higher                | Moderate             | Bullish Williams fractal supports rebound, but down momentum and fear cap conviction.       |
| DJI    | Lower                 | Low                  | Bearish fractal and stress-test risk offset defensive Dow behavior.                         |
| QQQ    | Higher                | Low                  | Bullish fractal and model cluster support rebound, but semiconductor risk remains dominant. |
| VIX    | Lower                 | Moderate             | Mean-reverting structure supports fade, but event-risk floor remains active.                |
| TNX    | Lower                 | Moderate             | Bearish fractal and safe-haven demand offset sticky inflation pressure.                     |
| AAPL   | Higher but conflicted | Moderate             | Exact is above current, but memory-cost pressure and bearish sentiment remain material.     |

***

# W15. Trace Appendix

| EvidencePointer | Source                   |               |                                                                   |    |
| --------------- | ------------------------ | ------------- | ----------------------------------------------------------------- | -- |
| \`\[R7          | Sec="Executive Summary"  | Span=0:160    | Quote="TNX 4.493 ... Lower Yields retreating"]\`                  | R7 |
| \`\[R7          | Sec="Executive Summary"  | Span=321:480  | Quote="SPX 7365 ... 7415 Higher Advancing"]\`                     | R7 |
| \`\[R7          | Sec="Executive Summary"  | Span=801:1000 | Quote="BIAS\_POSITIONING\_CONFLICT: Bias determined as Higher"]\` | R7 |
| \`\[R7          | Sec="Cross-Asset Themes" | Span=0:180    | Quote="broad structural layer is unstable rather than cleanly"]\` | R7 |
| \`\[R7          | Sec="Scenario Analysis"  | Span=0:220    | Quote="Base Case ... 45 ... Risk-Off Extension"]\`                | R7 |
| \`\[R7          | Sec="SPX ML"             | Span=0:220    | Quote="DYNAMIX models are outliers 7153.91"]\`                    | R7 |
| \`\[R7          | Sec="QQQ ML"             | Span=0:220    | Quote="Torch ... and DYNAMIX ... models are outliers"]\`          | R7 |
| \`\[R7          | Sec="VIX ML"             | Span=0:180    | Quote="Torch model 16.40 is an outlier"]\`                        | R7 |
| \`\[R7          | Sec="TNX ML"             | Span=0:180    | Quote="ARIMAX model 4.4452 is an outlier"]\`                      | R7 |
| \`\[R7          | Sec="AAPL ML"            | Span=0:180    | Quote="DYNAMIX model 291.24 is an outlier"]\`                     | R7 |
| \`\[R7          | Sec="Risk Management"    | Span=0:180    | Quote="TDA analysis reveals NEUTRAL\_STRUCTURE"]\`                | R7 |
| \`\[R7          | Sec="Final Forecasts"    | Span=0:220    | Quote="Final Three-Day Forecasts Table SPX 7388"]\`               | R7 |
| \`\[R7          | Sec="References"         | Span=0:220    | Quote="Federal Reserve Board — Federal Reserve issues"]\`         | R7 |

***

# Validation Checklist

| Requirement                                            | Result |
| ------------------------------------------------------ | ------ |
| W1 Report Map exists for R7                            | PASS   |
| W2 CER Ledger contains 10–25 claims                    | PASS   |
| W3 Detailed Scorecard exists for R7                    | PASS   |
| W3B Final Scorecard Overview exists                    | PASS   |
| W3D Section Error Summary exists                       | PASS   |
| W4 Issue Log exists                                    | PASS   |
| W5 Canonical Claim List contains 30 claims             | PASS   |
| W6 Single-report claim matrix exists                   | PASS   |
| W7 Internal contradiction matrix is typed and resolved | PASS   |
| W8 Standalone ranking exists                           | PASS   |
| W9 Strengths Table exists                              | PASS   |
| W10 Weaknesses Table exists                            | PASS   |
| W11 Plain-Language Conclusions exist                   | PASS   |
| W12 Executive Contradiction Brief exists               | PASS   |
| W13 Reasoning Hierarchy Summary exists                 | PASS   |
| W14 Super-Truth Synthesis exists                       | PASS   |
| W15 Trace Appendix exists                              | PASS   |
| EvidencePointers are well-formed                       | PASS   |
| No chart-absence penalties were applied                | PASS   |

# VALIDATION: PASSED

# R7 EVALUATION COMPLETE
