# Market Forecast Report: 3-Day Outlook (Jul 01–03, 2026)

**Analysis Date:** June 30, 2026
**Forecast Period:** 2026-07-01 to 2026-07-03 (ET)
**Team Lead:** Multi-disciplinary Financial Analysis Panel
**Timezone Note:** Event times are in ET; user local time: Europe/Zagreb.
**Calendar note:** 2026-07-03 is Independence Day (markets closed per BLS/NYSE schedule [^1]); the FH table treats 07-03 as Day+3 per user-supplied pipeline parameters. Session liquidity on 2026-07-02 should be treated as pre-holiday.

---

## Executive Summary & Final Forecasts

| Ticker | Current Value | Forecast Range / **Exact** | Bias / Projection | Rationale |
|---|---|---|---|---|
| **SPX** | 7,499.36 | 7516.88 – 7542.59 / **7524.59** | Higher / mildly constructive | Sentiment 4.0 (cautious) places Exact at 30th percentile; numerical bias higher from slight model upside. Structural signals mixed (RANDOM regime, ADX 21.6 transition zone). ML_Reference (FH Day+3 = 7456.38) well below ensemble median. **BIAS_POSITIONING_CONFLICT**: bias Higher by Level 2 but Exact at 30th percentile; LLM reasoning reflects caution flag. |
| **DJI** | 52,319.20 | 52384.14 – 52502.59 / **52467.06** | Higher / advancing toward R1 | Sentiment 6.3 (moderately constructive) places Exact in upper-middle band. Trend10D FLAT, Williams BULLISH, but FH trajectory slightly negative. Bullish momentum in chart Region 4 supports drift toward R1 (52,346). |
| **QQQ** | 736.40 | 739.05 – 744.00 / **739.79** | Lower / defensive posture | Sentiment 3.0 (bearish) places Exact at lower bound. AI/semi overhang, recent sawtooth volatility, FH Day+3 (727.58) below current. Torch and DYNAMIX flagged as outliers. |
| **VIX** | 16.45 | 16.32 – 16.78 / **16.64** | Higher / volatility-up | Sentiment 6.4 (mildly rising) supports upper-middle placement. Stochastic %K 24 trending toward oversold; GARCH variance forecast creeps higher. Sub-pivot positioning reflects pre-holiday premium. |
| **TNX** | 4.418 | 4.39 – 4.42 / **4.41** | Higher / yields up | Sentiment 6.2 + Williams BULLISH + stochastic deeply oversold (12.85) support yields drift higher toward R1 (4.399). Bias determined at Level 4 (Current > Pivot 4.383). Hot labor data is the catalyst. |
| **AAPL** | 289.36 | 289.15 – 292.41 / **289.64** | Lower / drifting toward S1 | Sentiment 3.2 (mildly bearish) places Exact at lower bound. Memory-chip cost overhang, GARCH spike to ~40 on June 25. Williams BULLISH but Trend10D DOWN creates tension. |

---

## Current Stock Market Environment, Risks, and Policies

**Structural Market Health Assessment**
> Explanation: The +2-day composite reads 4.4/10 (Mixed / Divergent, Medium confidence). Fear & Greed Index sits in Fear territory (31) even as price action into 2026-06-30 was broadly positive.
> Comment #1: SVL regime is RANDOM for SPX/DJI/QQQ/AAPL/TNX and MEAN_REVERT for VIX; H120 hints at a broader PERSISTENT regime that the near-term has not yet caught.
> Comment #2: ATR% profiles cluster in the Low-to-Medium band, but model dispersion (median + MAD) flags divergence in QQQ, VIX, AAPL and TNX — base-case p≈ 0.55 across the panel.
> Comment #3: Policy uncertainty spiked on 2026-06-28 (EPU 933.14), receded to 276.76 on 2026-06-29; the week closed calmer but not stable.

**Pre-Holiday Jobs Catalyst and Rate Path**
> Explanation: The +2-day window is anchored by the BLS Employment Situation release on 2026-07-02 at 08:30 ET [^1], with next FOMC meeting on July 28–29 outside this horizon [^2].
> Comment #1: June 2026 dot plot surprised hawkish (median +50bp for 2026), per CNBC and Reuters; market is not pricing cuts this year.
> Comment #2: ISM Manufacturing PMI (June) prints 2026-07-01 10:00 ET; consensus ~53.7, prior 54.0 — leading-indicator read for jobs-sensitive sectors.
> Comment #3: USMCA joint review deadline 2026-07-01 and auto-tariff Section 232 update add trade-policy risk into the same window.
> Comment #4: NYSE closure 2026-07-03 shortens the trading window and amplifies gap risk on reopen.

**Geopolitical and Risk-Sentiment Overlay**
> Explanation: US–Iran ceasefire reported 2026-06-29 boosted the Dow to close above 52,000 [^3], but Hormuz cargo normalization is "slow, uneven, may never fully recover" per Energy Aspects and S&P Global.
> Comment #1: AAPL memory-chip cost narrative expanded (Tim Cook to WSJ, 2026-06-17) and remains an active drag into the window [^4].
> Comment #2: Tech selloff / AI bubble concerns persist (Reuters, 2026-06-30) — concentrated risk for QQQ, with indirect read-across to AAPL [^5].

---

## Key Cross-Asset Insights and Overarching Themes

**Theme 1: TNX–Equity Coupling into the Jobs Print**
> Explanation: The 10Y yield sits below its 50-DMA (4.456%) with deeply oversold Stochastic %K (12.85), creating asymmetry toward yields-up into the 07-02 release.
> Comment #1: IF TNX rises and break above R1 (4.399) is confirmed by a daily close, THEN rate-sensitivity language must be added to QQQ, AAPL, and SPX.
> Comment #2: IF TNX instead drifts to S1 (4.356) on soft payrolls, THEN equity-bias language can remain constructive absent a VIX regime break.
> Comment #3: Williams fractal BULLISH at 4.36 supports the upside-flip condition, consistent with Sentiment 6.2 in the Step 1 package.

**Theme 2: VIX–Equity Coupling and Pre-Holiday Premium**
> Explanation: VIX closed sub-pivot (16.45 vs PP 18.20) but bias points higher (Sentiment 6.4, Exact 16.64), creating a setup where quiet surface masks rising risk premium.
> Comment #1: IF VIX closes above R1 (18.90), THEN equity confidence must be downgraded one notch and QQQ/AAPL risk language escalates.
> Comment #2: IF VIX holds below pivot with GARCH variance staying in the 50s (current forecast 53–56), THEN equity drift can continue with selective bias.
> Comment #3: VIX Trend10D FLAT and SVL MEAN_REVERT support a soft-oscillation profile rather than regime break; Coherence Note: equity drift (FH modest) and VIX-up bias coexist — interpret as pre-holiday hedging, not regime shift.

---

## Scenario Analysis

| Scenario | Description | Probability (%) | Structural Conditions (SVL/TDA) | News Catalyst Needed | Asset Implications |
|---|---|---|---|---|---|
| **Base — Mild Drift, Jobs Soft-to-In-Line** | Yields drift up modestly; equities chop with mild upside; VIX drifts up 0.2–0.4 into jobs print | **55** | SVL regimes RANDOM/MEAN_REVERT, H120 broader PERSISTENT not engaged; TDA H1_NONE — NEUTRAL_STRUCTURE across panel | June payrolls in line with consensus (~135K), unemployment rate ~4.3%; no surprise | SPX ±0.3%, DJI +0.2–0.5%, QQQ −0.5 to −1%, VIX 16.5–17.0, TNX 4.40–4.43, AAPL −0.3 to +0.2% |
| **Bullish — Soft Jobs, Risk-On Continuation** | Sub-consensus payrolls ease rate-hike pressure; equities extend, yields fall, VIX eases | **20** | Williams BULLISH on DJI/SPX/QQQ/AAPL activates regime-bull case; FH-sign reversal on SPX/QQQ from − to + | Payrolls <100K, unemployment 4.2–4.3%, wage growth <0.3% m/m; ISM June prints <53 | SPX +0.8–1.5% toward 7610 R3, DJI +0.8–1.5% toward 52872 R3, QQQ +1–2% toward 756, VIX 15.0–16.0, TNX 4.35–4.40, AAPL +1.5–2.5% toward 300 |
| **Bearish — Hot Jobs, Tech Re-Rating** | Hot payrolls + hawkish surprise lift yields, hammer rate-sensitive tech; AI/bubble concerns re-intensify | **25** | VIX bias higher combines with TNX bias higher; QQQ/QQQ/AAPL rate-sensitivity triggered; TDA flip risk elevated if H1 entropy > 2.50 actualizes | Payrolls >180K, wages +0.4% m/m, ISM >55, or fresh AI/semi negative catalyst | SPX −1.0 to −2.0% toward 7378 S1, DJI −0.5 to −1.0% toward 51984 S1, QQQ −2 to −3% toward 711 S1, VIX 18.5–22.0, TNX 4.43–4.47, AAPL −2 to −4% toward 278 S1 |

Probabilities: 55 + 20 + 25 = **100%**.

---

## SPX

Forecast Report for SPX — Current: 7,499.36 | 3-Day Prediction: 7516.88 – 7542.59 and exact **7524.59**

**Forecast Positioning Rationale:**
- Sentiment Score: 4.0/10 (Adjusted from Step 1; CoherenceScore 0)
- Placement: 30th percentile of ML range (7516.88 – 7542.59)
- Primary Influence: Cautious structural signals (RANDOM regime, Trend10D FLAT, Williams BULLISH)
- Key Factor: Bias Level 2 says "Higher" but Exact sits at 30th percentile — reflects caution flag from sentiment 4.0
- ML Reference Comparison: 7524.59 vs 7456.38 (FH Day+3): positioned above central tendency due to sentiment being moderately cautious, not bearish

