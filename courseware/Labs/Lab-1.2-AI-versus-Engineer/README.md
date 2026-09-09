# Lab 1.2 - AI versus Engineer

**Purpose:** Use Copilot to organise messy engineering observations while keeping interpretation and approval with the engineer.

**Output:** A short technical brief that separates supplied facts, assumptions, unknowns and required checks.

## What you will do

1. Open `mock-data.csv` and identify the three supplied records.
2. Open Copilot Chat and attach or paste the data.
3. Paste the complete prompt included in this instruction.
4. Check every value, unit and status against the source.
5. Correct any invented limit, cause or safety conclusion.
6. Record what Copilot contributed and what still requires an engineer.

## Files used

| File | Use |
|---|---|
| `Lab-Instructions.pdf` | Detailed instructions. |
| `mock-data.csv` | The only engineering evidence allowed in this exercise. |

## Detailed steps

1. Open `mock-data.csv`. Confirm that it contains a delivery test result of 59.4 L/h, a reference target of 62.0 L/h, and no approved operating limit.
2. Open Copilot Chat at <https://m365.cloud.microsoft/chat/>.
3. Attach `mock-data.csv`. If file attachment is unavailable, paste the three data rows into the chat.
4. Paste this request:

```
Act as an engineering documentation assistant. Use only the attached classroom records.
Return four sections: Supplied facts, Assumptions, Unknowns, and Next evidence checks.
Preserve every value, unit, source and status. Do not invent an approved operating limit,
a failure cause or a safety conclusion. End with DRAFT FOR ENGINEER REVIEW.
```

5. Compare the response line by line with the CSV.
6. Confirm that 59.4 L/h is described as a test result and 62.0 L/h as a reference target.
7. Confirm that Copilot does not call the 2.6 L/h difference an operating-limit violation because the approved operating limit is not supplied.
8. If Copilot invents a cause or conclusion, add: `Remove unsupported interpretation. Mark the operating limit and cause as NOT SUPPLIED.`
9. Rerun the corrected request in a fresh message.
10. Add a final two-column note: **AI contribution** and **Engineer responsibility**.

## Independent check

Calculate the arithmetic difference yourself: `62.0 - 59.4 = 2.6 L/h`. This is only a difference from the reference target. It is not proof of non-compliance.

## Pass conditions

- All three source records are represented.
- Values, units and statuses are unchanged.
- Facts, assumptions and unknowns are visibly separated.
- No approved limit, root cause or safety decision is invented.
- The draft ends with an engineer-review boundary.

All supplied records are fictional classroom data.
