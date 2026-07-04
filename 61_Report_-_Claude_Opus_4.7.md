# Market Forecast Report: 3-Day Outlook (Jul 01–03, 2026)

**Analysis Date:** June 30, 2026
**Forecast Period:** 2026-07-01, 2026-07-02, 2026-07-03 (ET)
**Team Lead:** Multi-disciplinary Financial Analysis Panel
**Timezone Note:** Event times are in ET; user local time: Europe/Zagreb.

> Determinism notes (read once): Regime ∈ {RANDOM, MEAN_REVERT} for all six tickers, so the Range Builder resolves to **[P25, P75]** of the available Day-3 model points for every ticker. Exact placement is sentiment-anchored within that range. TDA_CONTEXT is present, so **TDA_AVAILABLE = true**; however every ticker is H1_NONE (H1_CountAbove = 0, H1_MaxPersistence < 0.50), so TDA_Structure_Signal = NEUTRAL_STRUCTURE (QQQ = DISTRIBUTED_CYCLES, Entropy 2.80 > 2.50) and TDA_Flip_Risk = LOW (cycle count stable at 0). Step 1 (Part 1 sentiment package) supplied per-ticker **Adjusted/Final** sentiment scores and a uniform **Medium** confidence; it did not decompose Base vs Structural Adjustment, so those two fields are flagged **MISSING_USER_INPUT** and the Adjusted Final Score is consumed directly. CoherenceScore is computed locally (Stage 4) for deterministic downstream rules only.

---

## 2) Executive Summary & Final Forecasts

| Ticker | Current Value | Forecast Range<br>---<br>**Exact** | Bias<br>---<br>Projection | Rationale |
| --- | --- | --- | --- | --- |
| **SPX** | 7499 | 7517–7543<br>---<br>**7525** | Higher<br>---<br>Constructive but capped; advancing toward the 7543 ML ceiling | ML ensemble floors above spot; sentiment 4.0 holds Exact low-in-range (30th pct). Key risk: hot payrolls 07-02 + AI-bubble fragility.[^6] `BIAS_POSITIONING_CONFLICT: SPX` |
| **DJI** | 52319 | 52384–52503<br>---<br>**52467** | Higher<br>---<br>Constructive bias; advancing toward 52503 (R2 52510) | Cleanest uptrend; RSI 65.7, Williams BULLISH, sentiment 6.3 places Exact upper-range (70th pct). Risk: labor repricing, USMCA trade overhang.[^7] |
| **QQQ** | 736.40 | 739.05–744.00<br>---<br>**739.79** | Lower<br>---<br>Defensive posture; downside pressure despite ML floor above spot | Sentiment 3.0 (≤3) dominates → Lower; DISTRIBUTED_CYCLES + AI/semis valuation risk.[^6][^10] Exact pinned to range floor (15th pct). |
| **VIX** | 16.45 | 16.32–16.78<br>---<br>**16.64** | Higher<br>---<br>Upside trajectory in volatility; advancing toward 16.78 | Sentiment 6.4 (vol-up), MEAN_REVERT regime; pre-payrolls, pre-holiday positioning. Exact upper-range (70th pct), aligned with ML central tendency. |
| **TNX** | 4.42 | 4.39–4.42<br>---<br>**4.41** | Higher<br>---<br>Yields biased higher (yields-up); constructive into payrolls | Sentiment 6.2, Williams BULLISH aligns FH-up; ML range sits marginally below spot. Most catalyst-sensitive to 07-02 payrolls.[^1] |
| **AAPL** | 289.36 | 289.15–292.41<br>---<br>**289.64** | Higher<br>---<br>Nominally higher (Current>PP) but conservatively positioned | Tie-break to pivot (Level 4) yields Higher, but sentiment 3.2 + Trend10D DOWN hold Exact at 15th pct. `BIAS_POSITIONING_CONFLICT: AAPL` |

`BIAS_POSITIONING_CONFLICT: SPX` — Bias determined Higher by Level 2 (Exact 7525 > Current 7499 by +0.34%, because the ML range floors above spot), but Exact is positioned at the 30th percentile (lower-40%) of range due to the cautious Step-1 sentiment of 4.0, FH_sign negative (Day1→Day3 down), and the 2026-06-29 RANDOM→MEAN_REVERT regime change.

`BIAS_POSITIONING_CONFLICT: AAPL` — Bias determined Higher by Level 4 (Current 289.36 > Classic Pivot 283.32), but Exact is positioned at the 15th percentile (lower-40%) of range due to bearish Step-1 sentiment 3.2, Trend10D DOWN, and the 2026-06-25 RANDOM→MEAN_REVERT regime change.

`MISSING_USER_INPUT: Base_Sentiment_Score (all tickers)` · `MISSING_USER_INPUT: Structural_Adjustment (all tickers)` — Step 1 supplied only the Adjusted/Final score per ticker.

---

## 3) Current Stock Market Environment, Risks, and Policies

**Structural Market Health Assessment**
> Explanation: Across all six instruments the short-window Hurst regime is RANDOM or MEAN_REVERT, indicating the near-term tape is consolidative rather than persistently trending; longer H120 lookbacks lean PERSISTENT, so the broad backdrop is constructive while the immediate window is choppy.
> Comment #1: Five of six tickers logged an SVL regime change within the last 10 sessions (SPX 06-29 RANDOM→MEAN_REVERT, QQQ 06-29 RANDOM→MEAN_REVERT, AAPL 06-25 RANDOM→MEAN_REVERT, VIX 06-17 RANDOM→MEAN_REVERT, TNX 06-30 MEAN_REVERT→RANDOM), which may reflect elevated transition risk rather than a clean directional setup.
> Comment #2: TDA returns H1_NONE for every ticker (no cycle persistence above 0.50), so topology adds no structural conviction; risk posture should default to ATR/ADX mechanics.
> Comment #3: ADX is sub-trend or transitional for most names (TNX 15.0 range; QQQ 19.0, SPX 21.6, VIX 22.8, DJI 24.0 transitional; only AAPL 25.6 is technically "trend"), consistent with range tactics over trend-following.
> Comment #4: The user-supplied Fear & Greed reading of 31 (Fear) diverges from firm index price action into 06-30, a divergence that could be interpreted as crowded-but-anxious positioning.

**Policy and Event Backdrop into the Holiday Window**
> Explanation: The +3-day window is dominated by labor data, not a Fed decision; the June Employment Situation prints Thursday 2026-07-02 at 08:30 ET, and the NYSE is closed Friday 2026-07-03 for Independence Day observed.[^1][^5]
> Comment #1: ADP private payrolls and the ISM Manufacturing PMI land Wednesday 2026-07-01, front-running the official report and capable of shifting rate expectations early.[^3][^4]
> Comment #2: The next FOMC meeting is 2026-07-28/29, outside this window, so the tape is driven by labor-data repricing rather than a same-window policy move.[^11]
> Comment #3: Trade-policy headlines (US expected not to extend USMCA; tariff "bark vs bite" commentary) form a contextual overhang most relevant to DJI industrials.[^7][^8]
> Comment #4: Pre-holiday, half-staffed liquidity into 07-02 can amplify any payrolls surprise, a condition that likely argues for smaller size and wider confirmation.

---

## 4) Key Cross-Asset Insights and Overarching Themes

**Rate-Sensitivity Coupling (TNX ↔ Equities)**
> Explanation: TNX carries a yields-higher bias (Bias = Higher; FH Day1→Day3 rising; Williams BULLISH aligned), which mechanically pressures rate-sensitive equities.
> Comment #1: If TNX prints an upper-tilted range or a close above R2 4.43 on hot payrolls, then downside/rate-sensitivity risk for QQQ, AAPL, and SPX increases and position sizing in those names should throttle.
> Comment #2: If TNX instead closes below PP 4.38 on soft payrolls, then a constructive equity bias is permitted unless VIX contradicts.
> Comment #3: Coherence Note — TNX up-yield AND AAPL nominally bullish (Higher) co-exist, so AAPL's upside is explicitly rate-contingent and should be treated as the lower-conviction long.

**Volatility Coupling (VIX ↔ Equities)**
> Explanation: VIX carries a volatility-higher bias (Bias = Higher; FH rising), which downgrades equity confidence by one notch absent strong bullish structural alignment.
> Comment #1: If VIX closes above PP 18.20, then equity confidence (SPX, DJI, QQQ, AAPL) is cut one notch and defensive tactics dominate into the holiday.
> Comment #2: If VIX fades below S1 16.94, then an equity confidence upgrade is permitted where SVL signals align (DJI is the best-aligned candidate).
> Comment #3: Coherence Note — equity-bullish (DJI, SPX Higher) AND VIX-up co-exist, so index upside is flagged as occurring into rising implied volatility, a fragile combination.
> Comment #4: VIX MEAN_REVERT with price below its 50-DMA (17.68) and 200-DMA (18.72) suggests mean-reversion pressure upward toward the pivot zone is structurally plausible but not high-conviction.

---

## 5) Scenario Analysis

