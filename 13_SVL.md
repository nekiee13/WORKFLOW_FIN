STRUCTURAL_CONTEXT (Computed from internal OHLCV; no web citations)
As-of (last close): 2026-06-30
Data source: Mixed (per ticker); see Provenance
Lookbacks: H20/H60/H120; Williams fractals (5-bar); H20 mini-history = last 10 business days
Trend definition: Trend10D computed from Close over last 10 business days (UP if >= +1%, DOWN if <= -1%, else FLAT)

[TNX]
Hurst:
  H20_current: 0.45
  H60_current: 0.54
  H120_current: 0.55
  Regime_current: RANDOM
  H20_last10: [0.48, 0.49, 0.49, 0.50, 0.47, 0.42, 0.45, 0.41, 0.42, 0.45]
  RegimeChange_last10: YES
  RegimeChange_note: "2026-06-30: MEAN_REVERT→RANDOM"
Trend10D: DOWN
WilliamsFractals:
  Signal_last5: BULLISH
  Level: 4.36
  Note: "Confirmed fractal index=489 (<= t-2)."
Provenance:
  computed_on: 2026-07-01 00:14
  method_notes: "SVL-v1.0: Hurst via R/S on log(Close) windows; Trend10D thresholds ±1%; Williams 5-bar fractals confirmed up to t-2. | H120 suggests broader regime differs (PERSISTENT); interpret near-term regime with caution. | Williams: Confirmed fractal index=489 (<= t-2)."

[DJI]
Hurst:
  H20_current: 0.46
  H60_current: 0.49
  H120_current: 0.55
  Regime_current: RANDOM
  H20_last10: [0.53, 0.47, 0.46, 0.46, 0.46, 0.46, 0.46, 0.46, 0.46, 0.46]
  RegimeChange_last10: NO
  RegimeChange_note: ""
Trend10D: FLAT
WilliamsFractals:
  Signal_last5: BULLISH
  Level: 51614.74
  Note: "Confirmed fractal index=492 (<= t-2)."
Provenance:
  computed_on: 2026-07-01 00:14
  method_notes: "SVL-v1.0: Hurst via R/S on log(Close) windows; Trend10D thresholds ±1%; Williams 5-bar fractals confirmed up to t-2. | H120 suggests broader regime differs (PERSISTENT); interpret near-term regime with caution. | Williams: Confirmed fractal index=492 (<= t-2)."

[SPX]
Hurst:
  H20_current: 0.44
  H60_current: 0.55
  H120_current: 0.59
  Regime_current: RANDOM
  H20_last10: [0.56, 0.50, 0.51, 0.50, 0.45, 0.45, 0.47, 0.47, 0.45, 0.44]
  RegimeChange_last10: YES
  RegimeChange_note: "2026-06-29: RANDOM→MEAN_REVERT"
Trend10D: FLAT
WilliamsFractals:
  Signal_last5: BULLISH
  Level: 7294.18
  Note: "Confirmed fractal index=492 (<= t-2)."
Provenance:
  computed_on: 2026-07-01 00:14
  method_notes: "SVL-v1.0: Hurst via R/S on log(Close) windows; Trend10D thresholds ±1%; Williams 5-bar fractals confirmed up to t-2. | H120 suggests broader regime differs (PERSISTENT); interpret near-term regime with caution. | Williams: Confirmed fractal index=492 (<= t-2)."

[VIX]
Hurst:
  H20_current: 0.39
  H60_current: 0.48
  H120_current: 0.46
  Regime_current: MEAN_REVERT
  H20_last10: [0.46, 0.40, 0.42, 0.40, 0.38, 0.38, 0.40, 0.40, 0.38, 0.39]
  RegimeChange_last10: YES
  RegimeChange_note: "2026-06-17: RANDOM→MEAN_REVERT"
Trend10D: FLAT
WilliamsFractals:
  Signal_last5: BEARISH
  Level: 20.72
  Note: "Confirmed fractal index=493 (<= t-2)."
Provenance:
  computed_on: 2026-07-01 00:14
  method_notes: "SVL-v1.0: Hurst via R/S on log(Close) windows; Trend10D thresholds ±1%; Williams 5-bar fractals confirmed up to t-2. | H120 suggests broader regime differs (RANDOM); interpret near-term regime with caution. | Williams: Confirmed fractal index=493 (<= t-2)."

[QQQ]
Hurst:
  H20_current: 0.40
  H60_current: 0.53
  H120_current: 0.59
  Regime_current: RANDOM
  H20_last10: [0.51, 0.48, 0.50, 0.49, 0.43, 0.43, 0.43, 0.46, 0.42, 0.40]
  RegimeChange_last10: YES
  RegimeChange_note: "2026-06-29: RANDOM→MEAN_REVERT"
Trend10D: FLAT
WilliamsFractals:
  Signal_last5: BULLISH
  Level: 702.81
  Note: "Confirmed fractal index=492 (<= t-2)."
Provenance:
  computed_on: 2026-07-01 00:14
  method_notes: "SVL-v1.0: Hurst via R/S on log(Close) windows; Trend10D thresholds ±1%; Williams 5-bar fractals confirmed up to t-2. | H120 suggests broader regime differs (PERSISTENT); interpret near-term regime with caution. | Williams: Confirmed fractal index=492 (<= t-2)."

[AAPL]
Hurst:
  H20_current: 0.36
  H60_current: 0.55
  H120_current: 0.53
  Regime_current: RANDOM
  H20_last10: [0.55, 0.53, 0.53, 0.52, 0.50, 0.49, 0.44, 0.35, 0.37, 0.36]
  RegimeChange_last10: YES
  RegimeChange_note: "2026-06-25: RANDOM→MEAN_REVERT"
Trend10D: DOWN
WilliamsFractals:
  Signal_last5: BULLISH
  Level: 273.75
  Note: "Confirmed fractal index=491 (<= t-2)."
Provenance:
  computed_on: 2026-07-01 00:14
  method_notes: "SVL-v1.0: Hurst via R/S on log(Close) windows; Trend10D thresholds ±1%; Williams 5-bar fractals confirmed up to t-2. | Williams: Confirmed fractal index=491 (<= t-2)."
