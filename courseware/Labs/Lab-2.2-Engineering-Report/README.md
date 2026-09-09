# Lab 2.2 - Engineering Report

**Purpose:** Use Copilot in Word to convert inspection records into a controlled report without mixing observation, interpretation and recommendation.

**Output:** A draft report with source records, observations, limitations, actions and reviewer fields.

## What you will do

1. Open the supplied CSV and a blank Word document.
2. Ask Copilot for a fixed report structure.
3. Verify all values, units, sources and statuses.
4. Separate observation from interpretation.
5. Mark missing criteria and evidence.
6. Correct one unsupported statement.
7. Save the report as a draft for review.

## Files used

| File | Use |
|---|---|
| `Lab-Instructions.pdf` | Detailed instructions. |
| `mock-data.csv` | The only inspection evidence used. |

## Detailed steps

1. Open `mock-data.csv` and identify the delivery result, reference target and missing approved limit.
2. Open Word and create **CW-401 Delivery Check - Draft Engineering Report**.
3. Open Copilot in Word and attach or paste the CSV.
4. Paste this request:

```
Use only the supplied classroom records. Draft these sections:
Scope, Source records, Observations, Interpretation and limitations,
Recommended evidence checks, Action table, and Reviewer decision.
Preserve all dates, values, units, sources and statuses. Keep observations separate
from interpretation. Do not invent an approved limit, failure cause, owner, due date
or approval. Write NOT SUPPLIED where evidence is absent. Leave Reviewer decision blank.
```

5. In **Observations**, require factual statements only: 59.4 L/h was recorded; 62.0 L/h is the reference target; the approved limit is absent.
6. In **Interpretation and limitations**, allow the arithmetic difference but not a compliance or safety conclusion.
7. Check the action table. Unknown owners and dates must remain NOT SUPPLIED.
8. Find one unsupported or ambiguous statement. Use a follow-up prompt that names exactly what must change.
9. Reread the revised paragraph against the source.
10. Save the final result with **DRAFT FOR ENGINEER REVIEW**.

## Independent check

`62.0 - 59.4 = 2.6 L/h`. This supports a numerical comparison only. It does not establish a deviation from an approved operating limit.

## Pass conditions

- Observations are traceable to the CSV.
- Interpretation is in a separate section.
- Units and source statuses are unchanged.
- Missing criteria, owners and dates are visible.
- Reviewer decision remains blank.
- No cause, compliance finding or approval is invented.

All supplied records are fictional classroom data.
