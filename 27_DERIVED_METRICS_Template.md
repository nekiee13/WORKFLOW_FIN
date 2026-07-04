# 27 — DERIVED_METRICS (GROUND TRUTH) — Template

────────────────────────────────────────────────────────
PURPOSE & AUTHORITY
────────────────────────────────────────────────────────
This block is USER-PREPARED input data, computed OUTSIDE the LLM (user pipeline,
spreadsheet, or by hand). It is pasted into 28_QUERY alongside 10/13/14/15.

- Every value here is GROUND TRUTH with the same standing as closes and indicators
  (AXIOM 0 — User Data Primacy).
- NO-COMPUTE RULE (HARD): LLMs consuming this block perform NO arithmetic on covered
  fields — no recomputation, no verification math, no re-rounding. Quote and interpret
  only.
- The formulas shown below are DEFINITIONS OF RECORD: they document how the user
  computes each value (mirroring 29_QUERY_Template) so the numbers stay consistent
  with the query's rules. They are NOT instructions for the LLM to execute.

ASSEMBLY
- Fill one block per ticker (SPX, DJI, QQQ, VIX, TNX, AAPL), all fields.
- A field the user cannot supply stays "ABSENT" — the LLM will print
  MISSING_USER_INPUT for it and only then apply the legacy flagged-formula fallback.
- Under DAY+2 FALLBACK (Day+3 non-trading): the model set stays the provided Day-3
  set; set MODEL_SET_DAY accordingly and note the fallback.

────────────────────────────────────────────────────────
DEFINITIONS OF RECORD (user-side; mirror 29_QUERY_Template)
────────────────────────────────────────────────────────
- P = available Day-3 point forecasts {PyCaret/Torch, ARIMAX, PCE, LSTM, GARCH, VAR, RW, ETS, DYNAMIX where present}
- median_P = median(P);  MAD = median(|Pi − median_P|);  MAD_floor = max(MAD, 0.10×ATR)
- Outlier: model i with |Pi − median_P| ≥ 3.00×MAD_floor
- Dispersion trigger: (a) (max(P) − min(P)) ≥ max(1.50×ATR, 4.00×MAD_floor)  OR  (b) any Outlier
- Range branch (requires |P| ≥ 3):
    A: Regime ∈ {RANDOM, MEAN_REVERT} OR ADX < 18  → Range = [P25, P75]
    B: Regime = PERSISTENT OR ADX ≥ 25             → Range = [min(P), max(P)]
    C: 18 ≤ ADX < 25                               → Range = [P20, P80]
    D: |P| < 3 → cannot be precomputed (depends on Exact); leave Range fields ABSENT;
       the LLM applies the legacy Exact ± k×ATR rule, flagged DERIVED_METRIC.
- Placement zones over W = Range_Hi − Range_Lo (for sentiment-anchored Exact placement
  and consistency checks; all boundaries precomputed here so the LLM never computes
  percentages):
    P20 = Lo+0.20×W; P30 = Lo+0.30×W; P40 = Lo+0.40×W; P50 = Lo+0.50×W;
    P60 = Lo+0.60×W; P70 = Lo+0.70×W; P80 = Lo+0.80×W
- Pivot proximity: |Current − Classic_Pivot| ≤ 0.25×ATR → "Near"; else "Above"/"Below"
- ATR% = ATR(14) / Current × 100 (two decimals)
- Indicator zones use 29_QUERY_Template's deterministic baseline bands EXACTLY:
    RSI(14): <30 oversold, 30–70 neutral, >70 overbought
    Stochastic %K: <20 oversold, 20–80 neutral, >80 overbought
    Williams %R: <−80 oversold, −80 to −20 neutral, >−20 overbought
    ADX(14): <18 range, 18–25 transition, >25 trend
    CCI(14): <−100 oversold, −100 to +100 neutral, >+100 overbought
    Ultimate Oscillator: <30 oversold, 30–70 neutral, >70 overbought
    ROC(10): sign only (positive/negative/flat momentum)
    BullBear Power: sign only (bulls/bears/balanced)
    50-DMA / 200-DMA: Current above → bullish bias; below → bearish bias

────────────────────────────────────────────────────────
PER-TICKER BLOCKS (repeat ×6; fill every ==field==)
────────────────────────────────────────────────────────

### DERIVED_METRICS: ==TICKER==
ASOF: ==YYYY-MM-DD==   |   MODEL_SET_DAY: ==Day 3==   |   CALENDAR: ==normal / DAY+2 FALLBACK==

**Dispersion & outliers**
| Field | Value |
|---|---|
| N_models | ==N== |
| min_P / max_P | ==v== / ==v== |
| median_P | ==v== |
| MAD | ==v== |
| MAD_floor | ==v== |
| Outlier models | ==none / model names + values== |
| Dispersion trigger | ==NO / YES (rule a: wide dispersion / rule b: outlier)== |

**Range Builder (ground truth)**
| Field | Value |
|---|---|
| Regime (SVL) | ==RANDOM / MEAN_REVERT / PERSISTENT== |
| ADX(14) | ==v== |
| Branch fired | ==A [P25,P75] / B [min,max] / C [P20,P80] / D see definitions== |
| Range_Lo | ==v== |
| Range_Hi | ==v== |

**Placement zones (precomputed; LLM selects Exact inside the applicable interval)**
| Marker | Value |
|---|---|
| P20 / P30 / P40 | ==v== / ==v== / ==v== |
| P50 | ==v== |
| P60 / P70 / P80 | ==v== / ==v== / ==v== |

**Pivot & volatility**
| Field | Value |
|---|---|
| Current (Yahoo close) | ==v== |
| Classic_Pivot | ==v== |
| 0.10×ATR | ==v== |
| 0.25×ATR | ==v== |
| Pivot proximity | ==Above / Near / Below== |
| ATR% | ==v %== |

**Indicator zones (quote-only; zones per definitions of record)**
| Indicator | Reading | Zone |
|---|---|---|
| RSI(14) | ==v== | ==oversold / neutral / overbought== |
| Stochastic %K | ==v== | ==oversold / neutral / overbought== |
| Williams %R | ==v== | ==oversold / neutral / overbought== |
| ADX(14) | ==v== | ==range / transition / trend== |
| CCI(14) | ==v== | ==oversold / neutral / overbought== |
| Ultimate Oscillator | ==v== | ==oversold / neutral / overbought== |
| ROC(10) | ==v== | ==positive / negative / flat== |
| BullBear Power | ==v== | ==bulls / bears / balanced== |
| 50-DMA | ==v== | ==bullish bias / bearish bias== |
| 200-DMA | ==v== | ==bullish bias / bearish bias== |