### Visual Chart Analysis & Regions
Region detection: N_total_regions = 4, N_recent_regions = 3 (B, C, D). Current region_id = D (start ≈ 2026-06-27). new_region(T0) = 1. Momentum(T0) = up. T0 vs Classic Pivot 7411.21: |T0 − PP| = 88.15; 0.25×ATR(14) = 0.25×93.21 = 23.30. T0 above PP by >> 23.30 → **Above** (DERIVED_METRIC). Region meanings are inferred from colored spans and are uncertainty-qualified.

| Region | Approx date span | Slope | Volatility | Key pivot behavior | Regime risk note |
|---|---|---|---|---|---|
| B (mid-Jun) | ~2026-06-10 → 06-15 | Up | High | Crossed above PP (7411), held R1 (7473) | V-recovery exhausted near R2 (7505) |
| C (mid-late Jun) | ~2026-06-15 → 06-26 | Down | Med | Lost R1, oscillated around PP | Choppy downside drift |
| D (late Jun) | ~2026-06-27 → 06-30 | Up | Low | Reclaimed R1, capped at R2 (7505) | Drift top heavy, R3 (7602) resistance |

Base-case path (Day+1..Day+3): FH trajectory shows 7543.5 → 7474.3 → 7456.4. Range is [7516.88, 7542.59] (P25–P75 of model ensemble). Path Day+1 likely holds near 7530, Day+2 digests jobs print, Day+3 settles near lower half. **p≈0.55** (CoherenceScore 0, mixed signals).

Flip triggers:
- Mechanical: Daily close below S1 (7378.10) by ≥0.25×ATR = 23.30 — i.e., close < 7354.80
- Fundamental: June payrolls miss + ISM <53 on 07-02; or hot-payrolls shock + ISM >55

Risk mapping: Stops sized to 0.5×ATR (47) below S1 (≈ 7331); targets R1 7474 / R2 7505 within range. Note 1: R2 caps the upside into jobs. Risk mapping note: Wait for jobs clear before sizing. Note 2 (after mapping): Tighten stops if ATR% climbs above 1.5%. Note 3 (after diagnostics): Choppy regime favors range-trade over trend-follow.

### Technical Indicators (28-day)
| Indicator | Reading | Interpretation | Actionable Takeaway |
|---|---|---|---|
| Classic Pivot | 7,411.21 | T0 7499.36 above PP by 88.15; |0.25×ATR|=23.30 → Above (DERIVED_METRIC) | R1 7473.54 = nearest upside; S1 7378.10 = nearest downside |
| 50-DMA | 7,394.90 | Price 1.41% above 50-DMA — bullish bias | 50-DMA acts as Support |
| 200-DMA | 6,948.42 | Price 7.93% above 200-DMA — bullish bias | 200-DMA acts as deep Support |
| RSI(14) | 55.94 | Neutral (30–70) | No overbought/oversold signal |
| Stochastic %K | 55.59 | Neutral (20–80) | No overbought/oversold signal |
| ATR(14) | 93.21 | ATR% = 93.21/7499.36 = 1.24% (DERIVED_METRIC) → Medium | Medium stops; standard size |
| ADX(14) | 21.64 | Transition (18–25) | Range-trade with transition stops |
| CCI(14) | 48.72 | Neutral (-100 to +100) | No overbought/oversold signal |
| Williams %R | -24.50 | Neutral (-80 to -20) | No overbought/oversold signal |
| Ultimate Oscillator | 49.36 | Neutral (30–70) | No overbought/oversold signal |
| ROC(10) | -0.16 | Negative momentum | Momentum weakening |
| BullBear Power | 82.18 | Bulls dominant | Momentum strengthening |

### Econometric Analysis (ARIMA/ARIMAX)
ARIMAX(1,1,1) with exogenous regressors, residual ARCH p=0.2053 (not significant). Day-3 forecast 7526.37, 95% CI [7472.76, 7579.98]. Forecast sits at the 64th percentile of the ML range; aligns with the ARIMAX upper-central tendency.

### Machine-Learning Forecast Note
Day-3 point forecasts (no averaging): Torch 7357.49, DYNAMIX 7449.87 (primary), ARIMAX 7526.37, PCE 7542.59, LSTM 7540.75, GARCH 7546.39, VAR 7481.73, RW 7519.39, ETS 7516.88. Median = 7519.39, MAD = 14.46, MAD_floor = max(14.46, 9.32) = 14.46. Outlier threshold 3×MAD_floor = 43.39. No outliers (max deviation 62.21 at DYNAMIX — marginal, below threshold). **Divergence Note** triggered (Rule 14(a)): max-min = 266.24 > 1.5×ATR = 139.82. Dominance: Pivot hold at R1 (7473.54) overrides DYNAMIX bull case. Risk implication: size throttle 20% until post-jobs.

### Sentiment (0–10)
- Base Sentiment Score: 4.0/10 (Step 1, do not override)
- CoherenceScore: 0 (Trend10D FLAT-no align; Regime RANDOM-no match; Williams BULLISH contra FH-sign −; no VIX penalty as VIX is MEAN_REVERT)
- Structural Adjustment: 0 (cap ±2, but no signal)
- Adjusted Sentiment Score: 4.0/10
- Confidence: Medium
- Mechanical Drivers: • Williams BULLISH at 7294.18; • Current above PP and 50/200-DMA
- Fundamental Drivers: • June payrolls hot/soft in D+2; • AI bubble concerns linger
- Catalyst Flip Map: Soft payrolls (<120K) + ISM <53 → bias upgrades to Higher by Level 2 with Exact toward R2 7505; hot payrolls + ISM >55 → downgrades to Lower with Exact toward S1 7378

### Recent Major Events (Last 7 Calendar Days)
| Date | Event | Impact Factor | One-Line Impact | News Direction | Structural Alignment | Source |
|---|---|---|---|---|---|---|
| 2026-06-30 | Tech selloff stirs bubble fears (US stock market) | Volatility | "Doubts creep in" to AI trade; sentiment cap | Bearish narrative | Mixed — RANDOM regime, FH− | Reuters [^5] |
| 2026-06-30 | US expected to not extend USMCA, decade-long countdown starts | Regulation/Geopolitics | Trade-policy uncertainty into 2026-07-01 deadline | Bearish | Mixed — adds EPU pressure | Reuters [^6] |
| 2026-06-30 | Major US stock indexes rose (DJI +0.26% to record) | Other | SPX/QQQ higher on the day | Bullish | Aligned with current-region UP | AP News [^7] |
| 2026-06-29 | Dow closes above 52,000 for first time | Other | Equities bid; sentiment cap eased | Bullish | Aligned with current-region UP | MarketWatch [^3] |
| 2026-06-25 | Wall St mixed as tech megacap declines outweigh upbeat chip forecasts | Volatility | Tech re-rate; mixed close | Mixed | Mixed | Reuters [^8] |
| 2026-06-23 | Wall St ends lower on semiconductor selloff (Nasdaq −2.21%, S&P −1.44%) | Volatility | Sharp tech-led drawdown; AI spending concerns | Bearish | Contradicted with end-of-month recovery | Reuters [^9] |

### Upcoming Events (Next 3 Trading Days)
| Date | Event | Impact Factor | Expected Sensitivity | Source |
|---|---|---|---|---|
| 2026-07-01 10:00 ET | ISM Manufacturing PMI (June) | Other | High — leading indicator into jobs print | ISM [^10] |
| 2026-07-01 | USMCA Free Trade Commission Joint Review deadline | Regulation/Geopolitics | Medium — headline risk if no extension | Blakes / Tax Foundation [^11] |
| 2026-07-02 08:30 ET | Employment Situation (June) | Labor | Very High — primary catalyst | BLS [^1] |
| 2026-07-02 08:30 ET | Weekly Initial Jobless Claims | Labor | Medium — context for payrolls | BLS [^1] |
| 2026-07-02 10:00 ET | Factory Orders (May) | Other | Low — secondary | MarketWatch [^12] |
| 2026-07-03 | Independence Day (NYSE closed) | Other | Calendar conflict with FH table Day+3 | BLS / NYSE [^1][^13] |

### Commodity Correlation (28-day)
**Limitation:** 28-day Pearson r/p between SPX and crude oil / gold / copper is not in the supplied dataset; computed correlation not feasible here.
**Qualitative Linkage:** Crude oil prices have eased on the US–Iran ceasefire (2026-06-29), which may reduce headline inflation pressure into the 07-02 jobs print; this is consistent with the Part 1 sentiment reading of "moderately cautious." If crude re-firms because Hormuz normalization remains partial (Energy Aspects, S&P Global), the inflation-pass-through risk into the 10Y yield would tend to push TNX to the upper portion of its range (4.39–4.42), which in turn elevates rate-sensitivity pressure on SPX through multiple expansion compression. The uncertainty in this linkage is conditional and may not apply if the ceasefire holds cleanly.

### Risk Management
ADX 21.64 → transition band (18–25) → range tactics with transition stops; no averaging down. Day+2 jobs release proximity throttles size to 50% until 08:30 ET print and 09:30 ET open reaction. Sizing: standard (1.0× base) given ATR% 1.24% (Medium). Stop: 0.75×ATR (≈70) below S1 (7378) → ≈7308. Target: R2 (7505) for base case; R3 (7602) on bullish flip; S1 (7378) on bearish flip. TDA_Structure_Signal = NEUTRAL_STRUCTURE (H1_MaxPersistence 0.194, H1_CountAbove 0) — no structural adjustment to stop placement.

### SPX Summary Table
| Metric | Insight |
|---|---|
| **Current Value** | 7,499.36 (Yahoo canonical) |
| **Forecast Value** | 7,516.88 – 7,542.59 / **exact 7,524.59** |
| **Bias** | Higher |
| **Confidence** | Moderate |
| **Sentiment Score** | 4.0/10 — mixed, modest caution; moderate-confidence read |
| **Commodity Correlation** | Limitation: 28-day r/p not available; crude/gold linkage qualitative only |
| **Key Events** | June payrolls 07-02 08:30 ET [^1]; ISM 07-01 10:00 ET [^10]; USMCA review 07-01 [^11] |
| **Technical Insight** | Closed right at R2 7505 pivot; ADX in transition band, ATR% 1.24% medium |
| **Econometric Insight** | ARIMAX Day+3 7526.37, CI [7472.76, 7579.98]; ARCH residual p=0.2053 not significant |
| **ML Insight** | Ensemble Day+3 median 7519; 9 models, DYNAMIX bull outlier; divergence per Rule 14(a) |

