# 26 — MISSING DATA LIST (Reference)

**What this is:** the definitive list of quantities that do NOT exist in the user
inputs (10_Calculations, 13_SVL, 14_TDA, 15_fh3_table) and are therefore the ONLY
things an LLM is allowed to compute — exactly once per ticker, inside the
CALC WORKSHEET (29_QUERY_Template, global block 9), with operands shown.

**Rule of thumb:** if a value is in this list → computed in the worksheet, quoted
everywhere else. If a value is NOT in this list → it exists in the inputs and must
be quoted verbatim; recomputing it is a QA failure (WORKSHEET_CONSISTENCY_LOCK).

---

## MISSING — computed in the CALC WORKSHEET (per ticker)

| # | Quantity | Definition (definition of record) | Used by |
|---|---|---|---|
| 1 | median_P | middle value of the sorted Day-3 model forecasts P (n odd) or mean of the two middle values (n even) | Outlier rule 13 |
| 2 | MAD | median of sorted \|Pi − median_P\| (same middle-value convention) | Rule 13 |
| 3 | 0.10×ATR | ATR(14) quoted from 10 × 0.10 | MAD_floor |
| 4 | MAD_floor | max(MAD, 0.10×ATR) | Rules 13–14 |
| 5 | Outlier threshold + tests | threshold = 3.00×MAD_floor; per model: \|Pi − median_P\| ≥ threshold → Y/N | Rule 13, Divergence Note |
| 6 | Dispersion test | (max(P) − min(P)) ≥ max(1.50×ATR, 4.00×MAD_floor) → YES/NO | Rule 14 |
| 7 | Percentile positions | NEAREST-RANK method (pinned): Pk = value at position ceil((k/100)×n) of sorted P; no interpolation | Range Builder |
| 8 | Range_Lo, Range_Hi | values selected from sorted P at the row-7 positions, per branch A/B/C (branch itself is a lookup of Regime/ADX) | AXIOM 2 |
| 9 | Placement markers | marker = Range_Lo + f×(Range_Hi − Range_Lo); needed: P40, P50, P60 + bounds of the target zone | Exact positioning; Consistency Check; SENTIMENT_CONSISTENCY_LOCK |
| 10 | ATR% | ATR(14) / Current × 100 (two decimals) | Technical Indicators table |
| 11 | 0.25×ATR + pivot proximity | \|Current − Classic_Pivot\| ≤ 0.25×ATR → "Near", else "Above"/"Below" | Risk Management |

Edge cases:
- Branch D of the Range Builder (fewer than 3 model forecasts): Range = Exact ± k×ATR
  (k = 0.50/0.75/1.00 by ADX) — also computed in the worksheet if it ever fires.
- DAY+2 FALLBACK (Day+3 non-trading): rows 1–8 still use the provided Day-3 model
  set, re-labeled to the last effective session; anchors switch to FH_Day2 (quoted).

---

## PRESENT IN INPUTS — quote only, never recompute

| Source | Data |
|---|---|
| 10_Calculations | model forecasts + CIs (Torch/DYNAMIX/ARIMAX/PCE/LSTM/GARCH/VAR/RW/ETS); RSI, Stochastic %K, ATR, ADX, CCI, Williams %R, Ultimate Oscillator, ROC, BullBear Power, 50/200-DMA; Classic + Fibonacci pivots with S/R levels; ARIMAX/GARCH diagnostics |
| 13_SVL | Hurst regime (current + change flags), Trend10D, Williams fractals, H20 mini-history |
| 14_TDA | H1_MaxPersistence, H1_CountAbove, H1_Entropy, H1 labels (snapshot only — no Last10 sequences; flip risk = INDETERMINATE) |
| 15_fh3_table | Last_Close_ASOF, FH_Date1–3, FH_Day1–3 per ticker |

Not computing, by design:
- Indicator zone classification = LOOKUP (compare reading to the deterministic bands
  in 29 and quote the matching band row verbatim).
- Range Builder branch selection = LOOKUP (Regime/ADX condition matching).
- FH_sign, bias comparisons, calendar checks = sign/date comparisons, not arithmetic.

---

## Enforcement pointers

- 29_QUERY_Template → AXIOM 0 "CALC_WORKSHEET Contract" (missing-data principle)
- 29_QUERY_Template → Output Requirements, CALC WORKSHEET schema (global block 9; 15 rows, QUOTE/COMPUTE marked)
- 29_QUERY_Template → Stage 7 "WORKSHEET_CONSISTENCY_LOCK"
- 72_AXIOM → W0 FACT_CHECK worksheet, "WORKSHEET_OK" cross-check