| Scenario | Description | Probability (%) | Structural Conditions (SVL/TDA) | News Catalyst Needed | Asset Implications |
| --- | --- | --- | --- | --- | --- |
| **Goldilocks payrolls** | June payrolls soft-but-not-recessionary; yields ease, equities firm into the holiday | 40 | SVL regimes RANDOM/MEAN_REVERT (consolidative); TDA H1_NONE (no cycle conviction); DJI Williams BULLISH | Soft June Employment Situation, 07-02 08:30 ET[^1] | SPX/DJI grind up to R-zone; QQQ stabilizes off floor; AAPL holds PP; TNX eases toward PP 4.38; VIX fades toward S1 |
| **Hot payrolls / rate shock** | Hot payrolls lift yields; rate-sensitive AI/tech sells off again | 35 | SPX/QQQ 06-29 regime change to MEAN_REVERT (fragile); AAPL Trend10D DOWN; TDA adds no cushion (H1_NONE) | Hot June Employment Situation + firm ADP/ISM, 07-01/07-02[^1][^3][^4] | TNX breaks R2 4.43; QQQ/AAPL lead lower; SPX fades to PP 7411; DJI relatively resilient; VIX pops above PP 18.20 |
| **Pre-holiday drift** | Thin liquidity; muted ranges; no decisive catalyst surprise | 25 | All ADX sub-trend/transitional (range tactics); MEAN_REVERT bias supports chop | None required (in-line data) | All six pin near pivots; VIX range-bound 16–17; TNX holds 4.39–4.42; indices oscillate within ML ranges |

Probabilities sum to 100.

---

## SPX

Forecast Report for SPX — Current: 7499 | 3-Day Prediction: 7517–7543 and exact **7525**

### Forecast Positioning Rationale
**Forecast Positioning Rationale:**
• Sentiment Score: 4.0/10 (Adjusted Final Score from Step 1; Base + Structural Adjustment `MISSING_USER_INPUT`; local CoherenceScore 0)
• Placement: 30th percentile of ML range (7517 – 7543)
• Primary Influence: Neutral-to-cautious structural signals (Trend10D FLAT, RANDOM→MEAN_REVERT 06-29)
• Key Factor: Entire ML ensemble floors above spot, but cautious sentiment 4.0 holds Exact low-in-range; FH_sign negative (Day1 pop then fade)
• ML Reference Comparison: 7525 vs 7456 (FH_Day3): positioned above ML central tendency due to the elevated P25–P75 band, while remaining low within that band

### Visual Chart Analysis & Regions
Region detection summary: N_total_regions = 2 distinct colored spans (Region 1 tan ≈ Jun 01–11; Region 2 blue ≈ Jun 11–30); N_recent_regions = 2 (both shown). Current region_id(T0) = Region 2; new_region(T0) = 0 (Region 2 began > 3 trading days ago). Momentum(T0) = up/flat (last segment rises into 7499). Pivot interaction: T0 Above PP — |7499 − 7411| = 88.15 > 0.25×ATR = 23.30 (DERIVED_METRIC: 0.25×93.21).

| Region | Approx date span | Slope | Volatility | Key pivot behavior | Regime risk note |
| --- | --- | --- | --- | --- | --- |
| Region 1 | Jun 01–11 (approx) | Down | High | Rejected R3, broke to S2/S1 trough | Early-window stress flush |
| Region 2 | Jun 11–30 (approx) | Up | Med | Reclaimed PP, capped near R2 7507 | RANDOM→MEAN_REVERT 06-29 |

Note #3: Price retook the pivot but stalls under R2.

Base-case path (p≈0.45; CoherenceScore 0, momentum up contradicts FH-down): Day+1 pop toward the 7517–7543 band (FH 7544), then Day+2/Day+3 fade toward PP 7411 / R1 7474 as FH rolls to 7456; Exact 7525 sits inside the upper ML band.

Flip triggers:
- Mechanical: a daily close above R1 7474 by ≥ 0.25×ATR (≥ 23.3 pts) confirms upside continuation; a close below S1 7378 by the same margin flips bearish.
- Fundamental: June Employment Situation, 2026-07-02 08:30 ET.[^1]

Note #1: Cautious tone meets a model floor above spot.

Risk mapping: anchor longs above PP 7411 with stops near S1 7378 and trim into R2 7507, sizing to ATR 93.

Note #2: Keep size modest into Thursday payrolls.

Visual limitation: region meanings are inferred from colored spans and are uncertainty-qualified.

### Technical Indicators (28-day)

| Indicator | Reading | Interpretation | Actionable Takeaway |
| --- | --- | --- | --- |
| Classic Pivot | 7411 | Above PP; |7499−7411|=88.15 > 0.25×ATR=23.30 (DERIVED_METRIC) | Target R1 7474 / R2 7507 |
| 50-DMA | 7395 | Current above → bullish bias | 50-DMA as support |
| 200-DMA | 6948 | Current above → bullish bias | 200-DMA as deep support |
| RSI(14) | 55.94 | 30–70 neutral | No overbought/oversold signal |
| Stochastic %K | 55.59 | 20–80 neutral | No overbought/oversold signal |
| ATR(14) | 93.21 | Volatility input | Size stops to ~93 pts |
| ATR% | 1.24% | ATR%=93.21/7499.36=1.24% → Medium (1.00–2.00%) (DERIVED_METRIC) | Standard stop width |
| ADX(14) | 21.64 | 18–25 transition | Mixed range/trend posture |
| CCI(14) | 48.72 | −100…+100 neutral | No overbought/oversold signal |
| Williams %R | −24.50 | −80…−20 neutral | No overbought/oversold signal |
| Ultimate Oscillator | 49.36 | 30–70 neutral | No overbought/oversold signal |
| ROC(10) | −0.16 | Negative momentum (sign) | Momentum weakening slightly |
| BullBear Power | 82.18 | >0 bulls dominant | Bull control, fading momentum |

### Econometric Analysis (ARIMA/ARIMAX)
ARIMAX selected p,d,q = (1,1,1) with configured exogenous regressors. The residual ARCH test p-value is 0.2053 → Not Significant, so conditional heteroskedasticity is not flagged and the ARIMAX mean model is treated as adequate. The user-supplied Day-3 ARIMAX forecast is 7526.37 with 95% CI [7472.76, 7579.98]. No recomputation performed; values quoted as ground truth.

### Machine-Learning Forecast Note (no averaging)
Day-3 points (as provided): Torch 7357.49; DYNAMIX 7623.73 (alt path 7449.87); ARIMAX 7526.37; PCE 7542.59; LSTM 7540.75; GARCH 7546.39; VAR 7481.73; RW 7519.39; ETS 7516.88. Median = 7526.37, MAD = 16.22, MAD_floor = max(16.22, 0.10×ATR=9.32) = 16.22 (DERIVED_METRIC). Outliers (|Pi−m| ≥ 3×MAD_floor=48.66): **Torch (low)** and **DYNAMIX (high)**. Divergence Note: dispersion 266.24 ≥ max(1.5×ATR=139.82, 4×MAD_floor=64.88) → wide. Outliers Torch/DYNAMIX bracket the cluster; dominance condition = a close above R1 7474 favors the high cluster, a close below S1 7378 favors Torch; risk implication = wait-for-close given ADX 21.6 transitional. No averaging applied.

### Sentiment (0–10)
- Base Sentiment Score: `MISSING_USER_INPUT` (Step 1 supplied Adjusted only)
- CoherenceScore: 0 (Trend10D align 0 [FLAT vs FH-down]; Regime-ADX align 0 [RANDOM]; Williams align 0 [BULLISH vs FH-down]; VIX penalty 0 [VIX not PERSISTENT])
- Structural Adjustment: `MISSING_USER_INPUT` (cap ±2 with TDA available; not exceeded)
- Adjusted Sentiment Score: 4.0/10
- Confidence: Medium → downgraded to **Low–Medium** (VIX-up and TNX-up couplings)
- Mechanical Drivers: price above PP/50-DMA/200-DMA; RSI neutral 55.9; ML floor above spot
- Fundamental Drivers: June payrolls 07-02; AI-bubble/valuation fragility[^6][^10]; pre-holiday liquidity
- Catalyst Flip Map: Hot payrolls (07-02 08:30 ET) → yields up → close below S1 7378 flips bearish; soft payrolls + close above R1 7474 confirms upside.[^1]

Rate-sensitivity clause: TNX's yields-higher bias raises SPX downside risk if R2 4.43 breaks on hot data.

### Recent Major Events (Last 7 Calendar Days)

| Date | Event | Impact Factor | One-Line Impact | News Direction | Structural Alignment | Source |
| --- | --- | --- | --- | --- | --- | --- |
| 2026-06-23/24 | AI/tech selloff, bubble fears | Volatility | Nasdaq −2.2%, S&P −1.4% on AI-capex + hawkish-Fed worry | Negative | Mixed — matches MEAN_REVERT shift, not FLAT trend | [^6][^10] |
| 2026-06-30 | Chicago Business Barometer / Case-Shiller | Other | Minor month-end macro; limited index impact | Neutral | Aligned — consolidative RANDOM tape | [^9] `UNVERIFIED_OFFICIAL_LINK` |

### Upcoming Events (Next 3 Trading Days)

