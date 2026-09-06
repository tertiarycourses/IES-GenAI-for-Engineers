# Classroom FMEA Rating Scale

All records here are fictional training data. They describe no actual facility, person or organisation. Values are teaching assumptions, not approved design criteria. Do not use outputs to operate, maintain or approve real equipment.

## Severity (S)

| Rating | Meaning |
|---|---|
| 1-2 | No or barely noticeable effect on function. |
| 3-4 | Minor loss of function; operator notices, no safety impact. |
| 5-6 | Partial loss of function; output degraded, rework needed. |
| 7-8 | Major loss of function; unplanned shutdown, possible regulatory report. |
| 9-10 | Potential safety or environmental harm, or loss of a protective function. |

## Occurrence (O)

| Rating | Meaning |
|---|---|
| 1-2 | Not known to have occurred on comparable equipment. |
| 3-4 | Isolated occurrences on comparable equipment. |
| 5-6 | Occasional; recurs over the life of the asset. |
| 7-8 | Frequent; recurs within a maintenance cycle. |
| 9-10 | Near certain; recurs within normal operating periods. |

## Detection (D)

Detection is inverted: a HIGH rating means detection is POOR.

| Rating | Meaning |
|---|---|
| 1-2 | Automatic detection before any effect reaches the process. |
| 3-4 | Automatic alarm with clear operator response. |
| 5-6 | Routine inspection or scheduled test likely to find it. |
| 7-8 | Only found by targeted investigation after an effect is seen. |
| 9-10 | No credible means of detection before failure. |

## Rules that must not be broken

- RPN = Severity x Occurrence x Detection. Always show this formula.
- Any row with Severity 9 or higher is escalated for separate review whatever its RPN. A low RPN never cancels a high Severity.
- RPN is a triage aid for ordering work, not a risk acceptance threshold.
- A rating may only be lowered when verified evidence of control effectiveness exists. An intended or planned action is not evidence.
- Residual ratings stay unassessed until that evidence is produced.