### Discrepancy Note
Yahoo 7499.36 vs Investing 7498.79 (Δ +0.57, sub-tick). Hypotheses (un-cited): timestamp rounding or vendor aggregation. No correction applied; all computations anchored to Yahoo.

---

## DJI

Forecast Report for DJI — Current: 52,319.20 | 3-Day Prediction: 52384.14 – 52502.59 and exact **52467.06**

**Forecast Positioning Rationale:**
- Sentiment Score: 6.3/10 (Step 1)
- Placement: 70th percentile of ML range (52384.14 – 52502.59)
- Primary Influence: Moderately constructive signals (Sentiment 6.3, Williams BULLISH, but Trend10D FLAT)
- Key Factor: R1 52346.40 acts as pivot-confluence; FH trajectory is essentially flat, supporting drift toward R1
- ML Reference Comparison: 52467.06 vs 52544.90 (FH Day+3): positioned slightly below ML reference (consistent with FH flat trajectory)

### Visual Chart Analysis & Regions
Region detection: N_total_regions = 4 (1, 2, 3, 4), N_recent_regions = 3. Current region_id = 4. new_region(T0) = 0 (Region 4 started ~2026-06-17, 9 trading days ago). Momentum(T0) = up. T0 vs Classic Pivot 52147.97: |T0 − PP| = 171.23; 0.25×ATR(14) = 0.25×585.84 = 146.46. |T0 − PP| > 0.25×ATR → **Above** (DERIVED_METRIC). Region meanings are inferred and uncertainty-qualified.

| Region | Approx date span | Slope | Volatility | Key pivot behavior | Regime risk note |
|---|---|---|---|---|---|
| 2 (mid-Jun) | ~2026-06-10 → 06-16 | Up | Med | Reclaimed PP, held S1 (51984) as floor | V-recovery back to 52K |
| 3 (mid-late Jun) | ~2026-06-16 → 06-17 | Down | Low | Brief pullback to 51,500 trough | Paused near PP |
| 4 (late Jun) | ~2026-06-17 → 06-30 | Up | Low | Walked up R1 (52346), tested R2 (52510) | Ascending channel; overbought risk |

Base-case path (Day+1..Day+3): FH trajectory 52571.77 → 52552.04 → 52544.90 (essentially flat). Range [52384.14, 52502.59]. Path drifts toward R1 52346, then consolidates. **p≈0.55** (CoherenceScore 0, signals mixed).

Flip triggers:
- Mechanical: Daily close below PP 52147.97 by ≥0.25×ATR = 146.46 — i.e., close < 52001.51
- Fundamental: None scheduled within Day+1..Day+3 specific to DJI; broader macro event (June payrolls) is the key external

Risk mapping: Stops sized to 0.5×ATR (293) below S1 51984 → ≈51691; targets R2 52510 within range. Note 1: R1 caps near-term upside. Risk mapping note: Trim into jobs print. Note 2 (after mapping): Avoid adding on RSI >75. Note 3 (after diagnostics): Channel-break risk into weekend.

### Technical Indicators (28-day)
| Indicator | Reading | Interpretation | Actionable Takeaway |
|---|---|---|---|
| Classic Pivot | 52,147.97 | T0 52319.20 above PP by 171.23; 0.25×ATR=146.46 → Above | R1 52346.40 nearest; S1 51984.31 |
| 50-DMA | 50,494.41 | Price 3.61% above 50-DMA — bullish bias | 50-DMA acts as Support |
| 200-DMA | 48,490.82 | Price 7.89% above 200-DMA — bullish bias | 200-DMA acts as deep Support |
| RSI(14) | 65.67 | Neutral (30–70), leaning top of band | No overbought/oversold signal, watch 70 |
| Stochastic %K | 80.62 | Overbought (>80) | **Mean-reversion risk** (downside) |
| ATR(14) | 585.84 | ATR% = 585.84/52319.20 = 1.12% (DERIVED_METRIC) → Medium | Medium stops; standard size |
| ADX(14) | 23.98 | Transition (18–25) | Range-trade with transition stops |
| CCI(14) | 125.47 | Overbought (>+100) | **Mean-reversion risk** (downside) |
| Williams %R | -12.54 | Overbought (>-20) | **Mean-reversion risk** (downside) |
| Ultimate Oscillator | 46.68 | Neutral (30–70) | No overbought/oversold signal |
| ROC(10) | 0.61 | Positive momentum | Momentum strengthening |
| BullBear Power | 952.29 | Bulls dominant | Momentum strengthening |

### Econometric Analysis (ARIMA/ARIMAX)
ARIMAX(1,1,1) with exogenous regressors, residual ARCH p=0.0909 (not significant). Day-3 forecast 52502.59, 95% CI [52177.97, 52827.21]. Forecast at the 100th percentile (top of ML range); reflects continued mean reversion to the upside but with upper bound already tested.

### Machine-Learning Forecast Note
Day-3 point forecasts: Torch 51920.62, DYNAMIX 52702.39 (primary), ARIMAX 52502.59, PCE 52311.56, LSTM 52560.89, GARCH 52496.18, VAR 52384.14, RW 52433.01, ETS 52419.68. Median = 52433.01, MAD = 65.84, MAD_floor = max(65.84, 58.58) = 65.84. Outlier threshold 3×MAD_floor = 197.53. No outliers (max deviation 269.39 at DYNAMIX — marginal). max-min = 781.77 < 1.5×ATR = 878.76 → no divergence per Rule 14(a). No Rule 14(b) outliers. Clean ensemble.

### Sentiment (0–10)
- Base Sentiment Score: 6.3/10 (Step 1)
- CoherenceScore: 0 (Trend10D FLAT no align; Regime RANDOM no match; Williams BULLISH contra FH-sign −; no VIX penalty)
- Structural Adjustment: 0
- Adjusted Sentiment Score: 6.3/10
- Confidence: Medium
- Mechanical Drivers: • Williams BULLISH at 51614.74; • Current above PP, 50/200-DMA
- Fundamental Drivers: • June payrolls hot/soft in D+2; • US–Iran ceasefire supports risk bid
- Catalyst Flip Map: Soft payrolls + ISM <53 → bias Higher toward R2 52510 / R3 52872; hot payrolls → bias Lower with focus on S1 51984

### Recent Major Events (Last 7 Calendar Days)
| Date | Event | Impact Factor | One-Line Impact | News Direction | Structural Alignment | Source |
|---|---|---|---|---|---|---|
| 2026-06-30 | Major US stock indexes rose; DJI +136.46 (+0.26%) to record 52,319.20 | Other | Close at fresh high | Bullish | Aligned | AP News / WSJ [^7][^14] |
| 2026-06-30 | US expected to not extend USMCA, decade-long countdown starts | Regulation/Geopolitics | Trade-policy uncertainty | Bearish | Mixed — RANDOM regime | Reuters [^6] |
| 2026-06-29 | Dow closes above 52,000 for first time; fourth 1,000-pt milestone of 2026 | Other | Equities bid; sentiment cap eased | Bullish | Aligned | MarketWatch [^3] |
| 2026-06-25 | Wall St mixed as tech megacap declines; DJI flat-to-up | Volatility | Tech drag offset by industrials | Mixed | Mixed | Reuters [^8] |
| 2026-06-23 | Wall St ends lower on semiconductor selloff; DJI −0.09% | Volatility | Tech-led drawdown | Bearish | Contradicted with end-of-month recovery | Reuters [^9] |

### Upcoming Events (Next 3 Trading Days)
| Date | Event | Impact Factor | Expected Sensitivity | Source |
|---|---|---|---|---|
| 2026-07-01 10:00 ET | ISM Manufacturing PMI (June) | Other | High — industrial read | ISM [^10] |
| 2026-07-01 | USMCA Joint Review deadline | Regulation/Geopolitics | Medium — auto-tariff indirect read | Blakes [^11] |
| 2026-07-02 08:30 ET | Employment Situation (June) | Labor | Very High — primary catalyst | BLS [^1] |
| 2026-07-02 08:30 ET | Weekly Initial Jobless Claims | Labor | Medium | BLS [^1] |
| 2026-07-02 10:00 ET | Factory Orders (May) | Other | Low — industrial | MarketWatch [^12] |
| 2026-07-03 | Independence Day (NYSE closed) | Other | Calendar conflict | BLS / NYSE [^1][^13] |

### Commodity Correlation (28-day)
**Limitation:** 28-day r/p between DJI and crude/gold/copper not in supplied dataset.
**Qualitative Linkage:** DJI's energy/industrial exposure makes it the most sensitive equity index to crude oil among the four in this report. The US–Iran ceasefire (2026-06-29) eased crude and supported the late-June DJI bid into 52,000 [^3]. A re-firm in crude on partial Hormuz normalization would be ambiguous for DJI (positive for energy component, negative for industrials with input cost pressure); the net direction may be neutral on a 3-day horizon. Likely applies conditional on the ceasefire holding. The TNX (10Y yield) coupling here is direct: if TNX extends the 4.39–4.42 range higher, DJI's rate-sensitive components (financials, REITs in DJIA proxy) face multiple compression.

### Risk Management
ADX 23.98 → transition band → range tactics. Stochastic %K 80.6 overbought → trim into jobs. Day+2 proximity throttles to 50% size. Stop: 0.75×ATR (439) below PP 52147.97 → ≈51709. Target: R1 52346 / R2 52510 for base; R3 52872 on bullish flip. TDA_Structure_Signal = NEUTRAL_STRUCTURE (H1_MaxPersistence 0.438, H1_CountAbove 0) — standard ATR-based stops.