| Date | Event | Impact Factor | Expected Sensitivity | Source |
| --- | --- | --- | --- | --- |
| 2026-07-01 | ISM Manufacturing PMI (June); ADP private payrolls | Labor | Medium — early read on labor/factory momentum | [^3][^4] `UNVERIFIED_OFFICIAL_LINK` (ADP time) |
| 2026-07-02 08:30 ET | June Employment Situation (nonfarm payrolls) | Labor | High — primary SPX catalyst, rate-repricing | [^1] |
| 2026-07-03 | NYSE closed (Independence Day observed) | Other | None — market holiday | [^5] |

### Commodity Correlation (28-day)
**Limitation:** No commodity price series (e.g., WTI, gold, copper) was supplied in the user data, so a 28-day Pearson r and p-value cannot be computed without recomputation, which is prohibited.
**Qualitative Linkage:** SPX direction over the window is likely conditional on rates and volatility rather than commodities directly; a TNX move above R2 4.43 may pressure index multiples, while a VIX close above PP 18.20 would likely coincide with broad de-risking. Energy-flow risk tied to Hormuz remains an uncertain tail that could transmit through both oil and VIX. These linkages are conditional and uncertainty-qualified.

### Risk Management
ADX 21.64 → transitional: blend range and trend tactics. Anchor longs above PP 7411; standard stop ≈ PP − 1.0×ATR (TDA NEUTRAL_STRUCTURE, no tightening justified); first target R1 7474, second R2 7507. TDA_Flip_Risk = LOW → fundamental (payrolls) triggers outweigh mechanical ones; require a confirmed close for pivot breaks. Event-proximity throttle: cut size into 07-02 08:30 ET and avoid fresh risk on the 07-03 holiday. No averaging down.

### SPX Summary Table

| **Metric** | **Insight** |
| --- | --- |
| **Current Value** | 7499 |
| **Forecast Value** | 7517–7543 / **7525** |
| **Bias** | Higher (with `BIAS_POSITIONING_CONFLICT`) |
| **Confidence** | Low–Moderate |
| **Sentiment Score** | 4.0/10 — cautious; ML floor above spot |
| **Commodity Correlation** | Limitation (no series supplied) |
| **Key Events** | June payrolls 07-02[^1]; AI selloff[^6] |
| **Technical Insight** | Above all pivots/MAs; oscillators neutral |
| **Econometric Insight** | ARIMAX(1,1,1) 7526.37; ARCH not significant |
| **ML Insight** | Wide divergence; Torch/DYNAMIX outliers bracket cluster |

---

## DJI

Forecast Report for DJI — Current: 52319 | 3-Day Prediction: 52384–52503 and exact **52467**

### Forecast Positioning Rationale
**Forecast Positioning Rationale:**
• Sentiment Score: 6.3/10 (Adjusted Final Score from Step 1; Base + Structural Adjustment `MISSING_USER_INPUT`; local CoherenceScore 0)
• Placement: 70th percentile of ML range (52384 – 52503)
• Primary Influence: Constructive structural signals (RSI 65.7, Williams BULLISH, strongest uptrend of the set)
• Key Factor: Cleanest +3-day model cluster and uptrend; sentiment 6.3 places Exact upper-range
• ML Reference Comparison: 52467 vs 52545 (FH_Day3): positioned below ML central tendency to respect the P75 cap and event risk

### Visual Chart Analysis & Regions
Region detection summary: N_total_regions = 2 (Region 1 tan ≈ Jun 01–17; Region 2 blue ≈ Jun 17–30); N_recent_regions = 2. Current region_id(T0) = Region 2; new_region(T0) = 0. Momentum(T0) = up (steady higher-lows into 52319). Pivot interaction: Above PP — |52319 − 52148| = 171.23 > 0.25×ATR = 146.46 (DERIVED_METRIC: 0.25×585.84).

| Region | Approx date span | Slope | Volatility | Key pivot behavior | Regime risk note |
| --- | --- | --- | --- | --- | --- |
| Region 1 | Jun 01–17 (approx) | Up (V-recovery) | High | Held S3, reclaimed PP from 49.9k trough | Volatile base-building |
| Region 2 | Jun 17–30 (approx) | Up | Low | Higher-lows above S2/S1, nears R1/R2 | Stable RANDOM, no regime change |

Note #3: Steadiest trend and lowest late-window volatility of the six.

Base-case path (p≈0.45; CoherenceScore 0, momentum up contradicts marginally-down FH): Day+1 toward FH 52572 and the R1 52346 / R2 52510 shelf, then a flat-to-mild fade to FH 52545; Exact 52467 sits between R1 and R2.

Flip triggers:
- Mechanical: a daily close above R2 52510 by ≥ 0.25×ATR (≥ 146.5) extends the advance; a close below PP 52148 by the same margin flips defensive.
- Fundamental: June Employment Situation, 2026-07-02 08:30 ET.[^1]

Note #1: Best-aligned uptrend, but the model edge is small.

Risk mapping: anchor longs above PP 52148 with stops ≈ PP − 1.0×ATR and scale out into R2 52510, sizing to ATR 586.

Note #2: Trade with the trend but respect payrolls risk.

Visual limitation: region meanings are inferred from colored spans and are uncertainty-qualified.

### Technical Indicators (28-day)

| Indicator | Reading | Interpretation | Actionable Takeaway |
| --- | --- | --- | --- |
| Classic Pivot | 52148 | Above PP; |52319−52148|=171.23 > 0.25×ATR=146.46 (DERIVED_METRIC) | Target R1 52346 / R2 52510 |
| 50-DMA | 50494 | Current above → bullish bias | 50-DMA as support |
| 200-DMA | 48491 | Current above → bullish bias | 200-DMA as deep support |
| RSI(14) | 65.67 | 30–70 neutral (upper) | No overbought/oversold signal |
| Stochastic %K | 80.62 | >80 overbought | Mean-reversion risk (downside) |
| ATR(14) | 585.84 | Volatility input | Size stops to ~586 pts |
| ATR% | 1.12% | ATR%=585.84/52319.20=1.12% → Medium (DERIVED_METRIC) | Standard stop width |
| ADX(14) | 23.98 | 18–25 transition | Mixed range/trend posture |
| CCI(14) | 125.47 | >+100 overbought | Mean-reversion risk (downside) |
| Williams %R | −12.54 | >−20 overbought | Mean-reversion risk (downside) |
| Ultimate Oscillator | 46.68 | 30–70 neutral | No overbought/oversold signal |
| ROC(10) | 0.61 | Positive momentum (sign) | Momentum strengthening |
| BullBear Power | 952.29 | >0 bulls dominant | Strong bull control |

### Econometric Analysis (ARIMA/ARIMAX)
ARIMAX selected p,d,q = (1,1,1) with exogenous regressors. Residual ARCH test p-value 0.0909 → Not Significant; GARCH not required for the mean residuals. Day-3 ARIMAX forecast 52502.59, 95% CI [52177.97, 52827.21]. Quoted as ground truth; no recomputation.

### Machine-Learning Forecast Note (no averaging)
Day-3 points: Torch 51920.62; DYNAMIX 52702.39 (alt 52633.47); ARIMAX 52502.59; PCE 52311.56; LSTM 52560.89; GARCH 52496.18; VAR 52384.14; RW 52433.01; ETS 52419.68. Median = 52433.01, MAD = 69.58, MAD_floor = max(69.58, 0.10×ATR=58.58) = 69.58 (DERIVED_METRIC). Outliers (≥ 3×MAD_floor=208.74): **Torch (low)** and **DYNAMIX (high)**. Divergence Note: dispersion 781.77; though below the 1.5×ATR=878.76 wide-gate, the two MAD-outliers trigger Rule 14(b). Dominance condition = close above R2 52510 favors the high cluster; risk implication = throttle size into payrolls. No averaging.

### Sentiment (0–10)
- Base Sentiment Score: `MISSING_USER_INPUT`
- CoherenceScore: 0 (Trend10D align 0 [FLAT vs FH-down]; Regime-ADX align 0 [RANDOM]; Williams align 0 [BULLISH vs FH-down]; VIX penalty 0)
- Structural Adjustment: `MISSING_USER_INPUT` (cap ±2; not exceeded)
- Adjusted Sentiment Score: 6.3/10
- Confidence: Medium → held at **Medium** (best structural alignment; coupling downgrade offset by trend strength)
- Mechanical Drivers: above all pivots/MAs; RSI 65.7; BullBear Power +952; higher-lows
- Fundamental Drivers: labor data 07-02; USMCA non-extension / tariff overhang for industrials[^7][^8]
- Catalyst Flip Map: Close above R2 52510 post-payrolls extends; close below PP 52148 flips defensive.[^1]

Rate-sensitivity clause: a TNX break above R2 4.43 would temper DJI upside via cyclical/rate channels.

### Recent Major Events (Last 7 Calendar Days)

| Date | Event | Impact Factor | One-Line Impact | News Direction | Structural Alignment | Source |
| --- | --- | --- | --- | --- | --- | --- |
| 2026-06-30 | US expected not to extend USMCA | Geopolitics | Decade-long countdown for the trade pact; industrials overhang | Negative | Mixed — contextual, not yet in price trend | [^7] |
| 2026-06-30 | Tariff "bark vs limited bite" commentary | Geopolitics | Frames tariff risk as headline-heavy, impact-light | Neutral | Aligned — consistent with steady RANDOM tape | [^8] |

