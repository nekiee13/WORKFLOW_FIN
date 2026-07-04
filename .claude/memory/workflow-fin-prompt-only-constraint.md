---
name: workflow-fin-prompt-only-constraint
description: "Hard constraint — all WORKFLOW_FIN upgrades must be prompt-only; no scripts, pipeline code, or changes to upstream data generation"
metadata: 
  node_type: memory
  type: feedback
  originSessionId: c0fe27a1-20bf-43c4-a4d1-9f53775d4a06
---

All upgrades to the WORKFLOW_FIN forecast workflow must be **prompt-related only** — edits to the markdown prompt documents. No scripts, no pipeline code, no changes to how upstream data files (13_SVL, 14_TDA, 15_fh3) are generated.

**Why:** the user stated "all upgrades must be prompt related. Non-code upgrades. We are working only on the prompts in this workflow" (2026-07-04), after the first draft of [[workflow-fin-bottleneck-diagnosis]]'s plan included pipeline scripting phases.

**How to apply:** (1) FINAL RULE (settled 2026-07-04 after two withdrawn designs): *computation is allowed ONLY for data missing from the provided inputs* (10_Calculations, 13_SVL, 14_TDA, 15_fh3). Everything present in inputs is quoted, never recomputed. The missing derived quantities (median/MAD/MAD_floor/outlier tests/dispersion test/percentile positions/Range/placement markers/ATR%/pivot proximity) are computed once in the mandatory in-report CALC WORKSHEET (global block 9 in 29, fixed 15-row QUOTE/COMPUTE schema, operands shown, nearest-rank percentiles) and quoted everywhere else. The user will NOT prepare additional data files — a user-filled 27_DERIVED_METRICS template was explicitly rejected and deleted; LLM-side separate worksheet *prompts* were also rejected. (2) convert conditional rules into unconditional mandatory tables; (3) embed authoritative reference data (NYSE holiday calendar, indicator band definitions) verbatim in prompts; (4) make rules conditional on data actually present ("IF field present → rule, ELSE fixed fallback sentence"). Never propose changing 14_TDA/15_fh3 output — write prompt rules that degrade gracefully around what those files actually contain. Edits go to TEMPLATES (17, 29, 70-series, 90), never to user-prepared instances (16, 28). Reports 61–66 and the 99*/90/91 docs are illustrative examples only — never treat their file-level quirks as workflow issues.