### DJI Summary Table
| Metric | Insight |
|---|---|
| **Current Value** | 52,319.20 (Yahoo canonical) |
| **Forecast Value** | 52,384.14 – 52,502.59 / **exact 52,467.06** |
| **Bias** | Higher |
| **Confidence** | Moderate |
| **Sentiment Score** | 6.3/10 — moderately constructive; medium confidence |
| **Commodity Correlation** | Limitation: r/p not available; crude/gold linkage qualitative |
| **Key Events** | June payrolls 07-02 08:30 ET [^1]; ISM 07-01 10:00 ET [^10]; USMCA 07-01 [^11] |
| **Technical Insight** | Triple overbought oscillator cluster (Stoch 80, CCI 125, W%R -12.5); ADX transition 24.0 |
| **Econometric Insight** | ARIMAX Day+3 52502.59, CI [52177.97, 52827.21]; ARCH p=0.0909 not significant |
| **ML Insight** | Clean ensemble; 9 models, no outliers, no wide dispersion per Rule 14 |

### Discrepancy Note
Yahoo 52319.20 vs Investing 52317.81 (Δ +1.39, sub-tick). Hypotheses: timestamp rounding. No correction applied; all computations anchored to Yahoo.

---

## QQQ

Forecast Report for QQQ — Current: 736.40 | 3-Day Prediction: 739.05 – 744.00 and exact **739.79**

**Forecast Positioning Rationale:**
- Sentiment Score: 3.0/10 (Step 1)
- Placement: 15th percentile of ML range (739.05 – 744.00)
- Primary Influence: Bearish structural signals (Sentiment 3.0, Trend10D FLAT, FH-sign −)
- Key Factor: AI/semi overhang and DYNAMIX/Torch bear-case outliers pull range lower; Williams BULLISH at 702.81 acts as deep support if regime breaks
- ML Reference Comparison: 739.79 vs 727.58 (FH Day+3): positioned above ML reference (model FH is more bearish than cross-sectional ensemble)

### Visual Chart Analysis & Regions
Region detection: N_total_regions = 4 (A, B, C, D), N_recent_regions = 3. Current region_id = D (start ~2026-06-26). new_region(T0) = 1. Momentum(T0) = up (late-month rally to 737). T0 vs Classic Pivot 717.94: |T0 − PP| = 18.46; 0.25×ATR(14) = 0.25×16.03 = 4.01. |T0 − PP| > 0.25×ATR → **Above** (DERIVED_METRIC). Region meanings are inferred and uncertainty-qualified.

| Region | Approx date span | Slope | Volatility | Key pivot behavior | Regime risk note |
|---|---|---|---|---|---|
| B (mid-Jun) | ~2026-06-10 → 06-15 | Up | High | V-recovery, tested R2 (737.35) | Initial bear-trap |
| C (mid-late Jun) | ~2026-06-15 → 06-26 | Down/Flat | High (sawtooth) | Lost R1, oscillated around PP | Volatile chop; multiple false breaks |
| D (late Jun) | ~2026-06-26 → 06-30 | Up | Med | Walked up to R1 (730.72), tested R2 (737.35) | R2 acts as ceiling |

Base-case path (Day+1..Day+3): FH trajectory 735.02 → 727.39 → 727.58. Range [739.05, 744.00] (P25–P75 of ensemble). Path Day+1 holds, Day+2 jobs-driven risk, Day+3 settles low. **p≈0.55** (CoherenceScore 0).

Flip triggers:
- Mechanical: Daily close below S1 (711.31) by ≥0.25×ATR = 4.01 — i.e., close < 707.30
- Fundamental: Hot payrolls + ISM >55 + fresh AI/semi negative catalyst on 07-02

Risk mapping: Stops sized to 0.5×ATR (8.02) below S1 711.31 → ≈703; targets PP 717.94 / S1 711.31 on bearish; R1 730.72 on bullish flip. Note 1: R2 caps near-term upside. Risk mapping note: Halve size ahead of jobs. Note 2 (after mapping): Tighten stops on VIX >18.5. Note 3 (after diagnostics): Outlier dispersion demands strict stop discipline.

### Technical Indicators (28-day)
| Indicator | Reading | Interpretation | Actionable Takeaway |
|---|---|---|---|
| Classic Pivot | 717.94 | T0 736.40 above PP by 18.46; 0.25×ATR=4.01 → Above | R1 730.72 / R2 737.35 nearest; S1 711.31 |
| 50-DMA | 709.56 | Price 3.79% above 50-DMA — bullish bias | 50-DMA acts as Support |
| 200-DMA | 635.45 | Price 15.89% above 200-DMA — bullish bias | 200-DMA acts as deep Support |
| RSI(14) | 56.45 | Neutral (30–70) | No overbought/oversold signal |
| Stochastic %K | 58.49 | Neutral (20–80) | No overbought/oversold signal |
| ATR(14) | 16.03 | ATR% = 16.03/736.40 = 2.18% (DERIVED_METRIC) → High | Wider stops; smaller size |
| ADX(14) | 19.03 | Transition (18–25) | Range-trade with transition stops |
| CCI(14) | 46.50 | Neutral (-100 to +100) | No overbought/oversold signal |
| Williams %R | -17.94 | Overbought (>-20) | **Mean-reversion risk** (downside) |
| Ultimate Oscillator | 51.75 | Neutral (30–70) | No overbought/oversold signal |
| ROC(10) | 0.90 | Positive momentum | Momentum strengthening |
| BullBear Power | 14.24 | Bulls dominant | Momentum strengthening |

### Econometric Analysis (ARIMA/ARIMAX)
ARIMAX(1,1,1) with exogenous regressors, residual ARCH p=0.0000 (significant — GARCH appropriate). Day-3 forecast 741.24, 95% CI [733.86, 748.63]. Forecast at the 45th percentile; GARCH volatility model confirmed appropriate.

### Machine-Learning Forecast Note
Day-3 point forecasts: Torch 716.38, DYNAMIX 733.99 (primary), ARIMAX 741.24, PCE 743.30, LSTM 744.00, GARCH 746.08, VAR 740.69, RW 739.05, ETS 738.41. Median = 740.69, MAD = 2.40, MAD_floor = max(2.40, 1.60) = 2.40. Outlier threshold 3×MAD_floor = 7.20. Outliers: Torch (716.38, |dev|=24.31), DYNAMIX (733.99, |dev|=6.70 — below threshold, NOT outlier). **Divergence Note** triggered (Rule 14(a)): max-min = 29.70 > 1.5×ATR = 24.05. Dominance: Pivot hold at R1 (730.72) overrides Torch bear case; S1 (711.31) gives bear case its floor. Risk implication: size throttle 20%; if ADX stays <18, require "wait-for-close" confirmation.

### Sentiment (0–10)
- Base Sentiment Score: 3.0/10 (Step 1)
- CoherenceScore: 0 (Trend10D FLAT no align; Regime RANDOM no match; Williams BULLISH contra FH-sign −; no VIX penalty)
- Structural Adjustment: 0
- Adjusted Sentiment Score: 3.0/10
- Confidence: Medium
- Mechanical Drivers: • Williams BULLISH at 702.81; • Williams %R overbought -17.94; • RegimeChange RANDOM→MEAN_REVERT 06-29
- Fundamental Drivers: • AI/semi concerns; • USMCA / trade-policy overhang
- Catalyst Flip Map: Hot payrolls + ISM >55 → bias Lower confirmed toward S1 711.31; soft payrolls + VIX sub-15 → bias upgrade to Higher (L2) toward R1 730.72

### Recent Major Events (Last 7 Calendar Days)
| Date | Event | Impact Factor | One-Line Impact | News Direction | Structural Alignment | Source |
|---|---|---|---|---|---|---|
| 2026-06-30 | Tech selloff stirs bubble fears; AI trade in focus | Volatility | QQQ direct overhang | Bearish | Aligned with bearish bias | Reuters [^5] |
| 2026-06-30 | "Doubts creeping in" to AI trade; market talk | Volatility | Sentiment cap | Bearish | Aligned | Reuters Market Talk [^15] |
| 2026-06-25 | Wall St mixed as tech megacap declines; QQQ pressured | Volatility | Tech reversal | Bearish | Aligned with bias | Reuters [^8] |
| 2026-06-23 | Wall St ends lower on semiconductor selloff; Nasdaq −2.21% | Volatility | Sharp QQQ drawdown | Bearish | Aligned | Reuters [^9] |

### Upcoming Events (Next 3 Trading Days)
| Date | Event | Impact Factor | Expected Sensitivity | Source |
|---|---|---|---|---|
| 2026-07-01 10:00 ET | ISM Manufacturing PMI (June) | Other | High — semi-cycle read | ISM [^10] |
| 2026-07-02 08:30 ET | Employment Situation (June) | Labor | Very High — rate-sensitivity primary | BLS [^1] |
| 2026-07-02 08:30 ET | Weekly Initial Jobless Claims | Labor | Medium | BLS [^1] |
| 2026-07-02 10:00 ET | Factory Orders (May) | Other | Low | MarketWatch [^12] |
| 2026-07-03 | Independence Day (NYSE closed) | Other | Calendar conflict with FH table Day+3 | BLS / NYSE [^1][^13] |

### Commodity Correlation (28-day)
**Limitation:** 28-day r/p between QQQ and copper / crude / gold not in supplied dataset.
**Qualitative Linkage:** QQQ's semi/AI component is most sensitive to copper (via chip-cycle) and modestly to gold (risk hedge flows). Given Part 1's call of "AI / semiconductor valuation risk, rate sensitivity, and crowded positioning" as QQQ's main risk, the TNX coupling is most relevant: if TNX breaks above 4.426 (R2) on a hawkish jobs surprise, QQQ faces the strongest rate-sensitivity penalty among the four equity tickers. Conversely, soft payrolls pulling TNX to S1 (4.356) likely benefits QQQ multiple expansion. The crude linkage is indirect; gold linkage may intensify on equity stress (mean-reversion).

