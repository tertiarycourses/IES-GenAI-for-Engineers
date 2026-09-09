# Lab 4.3 - Minutes to Progress Report

**Purpose:** Convert explicit meeting decisions into an action tracker and progress report without inventing commitments.

**Output:** A checked action table and a short status report with evidence gaps.

## What you will do

1. Open the supplied meeting-record CSV.
2. Ask Copilot to extract only explicit actions, owners, dates and status.
3. Mark every missing field as NOT STATED.
4. Separate completed actions from planned or blocked work.
5. Generate a concise progress report from the checked action table.
6. Verify every report claim against the original record.
7. Correct one unsupported inference and retain the evidence.

## Files used

| File | Use |
|---|---|
| `Lab-Instructions.pdf` | Detailed instructions. |
| `mock-data.csv` | Fictional meeting action records. |

## Detailed steps

1. Open `mock-data.csv`. Read every row before using Copilot.
2. Open Copilot Chat or Word. Attach the CSV, or paste its contents if attachment is unavailable.
3. Paste this extraction request:

```
Use only the supplied meeting records. Create an action table with Action ID,
exact action wording, owner, due date, status, evidence and source row.
Do not infer an owner, deadline, completion or approval. Write NOT STATED for
every missing field. List ambiguities after the table.
```

4. Compare every action-table cell with the source. Correct paraphrases that change the commitment.
5. Confirm that a due date is not treated as evidence of completion.
6. Paste this second request:

```
Using only the checked action table, draft a progress report with:
Reporting period, Completed, In progress, Blocked, Next actions,
Unresolved information and blank Reviewer decision.
Preserve every action ID, owner, date, status and evidence reference.
End with DRAFT FOR REVIEW.
```

7. Trace every sentence in the report back to an action-table row.
8. If the report invents progress, add a precise correction such as: `ACT-03 is planned, not completed; move it to Next actions.`
9. Rerun the affected section and save the before-and-after evidence.

## Independent checks

- The number of action-table rows must equal the number of supplied action records.
- Any missing owner or due date must remain NOT STATED.
- A plan, due date or discussion is not evidence that work is complete.

## Pass conditions

- Every action has a source-row trace.
- Owners, due dates and statuses are preserved exactly.
- Missing fields are visible.
- Completed, in-progress and blocked work are separated.
- Reviewer decision remains blank.
- The report ends with DRAFT FOR REVIEW.

All supplied records are fictional classroom data.
