TDA_CONTEXT (Phase 2A — H1 cycles from return embeddings) (Computed from OHLCV; no web citations)
As-of (global): 2026-06-30
Method: Close -> log returns; delay embedding; persistent homology via ripser (maxdim=1).
Outputs: H1_MaxPersistence, H1_CountAbove_Thr, H1_Entropy.

[AAPL]
State: OK
AsOf:  2026-06-30
Params:
  window_len: 60
  embed_m: 3
  embed_tau: 1
  persist_thr: 0.500
  lastn: 10
Stats:
  n_obs_returns: 60
  n_embed_points: 58
  ret_vol: 0.017004
CPI Metrics (H1):
  H1_MaxPersistence: 0.335756
  H1_CountAbove_Thr: 0
  H1_Entropy: 2.159599
Assessment:
  H1_label: H1_NONE
  Note: "No meaningful H1 persistence above threshold (thr=0.500)."
Provenance:
  input: "OHLCV (Close -> log returns)"
  embedding: "delay(m=3, tau=1) over last 60 returns"
  ph: "ripser(maxdim=1) on standardized embedding"
  phase: "Phase 2A (H1-only persistence summary)"

[DJI]
State: OK
AsOf:  2026-06-30
Params:
  window_len: 60
  embed_m: 3
  embed_tau: 1
  persist_thr: 0.500
  lastn: 10
Stats:
  n_obs_returns: 60
  n_embed_points: 58
  ret_vol: 0.008258
CPI Metrics (H1):
  H1_MaxPersistence: 0.437645
  H1_CountAbove_Thr: 0
  H1_Entropy: 2.379507
Assessment:
  H1_label: H1_NONE
  Note: "No meaningful H1 persistence above threshold (thr=0.500)."
Provenance:
  input: "OHLCV (Close -> log returns)"
  embedding: "delay(m=3, tau=1) over last 60 returns"
  ph: "ripser(maxdim=1) on standardized embedding"
  phase: "Phase 2A (H1-only persistence summary)"

[QQQ]
State: OK
AsOf:  2026-06-30
Params:
  window_len: 60
  embed_m: 3
  embed_tau: 1
  persist_thr: 0.500
  lastn: 10
Stats:
  n_obs_returns: 60
  n_embed_points: 58
  ret_vol: 0.014845
CPI Metrics (H1):
  H1_MaxPersistence: 0.278164
  H1_CountAbove_Thr: 0
  H1_Entropy: 2.795720
Assessment:
  H1_label: H1_NONE
  Note: "No meaningful H1 persistence above threshold (thr=0.500)."
Provenance:
  input: "OHLCV (Close -> log returns)"
  embedding: "delay(m=3, tau=1) over last 60 returns"
  ph: "ripser(maxdim=1) on standardized embedding"
  phase: "Phase 2A (H1-only persistence summary)"

[SPX]
State: OK
AsOf:  2026-06-30
Params:
  window_len: 60
  embed_m: 3
  embed_tau: 1
  persist_thr: 0.500
  lastn: 10
Stats:
  n_obs_returns: 60
  n_embed_points: 58
  ret_vol: 0.008729
CPI Metrics (H1):
  H1_MaxPersistence: 0.194210
  H1_CountAbove_Thr: 0
  H1_Entropy: 2.136403
Assessment:
  H1_label: H1_NONE
  Note: "No meaningful H1 persistence above threshold (thr=0.500)."
Provenance:
  input: "OHLCV (Close -> log returns)"
  embedding: "delay(m=3, tau=1) over last 60 returns"
  ph: "ripser(maxdim=1) on standardized embedding"
  phase: "Phase 2A (H1-only persistence summary)"

[TNX]
State: OK
AsOf:  2026-06-30
Params:
  window_len: 60
  embed_m: 3
  embed_tau: 1
  persist_thr: 0.500
  lastn: 10
Stats:
  n_obs_returns: 60
  n_embed_points: 58
  ret_vol: 0.009385
CPI Metrics (H1):
  H1_MaxPersistence: 0.314691
  H1_CountAbove_Thr: 0
  H1_Entropy: 2.493923
Assessment:
  H1_label: H1_NONE
  Note: "No meaningful H1 persistence above threshold (thr=0.500)."
Provenance:
  input: "OHLCV (Close -> log returns)"
  embedding: "delay(m=3, tau=1) over last 60 returns"
  ph: "ripser(maxdim=1) on standardized embedding"
  phase: "Phase 2A (H1-only persistence summary)"

[VIX]
State: OK
AsOf:  2026-06-30
Params:
  window_len: 60
  embed_m: 3
  embed_tau: 1
  persist_thr: 0.500
  lastn: 10
Stats:
  n_obs_returns: 60
  n_embed_points: 58
  ret_vol: 0.075414
CPI Metrics (H1):
  H1_MaxPersistence: 0.123703
  H1_CountAbove_Thr: 0
  H1_Entropy: 2.275253
Assessment:
  H1_label: H1_NONE
  Note: "No meaningful H1 persistence above threshold (thr=0.500)."
Provenance:
  input: "OHLCV (Close -> log returns)"
  embedding: "delay(m=3, tau=1) over last 60 returns"
  ph: "ripser(maxdim=1) on standardized embedding"
  phase: "Phase 2A (H1-only persistence summary)"