### Upcoming Events (Next 3 Trading Days)

| Date | Event | Impact Factor | Expected Sensitivity | Source |
| --- | --- | --- | --- | --- |
| 2026-07-01 | ISM Manufacturing PMI (June); ADP payrolls | Labor | Medium — cyclicals/industrials read | [^3][^4] `UNVERIFIED_OFFICIAL_LINK` (ADP time) |
| 2026-07-02 08:30 ET | June Employment Situation | Labor | High — labor-sensitive Dow components | [^1] |
| 2026-07-03 | NYSE closed (Independence Day observed) | Other | None — market holiday | [^5] |

### Commodity Correlation (28-day)
**Limitation:** No commodity series supplied; a 28-day r/p is not computable without prohibited recomputation.
**Qualitative Linkage:** DJI's cyclical tilt means oil and industrial-metal moves may matter more here than for tech, but without data the relationship is uncertain. A TNX yields-up break could pressure rate-sensitive Dow names, while a VIX move above PP 18.20 would likely accompany broad de-risking. Energy and trade-policy channels remain conditional risks.

### Risk Management
ADX 23.98 → transitional, leaning trend given the clean uptrend: favor pullback-buys above PP 52148 with stops ≈ PP − 1.0×ATR (TDA NEUTRAL_STRUCTURE), targets R1 52346 then R2 52510. TDA_Flip_Risk = LOW → require confirmed closes for pivot breaks; fundamental (payrolls) dominates. Throttle size into 07-02 and stand aside on the 07-03 holiday. No averaging down.

### DJI Summary Table

| **Metric** | **Insight** |
| --- | --- |
| **Current Value** | 52319 |
| **Forecast Value** | 52384–52503 / **52467** |
| **Bias** | Higher |
| **Confidence** | Moderate |
| **Sentiment Score** | 6.3/10 — best structural alignment |
| **Commodity Correlation** | Limitation (no series supplied) |
| **Key Events** | Payrolls 07-02[^1]; USMCA[^7] |
| **Technical Insight** | Uptrend; Stoch/CCI/W%R overbought (pullback risk) |
| **Econometric Insight** | ARIMAX(1,1,1) 52502.59; ARCH not significant |
| **ML Insight** | Tight cluster; Torch/DYNAMIX outliers bracket it |

---

## QQQ

Forecast Report for QQQ — Current: 736.40 | 3-Day Prediction: 739.05–744.00 and exact **739.79**

### Forecast Positioning Rationale
**Forecast Positioning Rationale:**
• Sentiment Score: 3.0/10 (Adjusted Final Score from Step 1; Base + Structural Adjustment `MISSING_USER_INPUT`; local CoherenceScore 0)
• Placement: 15th percentile of ML range (739.05 – 744.00)
• Primary Influence: Bearish structural signals (sentiment ≤3 dominates; AI/semis valuation risk)
• Key Factor: DISTRIBUTED_CYCLES (TDA Entropy 2.80 > 2.50) + AI-bubble fragility; ML cluster floors above spot, so Exact pinned to the range floor
• ML Reference Comparison: 739.79 vs 727.58 (FH_Day3): positioned above ML reference because the P25–P75 band sits well above the bearish FH_Day3, but at the band floor to honor sentiment

### Visual Chart Analysis & Regions
Region detection summary: N_total_regions = 2 (Region 1 tan ≈ Jun 01–11; Region 2 blue ≈ Jun 11–30); N_recent_regions = 2. Current region_id(T0) = Region 2; new_region(T0) = 0. Momentum(T0) = up (recovery into 736 from late-June dip). Pivot interaction: Above PP — |736.40 − 717.94| = 18.46 > 0.25×ATR = 4.01 (DERIVED_METRIC: 0.25×16.03).

| Region | Approx date span | Slope | Volatility | Key pivot behavior | Regime risk note |
| --- | --- | --- | --- | --- | --- |
| Region 1 | Jun 01–11 (approx) | Down | High | Broke PP to S2 trough ~694 | AI-selloff stress |
| Region 2 | Jun 11–30 (approx) | Up | Med | Reclaimed PP, pinned near R2 737 | RANDOM→MEAN_REVERT 06-29 |

Note #3: Range-bound under R2 despite the bounce.

Base-case path (p≈0.45; CoherenceScore 0, momentum up contradicts FH-down): Day+1 near FH 735, then drift to FH 727–728 toward R1 730.72 / PP 717.94; Exact 739.79 sits at the ML floor, above spot but below the cluster.

Flip triggers:
- Mechanical: a daily close below PP 717.94 by ≥ 0.25×ATR (≥ 4.01) deepens downside; a close above R1 730.72 by the same margin negates the bearish lean.
- Fundamental: June Employment Situation, 2026-07-02 08:30 ET (rate-sensitive tech).[^1]

Note #1: Bearish sentiment fights a model floor above spot.

Risk mapping: fade rallies toward R2 737 with stops above R2 + 0.5×ATR, targeting PP 717.94, sizing down to ATR 16 and DISTRIBUTED_CYCLES.

Note #2: Use smaller size; breakouts may be false.

Visual limitation: region meanings are inferred from colored spans and are uncertainty-qualified.

### Technical Indicators (28-day)

| Indicator | Reading | Interpretation | Actionable Takeaway |
| --- | --- | --- | --- |
| Classic Pivot | 717.94 | Above PP; |736.40−717.94|=18.46 > 0.25×ATR=4.01 (DERIVED_METRIC) | Target R1 730.72 / R2 737.35 |
| 50-DMA | 709.56 | Current above → bullish bias | 50-DMA as support |
| 200-DMA | 635.45 | Current above → bullish bias | 200-DMA as deep support |
| RSI(14) | 56.45 | 30–70 neutral | No overbought/oversold signal |
| Stochastic %K | 58.49 | 20–80 neutral | No overbought/oversold signal |
| ATR(14) | 16.03 | Volatility input | Size stops to ~16 pts |
| ATR% | 2.18% | ATR%=16.03/736.40=2.18% → High (>2.00%) (DERIVED_METRIC) | Wider stops and/or smaller size |
| ADX(14) | 19.03 | 18–25 transition | Mixed range/trend posture |
| CCI(14) | 46.50 | −100…+100 neutral | No overbought/oversold signal |
| Williams %R | −17.94 | >−20 overbought | Mean-reversion risk (downside) |
| Ultimate Oscillator | 51.75 | 30–70 neutral | No overbought/oversold signal |
| ROC(10) | 0.90 | Positive momentum (sign) | Momentum strengthening |
| BullBear Power | 14.24 | >0 bulls dominant | Mild bull control |

### Econometric Analysis (ARIMA/ARIMAX)
ARIMAX selected p,d,q = (1,1,1) with exogenous regressors. Residual ARCH test p-value 0.0000 → Significant — GARCH is appropriate for QQQ, the only ticker where conditional heteroskedasticity is flagged, consistent with the High ATR% and DISTRIBUTED_CYCLES read. Day-3 ARIMAX forecast 741.24, 95% CI [733.86, 748.63]. Quoted as ground truth.

### Machine-Learning Forecast Note (no averaging)
Day-3 points: Torch 716.38; DYNAMIX 762.12 (alt 733.99); ARIMAX 741.24; PCE 743.30; LSTM 744.00; GARCH 746.08; VAR 740.69; RW 739.05; ETS 738.41. Median = 741.24, MAD = 2.75, MAD_floor = max(2.75, 0.10×ATR=1.60) = 2.75 (DERIVED_METRIC). Outliers (≥ 3×MAD_floor=8.26): **Torch (low)** and **DYNAMIX (high)**. Divergence Note: dispersion 45.74 ≥ max(1.5×ATR=24.05, 4×MAD_floor=11.02) → wide. Dominance condition = close below PP 717.94 favors Torch's bearish path; risk implication = wait-for-close, ADX 19.0 transitional, reduce size 20–30% (DISTRIBUTED_CYCLES). No averaging.

### Sentiment (0–10)
- Base Sentiment Score: `MISSING_USER_INPUT`
- CoherenceScore: 0 (Trend10D align 0 [FLAT vs FH-down]; Regime-ADX align 0 [RANDOM]; Williams align 0 [BULLISH vs FH-down]; VIX penalty 0)
- Structural Adjustment: `MISSING_USER_INPUT` (cap ±2; not exceeded)
- Adjusted Sentiment Score: 3.0/10
- Confidence: Medium → downgraded to **Low** (VIX-up + TNX-up couplings; weakest equity setup)
- Mechanical Drivers: above PP/MAs but pinned under R2; High ATR%; DISTRIBUTED_CYCLES
- Fundamental Drivers: AI/semiconductor valuation & capex risk[^6][^10]; rate sensitivity; tech regulation
- Catalyst Flip Map: Payrolls-driven yield spike + close below PP 717.94 deepens downside; close above R1 730.72 negates.[^1]

Rate-sensitivity clause: QQQ is the most rate-exposed name; a TNX close above R2 4.43 is the primary downside accelerant.

### Recent Major Events (Last 7 Calendar Days)

