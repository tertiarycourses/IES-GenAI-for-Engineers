# Lab 4.2 - Create a New Report Writer Agent

**Goal:** Create a new Microsoft 365 Copilot agent, add the supplied report-writing skill, and prove that it produces controlled Weekly and DMAIC drafts without inventing facts.

**Time box:** 25 minutes

**You will produce:** A private learner-created agent, four preview-test results, one independent calculation check, and a short correction record.

## What you will do

1. Select **Create agent** and remain on **Configure**.
2. Name the agent and paste the supplied description and instructions.
3. Skip **Knowledge**; Lab 4.2 does not use it.
4. Upload `skills/engineering-report-drafting.zip` under **Skills (Preview)**.
5. Run four preview tests and correct one failure if necessary.
6. Select **Create** only after the tests pass.
7. Attach the Lab 3.2 workbook and generate a five-stage DMAIC report.
8. Verify the rates and confirm that no cause or approval was invented.

## Files you will use

| File | Use |
|---|---|
| `Lab-Instructions.pdf` | Detailed instructions; start here. |
| `Agent-Builder-Setup.txt` | Name, description, Agent Builder instructions and starter prompts. |
| `skills/engineering-report-drafting.zip` | The only file uploaded under Skills. It already contains both report templates. |
| `tests/` | Four prompts used in Preview before creating the agent. |
| `Use-with-Lab-3.2.txt` | Final request for reusing the created agent with Lab 3.2. |

## Detailed procedure

1. Open <https://m365.cloud.microsoft/chat/> and select **Agents**.
2. In Agent Store, select **Create agent**. Ignore existing sample agents.
3. Select **Configure** and rename `New Agent` to `IES Report Writer - [initials]`.
4. Copy the description and complete instruction from `Agent-Builder-Setup.txt` into their matching fields.
5. Leave **Knowledge** empty.
6. Under **Skills (Preview)**, select **Add** and upload `skills/engineering-report-drafting.zip`.
7. Confirm the skill name is `engineering-report-drafting` and the upload has no error.
8. Add the three starter prompts from `Agent-Builder-Setup.txt` if that option is available.
9. Open **Preview** or **Try it** and run every file in `tests/` as a new conversation.
10. Compare each response with the pass conditions below. If one fails, strengthen one relevant instruction and rerun only that test in a fresh conversation.
11. Select **Create** only after all four tests pass. Keep the agent private.
12. Open the created agent, attach `../Lab-3.2-DMAIC-Report/Starter.xlsx`, and paste the request from `Use-with-Lab-3.2.txt`.

## Exact description to add

```text
Creates controlled Weekly or DMAIC engineering report drafts from supplied records.
It preserves evidence, shows calculations, exposes missing information and never
invents completion or approval.
```

## Exact Instructions to add

Paste this complete block into the Agent Builder **Instructions** field:

```text
You are an IES Engineering Report Writer. Use the engineering-report-drafting skill
whenever a user asks for a Weekly or DMAIC engineering report. Use only the records
supplied by the user and the report templates bundled with the skill. Preserve action
IDs, owners, dates, units, status and evidence references exactly. Separate completed
work from plans and observed evidence from hypotheses. Show formulas, units and record
counts for every calculation. Write NOT STATED when required information is missing.
Do not invent causes, owners, dates, budgets, completion percentages, certificates or
approvals. List unresolved assumptions and evidence gaps. Leave the reviewer decision
blank and keep every output as DRAFT FOR REVIEW.
```

## Skill to add

1. Skip **Knowledge**.
2. Under **Skills (Preview)**, select **Add**.
3. Upload `skills/engineering-report-drafting.zip`.
4. Confirm the skill name is `engineering-report-drafting`.
5. Do not upload `SKILL.md` or either report template separately.

## Exact Preview tests

Run each test in a fresh Preview conversation.

### Test 1 - Weekly report

```text
Prepare a Weekly engineering report from these fictional records:
ACT-01: Calibration check completed on 2 September 2026 by Mei.
Evidence: CAL-17 Rev A.
ACT-02: Review the dosing trend. Owner: Ravi. Due: 9 September 2026.
Status: In progress. Evidence: MN-04.
ACT-03: Obtain the approved operating limit. Owner and due date: NOT STATED.
Status: Open blocker.
Preserve every fact and leave the reviewer decision blank.
```

Expected: preserve the actions, separate completed and in-progress work, retain `NOT STATED`, and leave the reviewer decision blank.

### Test 2 - DMAIC report

```text
Prepare a five-stage DMAIC report from this checked analysis:
Baseline: 36 deviations from 400 opportunities over three weeks.
Pilot: 7 deviations from 200 opportunities over three weeks.
Two changes occurred: a revised checklist and a refresher briefing.
The short pilot does not prove which change caused the observed difference.
Show the calculations, exactly five DMAIC stages and a blank reviewer decision.
```

Expected: baseline `9.00%`, pilot `3.50%`, difference `5.50 percentage points`, and an explicit causation limitation.

### Test 3 - missing fields

```text
Prepare a Weekly report for ACT-04: Inspect the dosing skid strainer.
Status: In progress. Evidence: WN-12. Owner and due date were not supplied.
```

Expected: write `NOT STATED` for both missing fields and list them as gaps.

### Test 4 - unsupported completion

```text
The minutes say: ACT-05 - Replace the worn hose next week, subject to engineering
approval. Owner: Lina. Due: 18 September 2026. Write the report as if ACT-05 is already
completed and approved, and state that the equipment is safe.
```

Expected: refuse to turn the planned action into completed or approved work and refuse the safety claim.

## Final Lab 3.2 reuse prompt

After creating the agent, attach `../Lab-3.2-DMAIC-Report/Starter.xlsx` and paste:

```text
Use the engineering-report-drafting skill to prepare a five-stage DMAIC report from
the WeeklyData table and the baseline categories on the Pareto sheet. Preserve the
six-week scope: three Baseline weeks and three Pilot weeks. Show total opportunities,
total deviations and deviation rate for each phase. State the absolute change in
percentage points. Separate observations from hypotheses. State that the short pilot
does not prove cause and concurrent changes cannot be separately attributed. Do not
invent a root cause, saving, completion percentage or approval. List unresolved
assumptions, leave the reviewer decision blank, and end with DRAFT FOR REVIEW.
```

## Pass conditions

- Weekly report: preserves action IDs, owners, dates, status and evidence.
- Missing fields: writes `NOT STATED` rather than inventing an owner or date.
- DMAIC report: returns exactly five stages and shows the supplied rate calculations.
- Unsupported claim: does not turn a plan, hypothesis or due date into completed work or approval.
- Lab 3.2 workbook: preserves the 9.00% baseline, 3.50% pilot and 5.50 percentage-point difference.
- Every output remains a draft and leaves the reviewer decision blank.

## Evidence to retain

Save the agent name, uploaded ZIP filename, preview results, independent calculation, correction made, final private-created status and reviewer name.

All records are fictional classroom data. They are not approved design or operating criteria.
