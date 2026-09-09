# Lab 2.1 - Technical Specification

**Purpose:** Use Copilot in Word to turn supplied requirements into measurable draft clauses while exposing missing acceptance criteria.

**Output:** A draft specification table and verification checklist.

## What you will do

1. Open `mock-data.csv` and a blank Word document.
2. Add a clear specification title and source note.
3. Give Copilot the supplied records and the RISE prompt.
4. Generate measurable draft clauses.
5. Check every number, unit and acceptance method.
6. Mark unsupported limits as NOT SUPPLIED.
7. Revise one weak clause and retain the correction.

## Files used

| File | Use |
|---|---|
| `Lab-Instructions.pdf` | Detailed instructions. |
| `mock-data.csv` | Classroom requirement evidence. |

## Detailed steps

1. Open `mock-data.csv` and confirm the three data rows.
2. Open Word and create a blank document titled **CW-401 Dosing Skid - Draft Technical Specification**.
3. Add this source note: `Source: synthetic classroom case; approved operating limit not supplied.`
4. Open Copilot in Word. Attach the CSV if supported; otherwise paste its contents under the source note.
5. Paste this request:

```
ROLE: Act as a technical specification editor supporting a competent engineer.
INPUT: Use only the supplied CW-401 classroom records.
STEPS: Draft a table with Requirement ID, shall statement, value and unit,
acceptance method, source, and unresolved gap.
EXPECTATIONS: Preserve 59.4 L/h and 62.0 L/h exactly. Do not convert the reference
target into an approved operating limit. Where a limit or test criterion is absent,
write NOT SUPPLIED. End with DRAFT FOR ENGINEER REVIEW.
```

6. Inspect every **shall** statement. A clause is measurable only if its value, unit, condition and acceptance method are supported.
7. Reject any clause that says the skid **shall operate at 62.0 L/h** unless the source explicitly identifies 62.0 L/h as an approved requirement. Here it is only a reference target.
8. Select one vague clause and revise it so the missing criterion is visible rather than guessed.
9. Add a verification checklist covering source, unit, test method, acceptance criterion and approving role.
10. Save the document as a draft.

## Independent checks

- The supplied difference is `62.0 - 59.4 = 2.6 L/h`.
- The approved operating limit remains NOT SUPPLIED.
- A reference value is not silently converted into a binding requirement.

## Pass conditions

- Each draft clause is traceable to a supplied record.
- Every stated value has its correct unit.
- Unsupported acceptance limits remain visible as gaps.
- The output includes a verification checklist and draft status.
- No clause is represented as approved.

All supplied records are fictional classroom data.