| Date | Event | Impact Factor | One-Line Impact | News Direction | Structural Alignment | Source |
| --- | --- | --- | --- | --- | --- | --- |
| 2026-06-23/24 | AI/semiconductor selloff, bubble fears | Volatility | Nasdaq −2.2%; trillion-dollar swings; capex scrutiny | Negative | Aligned — matches MEAN_REVERT shift, weak sentiment | [^6][^10] |
| 2026-06-30 | Month-end macro (Chicago PMI/Case-Shiller) | Other | Minor; limited tech impact | Neutral | Aligned — consolidative tape | [^9] `UNVERIFIED_OFFICIAL_LINK` |

### Upcoming Events (Next 3 Trading Days)

| Date | Event | Impact Factor | Expected Sensitivity | Source |
| --- | --- | --- | --- | --- |
| 2026-07-01 | ISM Manufacturing PMI; ADP payrolls | Labor | Medium — rate-path read for tech | [^3][^4] `UNVERIFIED_OFFICIAL_LINK` (ADP time) |
| 2026-07-02 08:30 ET | June Employment Situation | Labor | High — rate-sensitive Nasdaq leadership | [^1] |
| 2026-07-03 | NYSE closed (Independence Day observed) | Other | None — market holiday | [^5] |

### Commodity Correlation (28-day)
**Limitation:** No commodity series supplied; 28-day r/p not computable without prohibited recomputation.
**Qualitative Linkage:** QQQ is likely far more sensitive to rates than to commodities; a TNX yields-up break would plausibly compress tech multiples, and a VIX close above PP 18.20 would likely coincide with sharp Nasdaq drawdowns. Commodity linkages are weak and uncertain here, while the rate/vol channels are the conditional drivers to watch.

### Risk Management
ADX 19.03 → transitional with range bias: fade strength toward R2 737, stops above R2 + 0.5×ATR, target PP 717.94. TDA = DISTRIBUTED_CYCLES → reduce position size 20–30% and widen stops for false-breakout risk; TDA_Flip_Risk = LOW so fundamental (payrolls) triggers dominate. Throttle hard into 07-02 and avoid the 07-03 holiday. No averaging down.

### QQQ Summary Table

| **Metric** | **Insight** |
| --- | --- |
| **Current Value** | 736.40 |
| **Forecast Value** | 739.05–744.00 / **739.79** |
| **Bias** | Lower |
| **Confidence** | Low |
| **Sentiment Score** | 3.0/10 — weakest setup; AI/semis risk |
| **Commodity Correlation** | Limitation (no series supplied) |
| **Key Events** | Payrolls 07-02[^1]; AI selloff[^6] |
| **Technical Insight** | Above pivots but capped at R2; High ATR%; W%R overbought |
| **Econometric Insight** | ARIMAX(1,1,1) 741.24; ARCH significant (GARCH apt) |
| **ML Insight** | Wide divergence; Torch bearish vs DYNAMIX bullish outliers |

---

## VIX

Forecast Report for VIX — Current: 16.45 | 3-Day Prediction: 16.32–16.78 and exact **16.64**

### Forecast Positioning Rationale
**Forecast Positioning Rationale:**
• Sentiment Score: 6.4/10 (Adjusted Final Score from Step 1; Base + Structural Adjustment `MISSING_USER_INPUT`; local CoherenceScore 0)
• Placement: 70th percentile of ML range (16.32 – 16.78)
• Primary Influence: Volatility-up signals (sentiment 6.4 = vol-up; MEAN_REVERT from suppressed level)
• Key Factor: Pre-payrolls, pre-holiday demand for protection; price below both MAs implies mean-reversion higher
• ML Reference Comparison: 16.64 vs 16.78 (FH_Day3): |16.64 − 16.78| = 0.14 < 0.10×ATR = 0.21 → "Aligned with ML central tendency"

### Visual Chart Analysis & Regions
Region detection summary: N_total_regions = 2 (Region 1 tan ≈ Jun 01–11; Region 2 blue ≈ Jun 11–30); N_recent_regions = 2. Current region_id(T0) = Region 2; new_region(T0) = 0. Momentum(T0) = down (decline into 16.45 from the 06-23 peak ~19.5). Pivot interaction: Below PP — |16.45 − 18.20| = 1.75 > 0.25×ATR = 0.52 (DERIVED_METRIC: 0.25×2.07).

| Region | Approx date span | Slope | Volatility | Key pivot behavior | Regime risk note |
| --- | --- | --- | --- | --- | --- |
| Region 1 | Jun 01–11 (approx) | Up-spike | High | Spiked to R3 22.1, then faded | Vol-of-vol extreme early |
| Region 2 | Jun 11–30 (approx) | Down/Choppy | Med | Below PP, oscillating S2–S1 | MEAN_REVERT 06-17, fade-prone |

Note #3: Compressed below the pivot, prone to mean-reversion pops.

Base-case path (p≈0.45; CoherenceScore 0, momentum down contradicts FH-up): mild grind from FH 16.74 to 16.78 within S2 16.24 / S1 16.94; Exact 16.64 sits between S2 and S1, below PP.

Flip triggers:
- Mechanical: a daily close above PP 18.20 by ≥ 0.25×ATR (≥ 0.52) confirms a volatility-up regime; a close below S1 16.94 toward S2 16.24 reverts vol-down.
- Fundamental: June Employment Situation, 2026-07-02 08:30 ET (surprise = vol spike).[^1]

Note #1: Cheap vol can pop on any payrolls surprise.

Risk mapping: treat long-vol as event hedge, not trend; size to ATR 2.07 with the pivot 18.20 as the up-regime line.

Note #2: Use VIX as a hedge into Thursday.

Visual limitation: region meanings are inferred from colored spans and are uncertainty-qualified.

### Technical Indicators (28-day)

| Indicator | Reading | Interpretation | Actionable Takeaway |
| --- | --- | --- | --- |
| Classic Pivot | 18.20 | Below PP; |16.45−18.20|=1.75 > 0.25×ATR=0.52 (DERIVED_METRIC) | Watch S1 16.94 / S2 16.24 |
| 50-DMA | 17.68 | Current below → bearish bias (low vol) | 50-DMA as resistance |
| 200-DMA | 18.72 | Current below → bearish bias (low vol) | 200-DMA as resistance |
| RSI(14) | 45.22 | 30–70 neutral | No overbought/oversold signal |
| Stochastic %K | 24.04 | 20–80 neutral (low) | No overbought/oversold signal |
| ATR(14) | 2.07 | Volatility input | Size stops to ~2.07 |
| ATR% | 12.60% | ATR%=2.0725/16.45=12.60% → High (DERIVED_METRIC) | Wider stops; vol-of-vol elevated |
| ADX(14) | 22.76 | 18–25 transition | Mixed range/trend posture |
| CCI(14) | −68.15 | −100…+100 neutral | No overbought/oversold signal |
| Williams %R | −90.03 | <−80 oversold | Mean-reversion risk (upside in VIX) |
| Ultimate Oscillator | 34.76 | 30–70 neutral (low) | No overbought/oversold signal |
| ROC(10) | 0.24 | Positive momentum (sign) | Momentum mildly strengthening |
| BullBear Power | −1.58 | <0 bears dominant | Bear control (low-vol drift) |

### Econometric Analysis (ARIMA/ARIMAX)
ARIMAX selected p,d,q = (1,1,1) with exogenous regressors. Residual ARCH test p-value 0.1099 → Not Significant. Day-3 ARIMAX forecast 16.33, 95% CI [15.16, 17.49]. The GARCH variance forecast is comparatively large in level terms (52.33→54.44), reflecting VIX's intrinsic vol-of-vol; quoted as ground truth, no recomputation.

### Machine-Learning Forecast Note (no averaging)
Day-3 points: Torch 18.89; DYNAMIX 14.67 (alt 17.11); ARIMAX 16.33; PCE 17.03; LSTM 15.88; GARCH 16.78; VAR 16.76; RW 16.32; ETS 16.57. Median = 16.57, MAD = 0.25, MAD_floor = max(0.25, 0.10×ATR=0.21) = 0.25 (DERIVED_METRIC). Outliers (≥ 3×MAD_floor=0.76): **Torch (high, vol-up)** and **DYNAMIX (low, vol-down)**. Divergence Note: dispersion 4.22 ≥ max(1.5×ATR=3.11, 4×MAD_floor=1.02) → wide; models disagree on direction of fear. Dominance condition = close above PP 18.20 favors Torch; risk implication = treat as event-hedge, wait-for-close. No averaging.

### Sentiment (0–10)
- Base Sentiment Score: `MISSING_USER_INPUT`
- CoherenceScore: 0 (Trend10D align 0 [FLAT vs FH-up]; Regime-ADX align 0 [MEAN_REVERT but ADX 22.8 ≥ 18]; Williams align 0 [BEARISH vs FH-up]; VIX penalty n/a)
- Structural Adjustment: `MISSING_USER_INPUT` (cap ±2; not exceeded)
- Adjusted Sentiment Score: 6.4/10 (vol-up)
- Confidence: Medium
- Mechanical Drivers: below PP and both MAs (suppressed); W%R oversold; MEAN_REVERT
- Fundamental Drivers: payrolls surprise risk; policy uncertainty; unresolved Hormuz/Middle-East shipping tail
- Catalyst Flip Map: Payrolls surprise → close above PP 18.20 confirms vol-up; in-line data + close below S1 16.94 reverts vol-down.[^1]