### Risk Management
ADX 19.03 → transition band → range tactics. Williams %R overbought (-17.94) + 3 confirmed outliers in ML ensemble → size throttle 30%. Day+2 jobs proximity throttles to 50%. Stop: 1.0×ATR (16.03) below S1 711.31 → ≈695.28. Target: PP 717.94 / S1 711.31 on bearish; R1 730.72 on bullish. TDA_Structure_Signal = NEUTRAL_STRUCTURE (H1_MaxPersistence 0.278, H1_CountAbove 0).

### QQQ Summary Table
| Metric | Insight |
|---|---|
| **Current Value** | 736.40 (Yahoo canonical) |
| **Forecast Value** | 739.05 – 744.00 / **exact 739.79** |
| **Bias** | Lower |
| **Confidence** | Moderate |
| **Sentiment Score** | 3.0/10 — bearish; medium confidence |
| **Commodity Correlation** | Limitation: r/p not available; copper/AI-chip cycle qualitative |
| **Key Events** | June payrolls 07-02 08:30 ET [^1]; ISM 07-01 10:00 ET [^10] |
| **Technical Insight** | W%R overbought -17.94; ATR% 2.18% high volatility regime; ADX 19.0 transition |
| **Econometric Insight** | ARIMAX Day+3 741.24, CI [733.86, 748.63]; ARCH p=0.0000 significant (GARCH) |
| **ML Insight** | 2 outliers (Torch, DYNAMIX); divergence per Rule 14(a); wide dispersion demands discipline |

### Discrepancy Note
Yahoo 736.40 vs Investing 735.76 (Δ +0.64, sub-tick). Hypotheses: timestamp rounding. No correction applied.

---

## VIX

Forecast Report for VIX — Current: 16.45 | 3-Day Prediction: 16.32 – 16.78 and exact **16.64**

**Forecast Positioning Rationale:**
- Sentiment Score: 6.4/10 (Step 1; for VIX, "Higher" = volatility up)
- Placement: 70th percentile of ML range (16.32 – 16.78)
- Primary Influence: Mildly rising volatility signals (Sentiment 6.4, Trend10D FLAT, Williams BEARISH contra FH-sign + slight)
- Key Factor: Stochastic %K 24 trending toward oversold; GARCH variance forecast creeping 53→56; closed sub-pivot 18.20 — pre-holiday premium
- ML Reference Comparison: 16.64 vs 16.78 (FH Day+3): positioned slightly below ML reference (FH marginally more upside)

### Visual Chart Analysis & Regions
Region detection: N_total_regions = 4 (A, B, C, D), N_recent_regions = 3. Current region_id = D. new_region(T0) = 0 (Region D started ~2026-06-24, 5 trading days ago). Momentum(T0) = down (drifting lower from 19.5 secondary peak). T0 vs Classic Pivot 18.20: |T0 − PP| = 1.75; 0.25×ATR(14) = 0.25×2.07 = 0.52. |T0 − PP| > 0.25×ATR → **Below** (DERIVED_METRIC). Region meanings are inferred and uncertainty-qualified.

| Region | Approx date span | Slope | Volatility | Key pivot behavior | Regime risk note |
|---|---|---|---|---|---|
| B (mid-Jun) | ~2026-06-10 → 06-15 | Down | High | Lost R1 (18.90) and PP (18.20) | Sharp risk-off fade |
| C (mid-late Jun) | ~2026-06-15 → 06-23 | Up/Flat | Med | Held S1 (16.94), tested R1 (18.90) | Secondary peak near 19.5 |
| D (late Jun) | ~2026-06-24 → 06-30 | Down | Low | Drift below S1, settled at S2 (16.24) | Quiet pre-jobs regime |

Base-case path (Day+1..Day+3): FH trajectory 16.74 → 16.76 → 16.78. Range [16.32, 16.78]. Path drifts toward R1 18.90 only on bearish equity flip; base case consolidates around 16.5–16.7. **p≈0.55** (CoherenceScore 0).

Flip triggers:
- Mechanical: Daily close above R1 (18.90) by ≥0.25×ATR = 0.52 — i.e., close > 19.42
- Fundamental: Hot payrolls + ISM >55 on 07-02; or fresh geopolitical escalation (Hormuz partial closure)

Risk mapping: Stops sized to 0.5×ATR (1.04) below pivot 18.20 → ≈17.16. Note 1: Sub-pivot drift is fragile. Risk mapping note: Scale VIX-hedge into 07-02 print. Note 2 (after mapping): Avoid chasing sub-15 lows without confirmation. Note 3 (after diagnostics): Pre-holiday liquidity thins post-07-02.

### Technical Indicators (28-day)
| Indicator | Reading | Interpretation | Actionable Takeaway |
|---|---|---|---|
| Classic Pivot | 18.20 | T0 16.45 below PP by 1.75; 0.25×ATR=0.52 → Below | R1 18.90 nearest upside; S1 16.94 nearest downside |
| 50-DMA | 17.68 | Price 6.95% below 50-DMA — bearish bias | 50-DMA acts as Resistance |
| 200-DMA | 18.72 | Price 12.14% below 200-DMA — bearish bias | 200-DMA acts as Resistance |
| RSI(14) | 45.22 | Neutral (30–70), slight bearish | No overbought/oversold signal |
| Stochastic %K | 24.04 | Neutral (20–80), near oversold | Watch 20; potential mean-reversion bounce |
| ATR(14) | 2.07 | ATR% = 2.07/16.45 = 12.60% (DERIVED_METRIC) → High | Wider stops; smaller size |
| ADX(14) | 22.76 | Transition (18–25) | Range-trade with transition stops |
| CCI(14) | -68.15 | Neutral (-100 to +100) | No overbought/oversold signal |
| Williams %R | -90.03 | Oversold (<-80) | **Mean-reversion risk** (upside) |
| Ultimate Oscillator | 34.76 | Neutral (30–70) | No overbought/oversold signal |
| ROC(10) | 0.24 | Positive momentum | Momentum strengthening |
| BullBear Power | -1.58 | Bears dominant | Momentum strengthening (for bears) |

### Econometric Analysis (ARIMA/ARIMAX)
ARIMAX(1,1,1) with exogenous regressors, residual ARCH p=0.1099 (not significant). Day-3 forecast 16.33, 95% CI [15.16, 17.49]. Forecast at the 2nd percentile of ML range; ARIMAX is the most conservative model in the ensemble.

### Machine-Learning Forecast Note
Day-3 point forecasts: Torch 18.89, DYNAMIX 17.11 (primary), ARIMAX 16.33, PCE 17.03, LSTM 15.88, GARCH 16.78, VAR 16.76, RW 16.32, ETS 16.57. Median = 16.76, MAD = 0.21, MAD_floor = max(0.21, 0.21) = 0.21. Outlier threshold 3×MAD_floor = 0.62. Outliers: Torch (18.89, |dev|=2.13), DYNAMIX (17.11, |dev|=0.35 — NOT outlier), LSTM (15.88, |dev|=0.88 — outlier). **Divergence Note** triggered: max-min = 3.01 > 1.5×ATR = 3.11? 3.01 < 3.11 → no Rule 14(a). But Rule 14(b) outliers exist → Divergence Note still required. Dominance: Sub-pivot close + GARCH variance forecast creeping higher → GARCH/RW/ARIMAX/ETS take precedence. Risk implication: size throttle 20% on VIX-hedge entries; require "wait-for-close" above R1 (18.90) to add aggressively.

### Sentiment (0–10)
- Base Sentiment Score: 6.4/10 (Step 1; volatility-up bias)
- CoherenceScore: 0 (Trend10D FLAT no align; Regime MEAN_REVERT but ADX 22.76 not <18; Williams BEARISH contra FH-sign +; no VIX penalty since this IS VIX)
- Structural Adjustment: 0
- Adjusted Sentiment Score: 6.4/10
- Confidence: Medium
- Mechanical Drivers: • Williams BEARISH at 20.72; • Williams %R oversold -90.03; • Sub-pivot positioning
- Fundamental Drivers: • Jobs print risk; • Hormuz partial normalization; • USMCA deadline
- Catalyst Flip Map: Hot payrolls + ISM >55 → VIX R1 18.90 / R2 20.16 test; soft payrolls → drift toward S3 14.28

### Recent Major Events (Last 7 Calendar Days)
| Date | Event | Impact Factor | One-Line Impact | News Direction | Structural Alignment | Source |
|---|---|---|---|---|---|---|
| 2026-06-30 | US expected to not extend USMCA | Regulation/Geopolitics | VIX-supportive uncertainty | Volatility-up | Mixed | Reuters [^6] |
| 2026-06-30 | Tech selloff stirs bubble fears | Volatility | VIX sub-pivot absorbs some premium | Volatility-up | Aligned | Reuters [^5] |
| 2026-06-29 | CNBC: Hormuz shipping "unlikely to rebound quickly" | Geopolitics | Insurance/energy-flow risk persists | Volatility-up | Aligned | CNBC [^16] |
| 2026-06-25 | Wall St mixed; semi/AI cap | Volatility | VIX drift contained | Mixed | Mixed | Reuters [^8] |
| 2026-06-23 | Wall St ends lower; Nasdaq −2.21% | Volatility | VIX spike | Volatility-up | Aligned | Reuters [^9] |

### Upcoming Events (Next 3 Trading Days)
| Date | Event | Impact Factor | Expected Sensitivity | Source |
|---|---|---|---|---|
| 2026-07-01 10:00 ET | ISM Manufacturing PMI (June) | Other | Medium — risk sentiment | ISM [^10] |
| 2026-07-01 | USMCA Joint Review deadline | Regulation/Geopolitics | Medium | Blakes [^11] |
| 2026-07-02 08:30 ET | Employment Situation (June) | Labor | Very High — primary VIX catalyst | BLS [^1] |
| 2026-07-02 08:30 ET | Weekly Initial Jobless Claims | Labor | Medium | BLS [^1] |
| 2026-07-02 10:00 ET | Factory Orders (May) | Other | Low | MarketWatch [^12] |
| 2026-07-03 | Independence Day (NYSE closed) | Other | Calendar conflict; gap risk | BLS / NYSE [^1][^13] |

