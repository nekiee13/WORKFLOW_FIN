Focus hard. Your tasks are:
1. Prepare final rankings for reports R1 to R==N== (N = total number of evaluated reports;
   use every report that appears in the batch evaluations supplied above — do not assume six).
2. Make a detailed summary. Focus only on the weaknesses of each report.

Cross-batch reconciliation (HARD):
- The batch evaluations above were scored in separate sessions. Do NOT merge them by
  naive concatenation of scores.
- For each adjacent pair in the final ranking whose reports come from DIFFERENT batches,
  add one sentence justifying that order using their W3B scorecards and weakness tables
  (e.g., completeness status, count and severity of deductions).
- If a report labeled "materially compressed" ranks above one labeled "broadly complete",
  the justification sentence is mandatory and must name the specific deductions that
  outweigh completeness.

Here is the requested output format (see draft below; extend all tables to R==N==):

"""

# Summary

| Report |                          File | Total chars | Structure status      | Main finding                               |
| ------ | ----------------------------: | ----------: | --------------------- | ------------------------------------------ |
| R1     |                    `<file 1>` |       ..... | ....                  | ....                                       |
| R2     |                    `<file 2>` |       ..... | ....                  | ....                                       |
| ...    |                           ... |         ... | ...                   | ...                                        |
| R==N== |                  `<file N>`   |       ..... | ....                  | ....                                       |

## Ranking
#1: R_ (score/100)
#2: R_ (score/100)
...
#==N==: R_ (score/100)
(one reconciliation sentence after each adjacent cross-batch pair)

## Reasoning Hierarchy Score

| Dimension            |  R1  |  R2  |  ...  | R==N== |
| -------------------- | ---- | ---- | ----- | ------ |
| Deductive discipline |      |      |       |        |
| Inductive support    |      |      |       |        |
| Causal restraint     |      |      |       |        |
| Synthesis            |      |      |       |        |
| Completeness         |      |      |       |        |
| Traceability         |      |      |       |        |
| Decision usefulness  |      |      |       |        |

## Weaknesses (per report)


"""
Perform the requested tasks to your full capacity. Proceed.