### Recent Major Events (Last 7 Calendar Days)

| Date | Event | Impact Factor | One-Line Impact | News Direction | Structural Alignment | Source |
| --- | --- | --- | --- | --- | --- | --- |
| 2026-06-23/24 | AI/tech selloff (risk spike) | Volatility | Drove the late-June VIX peak ~19.5 before fade | Negative (risk-off) | Aligned — spike-then-revert matches MEAN_REVERT | [^6][^10] |
| 2026-06-30 | Month-end positioning | Volatility | Vol drifted lower into month/quarter-end | Neutral | Aligned — compression below pivot | [^9] `UNVERIFIED_OFFICIAL_LINK` |

### Upcoming Events (Next 3 Trading Days)

| Date | Event | Impact Factor | Expected Sensitivity | Source |
| --- | --- | --- | --- | --- |
| 2026-07-01 | ISM Manufacturing PMI; ADP payrolls | Labor | Medium — pre-positioning for the jobs print | [^3][^4] `UNVERIFIED_OFFICIAL_LINK` (ADP time) |
| 2026-07-02 08:30 ET | June Employment Situation | Volatility | High — primary vol catalyst this window | [^1] |
| 2026-07-03 | NYSE closed (Independence Day observed) | Other | None — market holiday; pre-holiday vol decay | [^5] |

### Commodity Correlation (28-day)
**Limitation:** No commodity series supplied; 28-day r/p not computable without prohibited recomputation.
**Qualitative Linkage:** VIX typically rises with risk-off episodes that may accompany oil spikes from Middle-East shipping disruption, but the relationship is uncertain and regime-dependent. A VIX close above PP 18.20 would likely coincide with equity drawdowns (SPX/QQQ/AAPL) and a flight that may pull TNX lower; these couplings are conditional.

### Risk Management
ADX 22.76 → transitional: trade VIX as an event hedge rather than a trend. The up-regime line is PP 18.20; below S1 16.94 favors continued decay. TDA NEUTRAL_STRUCTURE → standard ATR posture, but ATR% 12.60% means vol-of-vol is high, so size small. TDA_Flip_Risk = LOW → fundamental (payrolls) triggers dominate. Concentrate any long-vol as a 07-02 hedge; expect pre-holiday decay 07-03. No averaging down.

### VIX Summary Table

| **Metric** | **Insight** |
| --- | --- |
| **Current Value** | 16.45 |
| **Forecast Value** | 16.32–16.78 / **16.64** |
| **Bias** | Higher (volatility-up) |
| **Confidence** | Moderate |
| **Sentiment Score** | 6.4/10 — vol-up into payrolls |
| **Commodity Correlation** | Limitation (no series supplied) |
| **Key Events** | Payrolls 07-02[^1]; AI risk spike[^6] |
| **Technical Insight** | Below PP/MAs; W%R oversold (pop risk) |
| **Econometric Insight** | ARIMAX(1,1,1) 16.33; ARCH not significant |
| **ML Insight** | Wide divergence; Torch vol-up vs DYNAMIX vol-down |

---

## TNX

Forecast Report for TNX — Current: 4.42 | 3-Day Prediction: 4.39–4.42 and exact **4.41**

### Forecast Positioning Rationale
**Forecast Positioning Rationale:**
• Sentiment Score: 6.2/10 (Adjusted Final Score from Step 1; Base + Structural Adjustment `MISSING_USER_INPUT`; local CoherenceScore 1)
• Placement: 70th percentile of ML range (4.39 – 4.42)
• Primary Influence: Yields-up signals (Williams BULLISH aligns with FH-up; sentiment 6.2)
• Key Factor: Most catalyst-sensitive instrument; the ML range sits marginally below spot 4.418, so even upper placement is ≤ current
• ML Reference Comparison: 4.41 vs 4.456 (FH_Day3): positioned below ML reference because P25–P75 caps below FH_Day3; placement honors yields-up within that capped band

### Visual Chart Analysis & Regions
Region detection summary: N_total_regions = 3 (Region 1 tan ≈ Jun 01–10; Region 2 blue ≈ Jun 11–23; Region 3 green ≈ Jun 24–30); N_recent_regions = 3. Current region_id(T0) = Region 3; new_region(T0) = 0 (Region 3 began ≈ 5 sessions ago). Momentum(T0) = up (rebound from the 4.372 trough to 4.418). Pivot interaction: Above PP — |4.418 − 4.383| = 0.035 > 0.25×ATR = 0.013 (DERIVED_METRIC: 0.25×0.0537).

| Region | Approx date span | Slope | Volatility | Key pivot behavior | Regime risk note |
| --- | --- | --- | --- | --- | --- |
| Region 2 | Jun 11–23 (approx) | Down/Choppy | Med | Oscillated PP–R3, faded from 4.55 peak | Rate-path indecision |
| Region 3 | Jun 24–30 (approx) | Up (rebound) | Low | Held above PP, reclaimed toward R2 4.43 | MEAN_REVERT→RANDOM 06-30 |

Note #3: Yields rebounded off support into the jobs print.

Base-case path (p≈0.55; CoherenceScore 1, signals mixed): rise from FH 4.425 toward FH 4.456 and R2 4.426, holding above PP 4.383; Exact 4.41 sits between PP and R2.

Flip triggers:
- Mechanical: a daily close above R2 4.426 by ≥ 0.25×ATR (≥ 0.013, i.e. > 4.439) confirms yields-up; a close below PP 4.383 by the same margin flips yields-down.
- Fundamental: June Employment Situation, 2026-07-02 08:30 ET (the dominant yield driver).[^1]

Note #1: Hot jobs lift yields; soft jobs pull them down.

Risk mapping: trade the PP 4.383 / R2 4.426 band, stops beyond the broken pivot, sizing to the very small ATR 0.0537.

Note #2: Tiny ATR means small absolute moves matter.

Visual limitation: region meanings are inferred from colored spans and are uncertainty-qualified.

### Technical Indicators (28-day) — direction interpreted in yield terms

| Indicator | Reading | Interpretation | Actionable Takeaway |
| --- | --- | --- | --- |
| Classic Pivot | 4.38 | Above PP; |4.418−4.383|=0.035 > 0.25×ATR=0.013 (DERIVED_METRIC) | Target R1 4.40 / R2 4.43 (yields-up) |
| 50-DMA | 4.46 | Current below → bearish bias (yields below trend) | 50-DMA as yield resistance |
| 200-DMA | 4.23 | Current above → bullish bias (yields above trend) | 200-DMA as yield support |
| RSI(14) | 46.02 | 30–70 neutral | No overbought/oversold signal |
| Stochastic %K | 12.85 | <20 oversold | Mean-reversion risk (yields up) |
| ATR(14) | 0.05 | Volatility input | Size stops to ~0.05 (5bp) |
| ATR% | 1.22% | ATR%=0.0537/4.4180=1.22% → Medium (DERIVED_METRIC) | Standard stop width |
| ADX(14) | 15.03 | <18 range | Range-trade posture |
| CCI(14) | −64.59 | −100…+100 neutral | No overbought/oversold signal |
| Williams %R | −70.59 | −80…−20 neutral | No overbought/oversold signal |
| Ultimate Oscillator | 45.01 | 30–70 neutral | No overbought/oversold signal |
| ROC(10) | −0.23 | Negative momentum (sign) | Momentum weakening (yields) |
| BullBear Power | −0.05 | ~0 balanced | Balanced; no edge |

### Econometric Analysis (ARIMA/ARIMAX)
ARIMAX selected p,d,q = (1,1,1) with exogenous regressors. Residual ARCH test p-value 0.6056 → Not Significant; the highest (least-flagged) of the set. Day-3 ARIMAX forecast 4.3873, 95% CI [4.3535, 4.4210]. GARCH beta 0.9831 indicates very persistent (near-unit) variance memory; quoted as ground truth.

### Machine-Learning Forecast Note (no averaging)
Day-3 points: Torch 4.3920; DYNAMIX 4.3949 (alt 4.3783); ARIMAX 4.3873; PCE 4.3954; LSTM 4.4175; GARCH 4.4164; VAR 4.4160; RW 4.4189; ETS 4.4152. Median = 4.4152, MAD = 0.0037, MAD_floor = max(0.0037, 0.10×ATR=0.0054) = 0.0054 (DERIVED_METRIC). Outliers (≥ 3×MAD_floor=0.0162): **Torch, DYNAMIX, ARIMAX, PCE** (the four lower-yield estimates). Divergence Note: dispersion 0.0316 is below the 1.5×ATR=0.081 wide-gate, but four MAD-outliers trigger Rule 14(b); the split is "yields-flat-to-down" (4.39 cluster) vs "yields-up" (4.42 cluster). Dominance condition = a close above R2 4.426 favors the high cluster; risk implication = wait-for-close, ADX 15.0 range. No averaging.