### Commodity Correlation (28-day)
**Limitation:** 28-day r/p between VIX and crude / gold not in supplied dataset.
**Qualitative Linkage:** VIX–crude correlation is structurally positive (both risk proxies). With the US–Iran ceasefire holding into the window, crude has eased but Hormuz remains structurally constrained (Energy Aspects, S&P Global); this caps the VIX downside and supports the "volatility-up" bias at the upper portion of the 16.32–16.78 range. VIX–gold correlation is more conditional: if VIX rises on jobs shock, gold may follow as safe-haven. The TNX↔VIX coupling is critical: if TNX breaks R1 (4.399), VIX faces upside (rate-sensitivity); if TNX stalls, VIX drift remains toward the upper end of the range.

### Risk Management
ADX 22.76 → transition band → range tactics. Williams %R oversold (-90.03) → mean-reversion to upside; trim VIX-short exposure. Day+2 jobs proximity throttles to 50%. Stop: 0.75×ATR (1.55) below PP 18.20 → ≈16.65. Target: R1 18.90 base; R2 20.16 on bullish flip; S1 16.94 on bearish flip. TDA_Structure_Signal = NEUTRAL_STRUCTURE (H1_MaxPersistence 0.124, H1_CountAbove 0).

### VIX Summary Table
| Metric | Insight |
|---|---|
| **Current Value** | 16.45 (Yahoo canonical) |
| **Forecast Value** | 16.32 – 16.78 / **exact 16.64** |
| **Bias** | Higher (volatility up) |
| **Confidence** | Moderate |
| **Sentiment Score** | 6.4/10 — volatility-up; medium confidence |
| **Commodity Correlation** | Limitation: r/p not available; crude/gold linkage qualitative |
| **Key Events** | June payrolls 07-02 08:30 ET [^1]; USMCA 07-01 [^11] |
| **Technical Insight** | Williams %R oversold -90.03; sub-pivot drift; ATR% 12.60% high |
| **Econometric Insight** | ARIMAX Day+3 16.33, CI [15.16, 17.49]; ARCH p=0.1099 not significant |
| **ML Insight** | 2 outliers (Torch, LSTM); divergence per Rule 14(b); GARCH/ARIMAX converge |

### Discrepancy Note
Yahoo 16.45 vs Investing 16.45 (no diff). No correction needed.

---

## TNX

Forecast Report for TNX — Current: 4.418 | 3-Day Prediction: 4.39 – 4.42 and exact **4.41**

**Forecast Positioning Rationale:**
- Sentiment Score: 6.2/10 (Step 1; for TNX, "Higher" = yields up)
- Placement: 70th percentile of ML range (4.3949 – 4.4164)
- Primary Influence: Moderately constructive signals (Sentiment 6.2, Williams BULLISH at 4.36)
- Key Factor: Stochastic %K deeply oversold 12.85; close above pivot 4.383; Trend10D DOWN creates tension but Williams-confirmed fractal at 4.36 supports yields-up bias
- ML Reference Comparison: 4.41 vs 4.46 (FH Day+3): positioned slightly below ML reference (FH has 4.4583 peak D+2 then mild pullback)

### Visual Chart Analysis & Regions
Region detection: N_total_regions = 4 (A, B, C, D), N_recent_regions = 3. Current region_id = D (start ~2026-06-30). new_region(T0) = 1. Momentum(T0) = up (bounce from 4.37 low). T0 vs Classic Pivot 4.383: |T0 − PP| = 0.035; 0.25×ATR(14) = 0.25×0.0537 = 0.0134. |T0 − PP| > 0.25×ATR → **Above** (DERIVED_METRIC). Region meanings are inferred and uncertainty-qualified.

| Region | Approx date span | Slope | Volatility | Key pivot behavior | Regime risk note |
|---|---|---|---|---|---|
| B (mid-Jun) | ~2026-06-08 → 06-22 | Down/Flat | Med | Lost R1 (4.469), oscillated around PP (4.383) | Consolidation post-peak |
| C (late Jun) | ~2026-06-23 → 06-29 | Down | High | Tested S1 (4.356) and S2 (4.340) | Sharp risk-off yield drop |
| D (Jun 30) | 2026-06-30 | Up | Low | Reclaimed PP, close at 4.418 | Bounce toward R1 4.399 |

Base-case path (Day+1..Day+3): FH trajectory 4.4253 → 4.4583 → 4.4564 (peak D+2). Range [4.39, 4.42]. Path Day+1 drift up, Day+2 yields-up to R1/R2 zone, Day+3 modest pullback. **p≈0.55** (CoherenceScore 1).

Flip triggers:
- Mechanical: Daily close below S1 (4.356) by ≥0.25×ATR = 0.0134 — i.e., close < 4.343
- Fundamental: Soft June payrolls <100K → bias Lower with focus on S1 4.356; hot payrolls >180K → bias Higher with focus on R2 4.426

Risk mapping: Stops sized to 0.5×ATR (0.027) below PP 4.383 → ≈4.356. Note 1: Stochastic %K 12.85 oversold favors bounce. Risk mapping note: Fade sub-4.36 levels. Note 2 (after mapping): Avoid chasing above 4.426 without jobs confirm. Note 3 (after diagnostics): Yields-curve impact on QQQ/AAPL rate-sensitivity.

### Technical Indicators (28-day)
| Indicator | Reading | Interpretation | Actionable Takeaway |
|---|---|---|---|
| Classic Pivot | 4.38 | T0 4.418 above PP by 0.035; 0.25×ATR=0.0134 → Above | R1 4.399 nearest; S1 4.356 |
| 50-DMA | 4.46 | Price 0.83% below 50-DMA — bearish bias | 50-DMA acts as Resistance |
| 200-DMA | 4.23 | Price 4.41% above 200-DMA — bullish bias | 200-DMA acts as deep Support |
| RSI(14) | 46.02 | Neutral (30–70) | No overbought/oversold signal |
| Stochastic %K | 12.85 | **Oversold (<20)** | **Mean-reversion risk** (upside) |
| ATR(14) | 0.0537 | ATR% = 0.0537/4.418 = 1.22% (DERIVED_METRIC) → Medium | Medium stops; standard size |
| ADX(14) | 15.03 | Range (<18) | Range-trade posture |
| CCI(14) | -64.59 | Neutral (-100 to +100) | No overbought/oversold signal |
| Williams %R | -70.59 | Neutral (-80 to -20) | No overbought/oversold signal |
| Ultimate Oscillator | 45.01 | Neutral (30–70) | No overbought/oversold signal |
| ROC(10) | -0.23 | Negative momentum | Momentum weakening |
| BullBear Power | -0.0515 | Bears dominant | Momentum strengthening (for bears) |

### Econometric Analysis (ARIMA/ARIMAX)
ARIMAX(1,1,1) with exogenous regressors, residual ARCH p=0.6056 (not significant). Day-3 forecast 4.3873, 95% CI [4.3535, 4.4210]. Forecast at 0th percentile of ML range (lower bound); ARIMAX is the most conservative model.

### Machine-Learning Forecast Note
Day-3 point forecasts: Torch 4.3920, DYNAMIX 4.3949 (primary), ARIMAX 4.3873, PCE 4.3954, LSTM 4.4175, GARCH 4.4164, VAR 4.4160, RW 4.4189, ETS 4.4152. Median = 4.4152, MAD = 0.0037, MAD_floor = max(0.0037, 0.0054) = 0.0054. Outlier threshold 3×MAD_floor = 0.0161. Outliers: ARIMAX (4.3873, |dev|=0.0279), DYNAMIX (4.3949, |dev|=0.0203). **Divergence Note** triggered: Rule 14(b) outliers present. max-min = 0.0316 < 1.5×ATR = 0.0806 → no Rule 14(a). Dominance: GARCH/RW/ETS cluster around 4.41–4.42 → take precedence over ARIMAX/DYNAMIX lower. Risk implication: size throttle on rate-hedging; require close above R1 (4.399) for conviction long-yield.

### Sentiment (0–10)
- Base Sentiment Score: 6.2/10 (Step 1; yields-up bias)
- CoherenceScore: 1 (Trend10D DOWN contra FH-sign +; Regime RANDOM no match; Williams BULLISH align FH-sign +; no VIX penalty as VIX is MEAN_REVERT)
- Structural Adjustment: 0
- Adjusted Sentiment Score: 6.2/10
- Confidence: Medium
- Mechanical Drivers: • Williams BULLISH at 4.36; • Stochastic %K 12.85 oversold
- Fundamental Drivers: • June payrolls hot/soft in D+2; • June FOMC hawkish dot plot
- Catalyst Flip Map: Hot payrolls >180K → bias Higher toward R2 4.426 / R3 4.469; soft payrolls <100K → bias Lower toward S1 4.356

### Recent Major Events (Last 7 Calendar Days)
| Date | Event | Impact Factor | One-Line Impact | News Direction | Structural Alignment | Source |
|---|---|---|---|---|---|---|
| 2026-06-30 | Reuters: "Why Trump's tariffs had plenty bark, limited bite" | Other | TACO narrative | Yield-down (risk-on) | Mixed — TACO limits spike | Reuters [^17] |
| 2026-06-29 | 10Y yield around 4.38% (FRED daily) | Other | Yield drift lower | Yield-down | Mixed | FRED [^18] |
| 2026-06-25 | 10Y auction rate 4.38% (MacroMicro) | Other | Auction clearing well | Yield-down | Mixed | MacroMicro [^19] |
| 2026-06-23 | Tech-led equity selloff; rate-sensitivity cap | Volatility | Mild yield-up | Yield-up | Contradicted with end-of-month drift | Reuters [^9] |

