# Copilot in Excel: FMEA and risk prioritisation

Prompts are also in Starter.xlsx > Prompts. Use them in the Copilot side pane in Excel.

## FMEA1 Structure the review

Use FMEA_Input and Evidence. Create FMEA_Review with function, mode, effect, potential cause, current control, evidence, supplied provisional S/O/D, RPN, action, owner and status. Keep the six mode IDs. Separate actual observations from prospective scenarios. Use ScoringNote for definitions and do not infer occurrence ratings from the short test series.

## FMEA2 Calculate and prioritise

Add an Excel formula RPN=S*O*D for every row. Sort a view by RPN descending while preserving mode IDs and source rows. Add a separate high-severity review flag for S>=9. Create an RPN column chart. Do not treat rank or low RPN as evidence of safety acceptance.

## FMEA3 Challenge with personas

Simulate reliability, operations and safety review lenses. First return one separate evidence-based concern per role. Run two concise challenge/response rounds, citing mode IDs and evidence records. A moderator returns agreed revisions, unresolved disagreement and missing evidence. Do not force consensus or invent approval. Keep residual ratings unassessed until action-effectiveness evidence exists.