### Sentiment (0–10) — yields-up = bullish
- Base Sentiment Score: `MISSING_USER_INPUT`
- CoherenceScore: 1 (Trend10D align 0 [DOWN vs FH-up]; Regime-ADX align 0 [RANDOM]; Williams align +1 [BULLISH = yields-up = FH-up]; VIX penalty 0)
- Structural Adjustment: `MISSING_USER_INPUT` (cap ±2; not exceeded)
- Adjusted Sentiment Score: 6.2/10
- Confidence: Medium
- Mechanical Drivers: above PP and 200-DMA; Stoch oversold (mean-revert up); near-unit GARCH persistence
- Fundamental Drivers: June payrolls 07-02 (dominant); ADP/ISM 07-01; Fed-path repricing
- Catalyst Flip Map: Hot payrolls → close above R2 4.426 confirms yields-up; soft payrolls → close below PP 4.383 flips yields-down.[^1]

### Recent Major Events (Last 7 Calendar Days)

| Date | Event | Impact Factor | One-Line Impact | News Direction | Structural Alignment | Source |
| --- | --- | --- | --- | --- | --- | --- |
| 2026-06-23/24 | Hawkish-Fed worry amid tech selloff | Fed | Reinforced rate-cut caution; supported yields | Yields-up | Mixed — Trend10D DOWN vs yields-up read | [^6] |
| 2026-06-30 | MEAN_REVERT→RANDOM regime change (SVL) | Other | Near-term yield regime less mean-reverting | Neutral | Aligned — user SVL ground truth | user-supplied (no cite) |

### Upcoming Events (Next 3 Trading Days)

| Date | Event | Impact Factor | Expected Sensitivity | Source |
| --- | --- | --- | --- | --- |
| 2026-07-01 | ISM Manufacturing PMI; ADP payrolls | Labor | Medium-High — early rate-path signal | [^3][^4] `UNVERIFIED_OFFICIAL_LINK` (ADP time) |
| 2026-07-02 08:30 ET | June Employment Situation | Labor | High — the dominant TNX catalyst | [^1] |
| 2026-07-03 | NYSE closed (Independence Day observed) | Other | None — bond-market holiday context | [^5] |

### Commodity Correlation (28-day)
**Limitation:** No commodity series supplied; 28-day r/p not computable without prohibited recomputation.
**Qualitative Linkage:** Yields may co-move with oil through the inflation-expectations channel, but the relationship is uncertain over a 3-day window. A TNX break above R2 4.43 would likely tighten financial conditions and pressure QQQ/AAPL/SPX, while a flight-to-quality (VIX up) could conditionally pull yields lower despite hot data. These couplings are conditional.

### Risk Management
ADX 15.03 → range tactics: fade extremes within PP 4.383 / R2 4.426, stops just beyond the broken pivot, sized to the 5bp ATR. TDA NEUTRAL_STRUCTURE → standard stops; TDA_Flip_Risk = LOW → the 07-02 payrolls (fundamental) trigger dominates over mechanical pivot breaks. Throttle size into 07-02 08:30 ET; mind reduced 07-03 liquidity. No averaging down.

### TNX Summary Table

| **Metric** | **Insight** |
| --- | --- |
| **Current Value** | 4.42 |
| **Forecast Value** | 4.39–4.42 / **4.41** |
| **Bias** | Higher (yields-up) |
| **Confidence** | Moderate |
| **Sentiment Score** | 6.2/10 — yields-up; most catalyst-sensitive |
| **Commodity Correlation** | Limitation (no series supplied) |
| **Key Events** | Payrolls 07-02[^1]; ADP/ISM 07-01[^3] |
| **Technical Insight** | Above PP/200-DMA; Stoch oversold (mean-revert up) |
| **Econometric Insight** | ARIMAX(1,1,1) 4.3873; ARCH not significant; persistent GARCH |
| **ML Insight** | Four low-yield MAD-outliers vs yields-up cluster |

---

## AAPL

Forecast Report for AAPL — Current: 289.36 | 3-Day Prediction: 289.15–292.41 and exact **289.64**

### Forecast Positioning Rationale
**Forecast Positioning Rationale:**
• Sentiment Score: 3.2/10 (Adjusted Final Score from Step 1; Base + Structural Adjustment `MISSING_USER_INPUT`; local CoherenceScore 1)
• Placement: 15th percentile of ML range (289.15 – 292.41)
• Primary Influence: Bearish structural signals (Trend10D DOWN; RANDOM→MEAN_REVERT 06-25; sentiment 3.2)
• Key Factor: ADX 25.6 (trend) + bearish sentiment pull toward the lower bound, while the pivot tie-break sets nominal Bias = Higher
• ML Reference Comparison: 289.64 vs 288.77 (FH_Day3): |289.64 − 288.77| = 0.87 > 0.10×ATR=0.82 → positioned just above ML reference (boundary case) to honor the range floor

### Visual Chart Analysis & Regions
Region detection summary: N_total_regions = 1 (single tan Region 1 spanning the displayed window); N_recent_regions = 1. Current region_id(T0) = Region 1; new_region(T0) = 0. Momentum(T0) = up (recovery from the 06-25 trough ~275 into 289). Pivot interaction: Above PP — |289.36 − 283.32| = 6.04 > 0.25×ATR = 2.04 (DERIVED_METRIC: 0.25×8.16).

| Region | Approx date span | Slope | Volatility | Key pivot behavior | Regime risk note |
| --- | --- | --- | --- | --- | --- |
| Region 1 (early) | Jun 01–16 (approx) | Down | High | Rejected R3 315→299, faded to R2 | Distribution from highs |
| Region 1 (late) | Jun 17–30 (approx) | Down-then-bounce | High | Broke to S2 275, rebounded to PP/R1 | RANDOM→MEAN_REVERT 06-25 |

Note #3: One labeled region; a late bounce off S2 support.

Base-case path (p≈0.55; CoherenceScore 1, signals mixed): dip toward FH 283.87 then recovery to FH 288–289 around PP 283.32 / R1 286.79; Exact 289.64 sits near the R2 291.84 approach, at the ML floor.

Flip triggers:
- Mechanical: a daily close above R2 291.84 by ≥ 0.25×ATR (≥ 2.04, i.e. > 293.9) negates the bearish lean; a close below S1 278.27 by the same margin confirms downside.
- Fundamental: June Employment Situation, 2026-07-02 08:30 ET (rate channel).[^1]

Note #1: Bearish trend meets a pivot that sits below price.

Risk mapping: fade rallies toward R2 291.84 with stops above R2 + 0.5×ATR, target PP 283.32 / S1 278.27, sizing to ATR 8.16.

Note #2: Respect the down-trend; keep stops above R2.

Visual limitation: region meanings are inferred from colored spans and are uncertainty-qualified.

### Technical Indicators (28-day)

| Indicator | Reading | Interpretation | Actionable Takeaway |
| --- | --- | --- | --- |
| Classic Pivot | 283.32 | Above PP; |289.36−283.32|=6.04 > 0.25×ATR=2.04 (DERIVED_METRIC) | Target R1 286.79 / R2 291.84 |
| 50-DMA | 293.60 | Current below → bearish bias | 50-DMA as resistance |
| 200-DMA | 271.31 | Current above → bullish bias | 200-DMA as support |
| RSI(14) | 46.55 | 30–70 neutral | No overbought/oversold signal |
| Stochastic %K | 39.10 | 20–80 neutral | No overbought/oversold signal |
| ATR(14) | 8.16 | Volatility input | Size stops to ~8.16 |
| ATR% | 2.82% | ATR%=8.1607/289.36=2.82% → High (DERIVED_METRIC) | Wider stops and/or smaller size |
| ADX(14) | 25.63 | >25 trend | Trend-follow posture (down-trend) |
| CCI(14) | −68.99 | −100…+100 neutral | No overbought/oversold signal |
| Williams %R | −45.55 | −80…−20 neutral | No overbought/oversold signal |
| Ultimate Oscillator | 35.35 | 30–70 neutral (low) | No overbought/oversold signal |
| ROC(10) | −3.30 | Negative momentum (sign) | Momentum weakening |
| BullBear Power | −10.96 | <0 bears dominant | Bear control |

### Econometric Analysis (ARIMA/ARIMAX)
ARIMAX selected p,d,q = (1,1,1) with exogenous regressors. Residual ARCH test p-value 0.9731 → Not Significant (the least-flagged residuals of the set). Day-3 ARIMAX forecast 289.15, 95% CI [285.23, 293.06]. GARCH beta 0.8998 indicates persistent variance; quoted as ground truth, no recomputation.

### Machine-Learning Forecast Note (no averaging)
Day-3 points: Torch 275.15; DYNAMIX 275.07 (alt 284.71); ARIMAX 289.15; PCE 289.24; LSTM 292.41; GARCH 292.64; VAR 295.70; RW 290.19; ETS 290.19. Median = 290.19, MAD = 2.22, MAD_floor = max(2.22, 0.10×ATR=0.82) = 2.22 (DERIVED_METRIC). Outliers (≥ 3×MAD_floor=6.66): **Torch and DYNAMIX** (both low ~275, the bearish pair). Divergence Note: dispersion 20.63 ≥ max(1.5×ATR=12.24, 4×MAD_floor=8.87) → wide; a bearish ~275 pair sits well below the ~289–296 cluster. Dominance condition = a close below S1 278.27 validates the Torch/DYNAMIX path; risk implication = wait-for-close, reduce size given High ATR%. No averaging.