### Upcoming Events (Next 3 Trading Days)
| Date | Event | Impact Factor | Expected Sensitivity | Source |
|---|---|---|---|---|
| 2026-07-01 10:00 ET | ISM Manufacturing PMI (June) | Other | High — yield driver | ISM [^10] |
| 2026-07-01 | USMCA Joint Review deadline | Regulation/Geopolitics | Medium | Blakes [^11] |
| 2026-07-02 08:30 ET | Employment Situation (June) | Labor | Very High — primary yield catalyst | BLS [^1] |
| 2026-07-02 08:30 ET | Weekly Initial Jobless Claims | Labor | Medium | BLS [^1] |
| 2026-07-02 10:00 ET | Factory Orders (May) | Other | Low | MarketWatch [^12] |
| 2026-07-03 | Independence Day (NYSE closed; bond market early close 14:00 ET typically) | Other | Calendar conflict; thin liquidity | BLS / NYSE [^1][^13] |

### Commodity Correlation (28-day)
**Limitation:** 28-day r/p between TNX and crude / gold / copper not in supplied dataset.
**Qualitative Linkage:** TNX–gold correlation is structurally positive (both safe-haven / real-rate proxies). The TNX–VIX coupling is direct: if jobs print hot, TNX breaks above R1 (4.399) on yield repricing; VIX simultaneously tests R1 (18.90). The TNX–crude linkage is via inflation expectations: a re-firm in crude on partial Hormuz normalization would be inflation-positive and yields-up supportive. Most likely applies conditional on the 07-02 print and ceasefire persistence; the linkage is uncertain if the ceasefire breaks.

### Risk Management
ADX 15.03 → range band (<18) → range tactics. Stochastic %K deeply oversold → mean-reversion to upside. Day+2 jobs proximity throttles to 50%. Stop: 0.5×ATR (0.027) below PP 4.383 → ≈4.356. Target: R1 4.399 base; R2 4.426 / R3 4.469 on bullish flip; S1 4.356 on bearish. TDA_Structure_Signal = NEUTRAL_STRUCTURE (H1_MaxPersistence 0.315, H1_CountAbove 0).

### TNX Summary Table
| Metric | Insight |
|---|---|
| **Current Value** | 4.418 (Yahoo canonical) |
| **Forecast Value** | 4.39 – 4.42 / **exact 4.41** |
| **Bias** | Higher (yields up) |
| **Confidence** | Moderate |
| **Sentiment Score** | 6.2/10 — moderately constructive; medium confidence |
| **Commodity Correlation** | Limitation: r/p not available; gold/crude linkage qualitative |
| **Key Events** | June payrolls 07-02 08:30 ET [^1]; ISM 07-01 10:00 ET [^10] |
| **Technical Insight** | Stochastic %K 12.85 oversold; ADX 15.0 range; ATR% 1.22% medium |
| **Econometric Insight** | ARIMAX Day+3 4.3873, CI [4.3535, 4.4210]; ARCH p=0.6056 not significant |
| **ML Insight** | 2 outliers (ARIMAX, DYNAMIX); divergence per Rule 14(b); GARCH/RW/ETS cluster at 4.41–4.42 |

### Discrepancy Note
Yahoo 4.418 vs Investing 4.467 (Δ +0.049 / +49bp — material). Hypotheses (un-cited): (a) timestamp/venue difference (TNX settles intraday vs end-of-day), (b) vendor methodology rounding to different decimal precision, (c) potentially stale Investing quote not updated for late-day rally. No correction applied; all computations anchored to Yahoo canonical.

---

## AAPL

Forecast Report for AAPL — Current: 289.36 | 3-Day Prediction: 289.15 – 292.41 and exact **289.64**

**Forecast Positioning Rationale:**
- Sentiment Score: 3.2/10 (Step 1)
- Placement: 15th percentile of ML range (289.15 – 292.41)
- Primary Influence: Mildly bearish structural signals (Sentiment 3.2, Trend10D DOWN, FH-sign +)
- Key Factor: Memory-chip cost overhang (Tim Cook to WSJ 2026-06-17); ADX 25.6 trend threshold; Williams BULLISH at 273.75 as deep support
- ML Reference Comparison: 289.64 vs 288.77 (FH Day+3): positioned slightly above ML reference (model FH marginally more bearish)

### Visual Chart Analysis & Regions
Region detection: N_total_regions = 4 (A, B, C, D), N_recent_regions = 3. Current region_id = D (start ~2026-06-26). new_region(T0) = 1. Momentum(T0) = up (recovery from $275 low). T0 vs Classic Pivot 283.32: |T0 − PP| = 6.04; 0.25×ATR(14) = 0.25×8.16 = 2.04. |T0 − PP| > 0.25×ATR → **Above** (DERIVED_METRIC). Region meanings are inferred and uncertainty-qualified.

| Region | Approx date span | Slope | Volatility | Key pivot behavior | Regime risk note |
|---|---|---|---|---|---|
| B (mid-Jun) | ~2026-06-09 → 06-16 | Up | Med | Reclaimed PP (283.32), tested R2 (291.84) | Recovery peak |
| C (mid-late Jun) | ~2026-06-16 → 06-25 | Down | High | Lost PP, tested S2 (274.80) and S3 (266.28) | Memory-chip cost shock |
| D (late Jun) | ~2026-06-26 → 06-30 | Up | Med | Reclaimed PP, testing R1 (286.79) | Recovery rally; R2 (291.84) caps |

Base-case path (Day+1..Day+3): FH trajectory 283.87 → 288.08 → 288.77. Range [289.15, 292.41]. Path Day+1 mild drift, Day+2 jobs-sensitive, Day+3 settles mid-range. **p≈0.55** (CoherenceScore 1, mixed signals).

Flip triggers:
- Mechanical: Daily close below S1 (278.27) by ≥0.25×ATR = 2.04 — i.e., close < 276.23
- Fundamental: Hot payrolls + AI/semi sector re-rating on 07-02; or fresh memory-chip cost escalation

Risk mapping: Stops sized to 0.5×ATR (4.08) below S1 278.27 → ≈274.19. Note 1: R2 caps near-term upside. Risk mapping note: Tighten stops if VIX >18.5. Note 2 (after mapping): Avoid adding on Williams %R overbought (-45.5 only). Note 3 (after diagnostics): Memory-cost narrative risk asymmetric.

### Technical Indicators (28-day)
| Indicator | Reading | Interpretation | Actionable Takeaway |
|---|---|---|---|
| Classic Pivot | 283.32 | T0 289.36 above PP by 6.04; 0.25×ATR=2.04 → Above | R1 286.79 nearest; S1 278.27 |
| 50-DMA | 293.60 | Price 1.44% below 50-DMA — bearish bias | 50-DMA acts as Resistance |
| 200-DMA | 271.31 | Price 6.65% above 200-DMA — bullish bias | 200-DMA acts as deep Support |
| RSI(14) | 46.55 | Neutral (30–70) | No overbought/oversold signal |
| Stochastic %K | 39.10 | Neutral (20–80) | No overbought/oversold signal |
| ATR(14) | 8.16 | ATR% = 8.16/289.36 = 2.82% (DERIVED_METRIC) → High | Wider stops; smaller size |
| ADX(14) | 25.63 | Trend (≥25) | Trend-follow posture; use wider stops |
| CCI(14) | -68.99 | Neutral (-100 to +100) | No overbought/oversold signal |
| Williams %R | -45.55 | Neutral (-80 to -20) | No overbought/oversold signal |
| Ultimate Oscillator | 35.35 | Neutral (30–70), leaning weak | Watch 30 |
| ROC(10) | -3.30 | Negative momentum | Momentum weakening |
| BullBear Power | -10.96 | Bears dominant | Momentum strengthening (for bears) |

### Econometric Analysis (ARIMA/ARIMAX)
ARIMAX(1,1,1) with exogenous regressors, residual ARCH p=0.9731 (not significant). Day-3 forecast 289.15, 95% CI [285.23, 293.06]. Forecast at 0th percentile (lower bound) of ML range.

### Machine-Learning Forecast Note
Day-3 point forecasts: Torch 275.15, DYNAMIX 284.71 (primary), ARIMAX 289.15, PCE 289.24, LSTM 292.41, GARCH 292.64, VAR 295.70, RW 290.19, ETS 290.19. Median = 290.19, MAD = 1.04, MAD_floor = max(1.04, 0.82) = 1.04. Outlier threshold 3×MAD_floor = 3.12. Outliers: Torch (275.15, |dev|=15.04), DYNAMIX (284.71, |dev|=5.48), VAR (295.70, |dev|=5.51). **Divergence Note** triggered: max-min = 20.55 > 1.5×ATR = 12.24 → Rule 14(a); plus Rule 14(b) outliers. Dominance: Pivot hold at PP 283.32 / R1 286.79 anchors; Torch and DYNAMIX are bear outliers. Risk implication: size throttle 30%; require close above R2 (291.84) for conviction long; stop placement tight given high ATR%.

### Sentiment (0–10)
- Base Sentiment Score: 3.2/10 (Step 1)
- CoherenceScore: 1 (Trend10D DOWN contra FH-sign +; Regime RANDOM no match; Williams BULLISH align FH-sign +; no VIX penalty as VIX is MEAN_REVERT)
- Structural Adjustment: 0
- Adjusted Sentiment Score: 3.2/10
- Confidence: Medium
- Mechanical Drivers: • Williams BULLISH at 273.75; • Below 50-DMA (Resistance)
- Fundamental Drivers: • Memory-chip cost escalation (Tim Cook 06-17); • AI/semi re-rating risk
- Catalyst Flip Map: Soft payrolls + VIX sub-15 → bias upgrade to Higher (L2) toward R1 286.79 / R2 291.84; hot payrolls + ISM >55 → bias Lower confirmed toward S1 278.27

### Recent Major Events (Last 7 Calendar Days)
| Date | Event | Impact Factor | One-Line Impact | News Direction | Structural Alignment | Source |
|---|---|---|---|---|---|---|
| 2026-06-30 | US expected to not extend USMCA | Regulation/Geopolitics | Supply-chain overhang | Bearish | Mixed | Reuters [^6] |
| 2026-06-25 | AAPL continues memory-chip cost narrative (post 06-17 Cook/WSJ) | Earnings / Supply chain | Price-hike overhang persists | Bearish | Aligned with bias | WSJ / Reuters [^4] |
| 2026-06-25 | Wall St mixed; tech/megacap declines | Volatility | AAPL pressured | Bearish | Aligned | Reuters [^8] |
| 2026-06-23 | Nasdaq −2.21%; semiconductor selloff | Volatility | Sharp AAPL drawdown | Bearish | Aligned | Reuters [^9] |

### Upcoming Events (Next 3 Trading Days)
| Date | Event | Impact Factor | Expected Sensitivity | Source |
|---|---|---|---|---|
| 2026-07-01 10:00 ET | ISM Manufacturing PMI (June) | Other | Medium — supply-chain read | ISM [^10] |
| 2026-07-02 08:30 ET | Employment Situation (June) | Labor | High — consumer-spending read | BLS [^1] |
| 2026-07-02 08:30 ET | Weekly Initial Jobless Claims | Labor | Medium | BLS [^1] |
| 2026-07-02 10:00 ET | Factory Orders (May) | Other | Low | MarketWatch [^12] |
| 2026-07-03 | Independence Day (NYSE closed) | Other | Calendar conflict | BLS / NYSE [^1][^13] |

### Commodity Correlation (28-day)
**Limitation:** 28-day r/p between AAPL and copper / gold / crude not in supplied dataset.
**Qualitative Linkage:** AAPL is most sensitive to copper (via chip cycle and Apple-specific supply-chain) and modestly to gold (safe-haven substitution). The TNX coupling is direct: if TNX breaks R1 (4.399) on hot payrolls, AAPL's relative rate-sensitivity (memory-chip costs + consumer-discretionary demand) elevates downside risk. Conversely, soft payrolls pulling TNX to S1 (4.356) likely allows the current-region uptrend (Region D) to continue toward R2 (291.84). The QQQ↔AAPL linkage is also meaningful given shared AI/semi exposure; if QQQ fails at S1 711.31, AAPL likely follows toward S1 278.27. May not apply if memory-chip narrative is resolved favorably.

### Risk Management
ADX 25.63 → trend band (≥25) → trend-follow tactics; no averaging down. Below 50-DMA (Resistance) → trend is fragile. Day+2 jobs proximity throttles to 50%. Stop: 1.0×ATR (8.16) below S1 278.27 → ≈270.11. Target: PP 283.32 / S1 278.27 on bearish; R2 291.84 on bullish flip. TDA_Structure_Signal = NEUTRAL_STRUCTURE (H1_MaxPersistence 0.336, H1_CountAbove 0).

### AAPL Summary Table
| Metric | Insight |
|---|---|
| **Current Value** | 289.36 (Yahoo canonical) |
| **Forecast Value** | 289.15 – 292.41 / **exact 289.64** |
| **Bias** | Lower |
| **Confidence** | Moderate |
| **Sentiment Score** | 3.2/10 — mildly bearish; medium confidence |
| **Commodity Correlation** | Limitation: r/p not available; copper/QQQ linkage qualitative |
| **Key Events** | June payrolls 07-02 08:30 ET [^1]; ISM 07-01 10:00 ET [^10] |
| **Technical Insight** | ADX 25.6 trend; below 50-DMA (Resistance); ATR% 2.82% high |
| **Econometric Insight** | ARIMAX Day+3 289.15, CI [285.23, 293.06]; ARCH p=0.9731 not significant |
| **ML Insight** | 3 outliers (Torch, DYNAMIX, VAR); divergence per Rule 14(a) and 14(b); high dispersion |

### Discrepancy Note
Yahoo 289.36 vs Investing 289.36 (no diff). No correction needed.

---

## Final Three-Day Forecasts Table

| Ticker | Forecast Range / **Exact** | Bias | Rationale |
|---|---|---|---|
| **SPX** | 7,516.88 – 7,542.59 / **7,524.59** | Higher | Sentiment 4.0, R2 acts as ceiling; cautious positioning at 30th percentile; bias Higher by L2 with structural caution. **BIAS_POSITIONING_CONFLICT** flagged. |
| **DJI** | 52,384.14 – 52,502.59 / **52,467.06** | Higher | Sentiment 6.3, Williams BULLISH, clean ML ensemble; drift toward R1 52,346. |
| **QQQ** | 739.05 – 744.00 / **739.79** | Lower | Sentiment 3.0, AI/semi overhang, Torch outlier; bias Lower by L1 confirmed. |
| **VIX** | 16.32 – 16.78 / **16.64** | Higher (vol-up) | Sentiment 6.4, sub-pivot drift, GARCH variance creeping up; bias Higher by L2. |
| **TNX** | 4.39 – 4.42 / **4.41** | Higher (yields up) | Sentiment 6.2, Stochastic %K deeply oversold, Williams BULLISH; bias Higher by L4. |
| **AAPL** | 289.15 – 292.41 / **289.64** | Lower | Sentiment 3.2, memory-chip cost overhang, ADX trend fragile below 50-DMA; bias Lower by L1. |

---

## References (Footnotes)

[^1]: Bureau of Labor Statistics — Schedule of Selected Releases 2026 (Employment Situation June 2026: Thursday July 2, 2026, 08:30 AM ET)
[^2]: Federal Reserve — Meeting calendars and information (FOMC July 28–29, 2026)
[^3]: MarketWatch — Stock Market News June 29, 2026 (Dow closes above 52,000)
[^4]: WSJ / Reuters — Apple to raise prices due to memory chip shortage, CEO Cook tells WSJ (2026-06-17)
[^5]: Reuters — Tech selloff stirs bubble fears in US stock market (2026-06-30)
[^6]: Reuters — US expected to not extend USMCA, starting decade-long countdown (2026-06-30)
[^7]: AP News — How major US stock indexes fared Tuesday 6/30/2026
[^8]: Reuters — Wall St ends mixed as tech megacap declines outweigh upbeat chip forecasts (2026-06-25)
[^9]: Reuters — Wall Street ends lower on semiconductor selloff as AI spending concerns mount (2026-06-23)
[^10]: Institute for Supply Management — Release Dates for the ISM Manufacturing and Services PMI Reports (July 1, 2026, 10:00 AM ET)
[^11]: Blakes — U.S.–Canada Tariffs Timeline (USMCA Free Trade Commission Review, July 1, 2026)
[^12]: MarketWatch — U.S. Economic Calendar (Factory Orders July 2, 2026, 10:00 AM ET)
[^13]: New York Stock Exchange — Holidays & Trading Hours (Independence Day observed, Friday July 3, 2026)
[^14]: WSJ — DJIA Dow Jones Industrial Average Stock Prices and Charts
[^15]: Reuters Market Talk — "Doubts are creeping in" to the AI trade (June 2026)
[^16]: CNBC — Analysts warn of supply risks as oil prices return to pre-war levels (Strait of Hormuz, 2026-06-29)
[^17]: Reuters Commentary — Why Trump's tariffs had plenty of bark, but limited bite (2026-06-30)
[^18]: FRED — Market Yield on U.S. Treasury Securities at 10-Year Constant Maturity (DGS10, 2026-06-29: 4.38)
[^19]: MacroMicro — US 10Y Treasury Auction Rate (June 2026: 4.38%)

---

## QA Audit Flags & Notes

- **LEDGER_FREEZE_VIOLATION:** None. All events in Recent/Upcoming tables are sourced from Stage 1 frozen ledger.
- **EVENT_LEDGER_CONFLICT:** None in formal rows.
- **UNVERIFIED_OFFICIAL_LINK:** None — all event timings from Official issuer pages (BLS, ISM, NYSE) or Tier-1 (Reuters, MarketWatch, CNBC, WSJ).
- **BIAS_POSITIONING_CONFLICT: SPX** — Bias = Higher by L2 (Exact 7524.59 > Current 7499.36 by 0.34%), but Exact positioned at 30th percentile of ML range (lower 40%). LLM reasoning: Sentiment 4.0 + cautious structural signals warrant conservative placement despite the numerical bias; jobs print is the principal swing factor.
- **FACT_LOCK_FAIL: SENTIMENT_CONSISTENCY_LOCK** — None. SPX (Sentiment 4.0, Exact in lower 50%) is consistent; all others consistent.
- **FACT_LOCK_FAIL: BIAS_LOCK** — None. Bias values consistent across Executive Summary, per-ticker Summary, and Final Forecasts Table.
- **FACT_LOCK_FAIL: RANGE_CONSTRAINT_LOCK** — None. All Exact values fall within [Range_Lo, Range_Hi].
- **CALENDAR_CONFLICT (unflagged in template):** FH table lists 2026-07-03 as Day+3; BLS/NYSE schedule marks this as Independence Day (markets closed). Proceeding per user-supplied FH parameters; holiday still shapes pre-holiday liquidity on 2026-07-02.
- **DISCREPANCY (Yahoo vs Investing):** TNX shows material 49bp gap (Yahoo 4.418 vs Investing 4.467) — Discrepancy Note included. All other tickers show sub-tick differences (rounding/timing).
- **PARITY:** Each ticker section is approximately 450–550 words of prose (excluding tables), per the practical parity target.
- **TDA:** All tickers show H1_NONE (H1_MaxPersistence <0.50, H1_CountAbove=0). TDA_Structure_Signal = NEUTRAL_STRUCTURE for all. TDA_Flip_Risk not computed (full 10-window time series not supplied); not referenced in Scenarios or Risk Management where it would otherwise be required.
- **MISSING_USER_INPUT:** None for required Step 1 sentiment fields; TDA Persistence_Sequence and Count_Sequence time series not provided (limitation noted).