### Sentiment (0–10)
- Base Sentiment Score: `MISSING_USER_INPUT`
- CoherenceScore: 1 (Trend10D align 0 [DOWN vs FH-up]; Regime-ADX align 0 [RANDOM, not the MEAN_REVERT&ADX<18 case]; Williams align +1 [BULLISH = FH-up]; VIX penalty 0)
- Structural Adjustment: `MISSING_USER_INPUT` (cap ±2; not exceeded)
- Adjusted Sentiment Score: 3.2/10
- Confidence: Medium → downgraded to **Low** (VIX-up + TNX-up couplings; Trend10D DOWN)
- Mechanical Drivers: above PP/200-DMA but below 50-DMA; ADX 25.6 down-trend; bears dominant
- Fundamental Drivers: memory-chip cost pressure / supply-chain; broad tech-risk compression; rate sensitivity[^6]
- Catalyst Flip Map: Close above R2 291.84 negates the bearish lean; close below S1 278.27 confirms downside; payrolls 07-02 risk.[^1]

Rate-sensitivity clause: a TNX close above R2 4.43 would compound AAPL downside via the rate channel; this keeps the nominal Higher tag low-conviction.

### Recent Major Events (Last 7 Calendar Days)

| Date | Event | Impact Factor | One-Line Impact | News Direction | Structural Alignment | Source |
| --- | --- | --- | --- | --- | --- | --- |
| 2026-06-23/24 | Tech/AI selloff; mega-cap swings | Volatility | Compressed AAPL into the 06-25 S2 trough | Negative | Aligned — matches Trend10D DOWN, weak sentiment | [^6][^10] |
| 2026-06-25 | RANDOM→MEAN_REVERT regime change (SVL) | Other | Near-term regime turned mean-reverting | Neutral | Aligned — user SVL ground truth | user-supplied (no cite) |

### Upcoming Events (Next 3 Trading Days)

| Date | Event | Impact Factor | Expected Sensitivity | Source |
| --- | --- | --- | --- | --- |
| 2026-07-01 | ISM Manufacturing PMI; ADP payrolls | Labor | Medium — supply-chain/rate read | [^3][^4] `UNVERIFIED_OFFICIAL_LINK` (ADP time) |
| 2026-07-02 08:30 ET | June Employment Situation | Labor | High — rate-sensitive mega-cap | [^1] |
| 2026-07-03 | NYSE closed (Independence Day observed) | Other | None — market holiday | [^5] |

### Commodity Correlation (28-day)
**Limitation:** No commodity series supplied; 28-day r/p not computable without prohibited recomputation.
**Qualitative Linkage:** AAPL is more exposed to rates and supply-chain costs than to commodities directly; a TNX yields-up break may pressure the multiple, and a VIX close above PP 18.20 would likely accompany a broad mega-cap drawdown. Memory-chip cost inflation is a company-specific channel whose market impact is uncertain over a 3-day window. These linkages are conditional.

### Risk Management
ADX 25.63 → trend tactics (down-trend bias): favor selling rallies toward R2 291.84, stops above R2 + 0.5×ATR, targets PP 283.32 then S1 278.27. TDA NEUTRAL_STRUCTURE → standard stops, but ATR% 2.82% (High) argues for smaller size; TDA_Flip_Risk = LOW → fundamental (payrolls) triggers dominate over mechanical ones. Throttle into 07-02 and avoid the 07-03 holiday. No averaging down.

### AAPL Summary Table

| **Metric** | **Insight** |
| --- | --- |
| **Current Value** | 289.36 |
| **Forecast Value** | 289.15–292.41 / **289.64** |
| **Bias** | Higher (Level-4 pivot; `BIAS_POSITIONING_CONFLICT`) |
| **Confidence** | Low |
| **Sentiment Score** | 3.2/10 — bearish trend; supply-chain risk |
| **Commodity Correlation** | Limitation (no series supplied) |
| **Key Events** | Payrolls 07-02[^1]; tech selloff[^6] |
| **Technical Insight** | Above PP/200-DMA, below 50-DMA; ADX 25.6 down-trend |
| **Econometric Insight** | ARIMAX(1,1,1) 289.15; ARCH not significant |
| **ML Insight** | Wide divergence; Torch/DYNAMIX bearish ~275 outliers |

---

## Structural Spotlight (StructuralSpotlight = true)
- **Topological Alert:** TDA is H1_NONE across all six tickers (no cycle persistence ≥ 0.50), so no topological support/resistance loops are detected; QQQ's elevated H1_Entropy (2.80) flags DISTRIBUTED_CYCLES → path-complexity risk and a 20–30% size reduction.
- **Fractal Convergence:** Williams 5-bar fractals are BULLISH on SPX, DJI, QQQ, TNX, AAPL and BEARISH on VIX; only TNX and AAPL have that bullish fractal aligning with their FH-up direction (CoherenceScore +1), making them the two names with any structural confirmation.
- **Cross-Asset Structural Linkage:** Five of six tickers changed SVL regime within 10 sessions and the +3-day window is gated by the 2026-07-02 payrolls print[^1] into a 2026-07-03 market holiday[^5] — a thin-liquidity, high-catalyst setup that argues for reduced size across the board.

---

## Final Three-Day Forecasts Table

| Ticker | Forecast range <br> --- <br> Forecast **exact** Value | Bias | Rationale |
| --- | --- | --- | --- |
| SPX | 7517–7543 <br> --- <br> **7525** | Higher | ML floor above spot; cautious sentiment 4.0 → 30th-pct placement; `BIAS_POSITIONING_CONFLICT`. Payrolls/AI risk.[^1][^6] |
| DJI | 52384–52503 <br> --- <br> **52467** | Higher | Cleanest uptrend; sentiment 6.3 → 70th-pct; R2 52510 target. Labor/USMCA risk.[^1][^7] |
| QQQ | 739.05–744.00 <br> --- <br> **739.79** | Lower | Sentiment 3.0 dominates; DISTRIBUTED_CYCLES + AI/semis risk; floor-pinned.[^6][^10] |
| VIX | 16.32–16.78 <br> --- <br> **16.64** | Higher | Vol-up sentiment 6.4; MEAN_REVERT below MAs; payrolls hedge.[^1] |
| TNX | 4.39–4.42 <br> --- <br> **4.41** | Higher | Yields-up; Williams aligned; most catalyst-sensitive to payrolls.[^1] |
| AAPL | 289.15–292.41 <br> --- <br> **289.64** | Higher | Level-4 pivot tie-break Higher vs bearish sentiment 3.2; `BIAS_POSITIONING_CONFLICT`.[^1] |

---

## References (Footnotes)

[^1]: U.S. Bureau of Labor Statistics — Schedule of Releases for the Employment Situation (June data, 2026-07-02 08:30 ET).
[^2]: U.S. Bureau of Labor Statistics — Schedule of Selected Releases 2026.
[^3]: Institute for Supply Management — ROB Report Calendar (ISM Manufacturing PMI, June 2026, 2026-07-01 10:00 ET).
[^4]: Investing.com — "ADP employment, manufacturing PMI, and oil inventories due Wednesday" (Tier-2; ADP timing unverified by official source).
[^5]: New York Stock Exchange — Holidays & Trading Hours (NYSE closed 2026-07-03, Independence Day observed).
[^6]: Reuters — "Tech selloff stirs bubble fears in US stock market" (2026-06-30).
[^7]: Reuters — "US expected to not extend USMCA, starting a decade-long countdown for trade pact" (2026-06-30).
[^8]: Reuters — "Why Trump's tariffs had plenty of bark, but limited bite" (2026-06-30).
[^9]: Kiplinger — "What to Look Out for in Economic Data This Week (June 29–July 3)."
[^10]: NPR — "Is AI 'one big bubble'? Behind the tech sell-off" (2026-06-23).
[^11]: Federal Reserve — FOMC Meeting Calendars (next meeting 2026-07-28/29; outside forecast window).

---

## QA / Fact-Lock Summary
- RANGE_CONSTRAINT_LOCK: PASS — every Exact ∈ [Range_Lo, Range_Hi] (SPX 7525∈[7517,7543]; DJI 52467∈[52384,52503]; QQQ 739.79∈[739.05,744.00]; VIX 16.64∈[16.32,16.78]; TNX 4.41∈[4.39,4.42]; AAPL 289.64∈[289.15,292.41]).
- SENTIMENT_CONSISTENCY_LOCK: PASS — sentiment ≤4 names (SPX 4.0, QQQ 3.0, AAPL 3.2) all placed in lower-50% of range; no ≥7 names.
- BIAS_LOCK: PASS — Bias consistent across Executive Summary, per-ticker Summary, and Final Table.
- BIAS_POSITIONING_CONFLICT: SPX, AAPL — flagged and explained (Higher bias with Exact in lower-40% of range).
- EVENT_LEDGER_LOCK: PASS — Recent/Upcoming tables match the frozen Stage-1 ledger; ADP-time rows carry `UNVERIFIED_OFFICIAL_LINK`.
- MISSING_USER_INPUT: Base_Sentiment_Score, Structural_Adjustment (all tickers) — Step 1 supplied Adjusted/Final only.
- TDA_AVAILABLE = true (H1_NONE all tickers); no LEDGER_FREEZE_VIOLATION; scenario probabilities sum to 100.