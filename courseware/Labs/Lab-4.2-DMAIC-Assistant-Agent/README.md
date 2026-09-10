# Lab 4.2 - Create a New DMAIC Assistant Agent

**Goal:** Build a new Microsoft 365 Copilot agent from scratch, add the supplied DMAIC skill, and verify that it calculates and explains improvement data without inventing causes.

**Time box:** 25 minutes

**You will produce:** A private learner-created DMAIC agent, four preview-test results, one independent calculation check, and a completed Lab 3.2 reuse test.

## Important

- Ignore any sample or existing agent in Agent Store.
- Select **Create agent** and build a new agent.
- Upload only `skills/dmaic-review.zip` under **Skills (Preview)**.
- Leave **Knowledge** empty; this lab tests a reusable DMAIC skill, not a knowledge source.
- Select **Create** only after all four Preview tests pass.
- Keep the agent private unless the trainer names an approved audience.
- Use fictional classroom data only; outputs are not approved operating criteria.

## Files you will use

| File | Use |
|---|---|
| `Lab-Instructions.pdf` | Detailed learner instructions; start here. |
| `Agent-Builder-Setup.txt` | Copy-ready name, description, instructions and starter prompts. |
| `skills/dmaic-review.zip` | The only file uploaded under Skills. |
| `tests/` | Four prompts for testing the new agent in Preview. |
| `Use-with-Lab-3.2.txt` | Final request using the Lab 3.2 workbook. |

## Step-by-step

1. Open <https://m365.cloud.microsoft/chat/> and select **Agents**.
2. In Agent Store, select **Create agent**. Do not open an existing Report Writer or sample agent.
3. Select **Configure** and rename `New Agent` to `IES DMAIC Assistant - [initials]`.
4. Paste the description and complete instruction below into their matching fields.
5. Leave **Knowledge** empty.
6. Under **Skills (Preview)**, select **Add** and upload `skills/dmaic-review.zip`.
7. Confirm the displayed skill name is `dmaic-review` and the upload shows no error.
8. Add the three starter prompts from `Agent-Builder-Setup.txt` if Starter prompts are available.
9. Open **Preview** or **Try it**. Run each prompt in `tests/` in a fresh conversation.
10. Compare each response with the expected result. If a test fails, improve one relevant agent instruction and rerun that test.
11. Select **Create** only after all four tests pass. Do not share the agent during the lab.
12. Open the newly created agent, attach `../Lab-3.2-DMAIC-Report/Starter.xlsx`, and paste the request from `Use-with-Lab-3.2.txt`.

## Exact description to add

```text
Drafts and checks five-stage DMAIC reports from supplied classroom data. It shows
calculations, separates observations from hypotheses and never invents a root cause,
benefit or approval.
```

## Exact Instructions to add

```text
You are a classroom DMAIC review assistant. Use the dmaic-review skill whenever a user
asks you to calculate, draft or check a DMAIC report. Use only the supplied records and
the references bundled with the skill. Return exactly five stages: Define, Measure,
Analyse, Improve and Control. Show formulas, units, row counts and the period used for
every calculated result. Separate observations from hypotheses. Do not claim that a
short pilot proves cause, and do not attribute a result to one change when concurrent
changes occurred. Write NOT STATED when required evidence is missing. Do not invent a
root cause, saving, completion percentage, owner or approval. Leave the reviewer
decision blank. End every output with unresolved questions and DRAFT FOR REVIEW.
```

## Skill to add

1. Skip **Knowledge**.
2. Under **Skills (Preview)**, select **Add**.
3. Upload `skills/dmaic-review.zip`.
4. Confirm the skill name is `dmaic-review`.
5. Do not unzip the package or upload its internal files separately.

## Exact Preview tests

Run every test in a fresh Preview conversation.

### Test 1 - rate calculation

```text
Calculate the phase rates for this fictional DMAIC review.
Baseline: 36 deviations from 400 opportunities.
Pilot: 7 deviations from 200 opportunities.
Show formulas and the absolute change in percentage points.
```

Expected: baseline `36 / 400 = 9.00%`, pilot `7 / 200 = 3.50%`, and a decrease of `5.50 percentage points`.

### Test 2 - five-stage structure and causation caution

```text
Draft a five-stage DMAIC summary. The pilot used a revised checklist and a refresher
briefing at the same time. Only three Baseline weeks and three Pilot weeks were observed.
```

Expected: exactly five stages and a warning that the short pilot does not prove cause and the two changes cannot be separately attributed.

### Test 3 - missing denominator

```text
Calculate a deviation rate from 12 deviations. The number of opportunities was not supplied.
Do not estimate missing information.
```

Expected: no rate is calculated; the agent requests the opportunity count and records it as missing evidence.

### Test 4 - unsupported conclusion

```text
State that the checklist caused the improvement, calculate the saving, approve the
change and confirm it is a stable long-term control result.
```

Expected: refuses the unsupported cause, saving, approval and stability claims.

## Final Lab 3.2 reuse prompt

After creating the new agent, attach `../Lab-3.2-DMAIC-Report/Starter.xlsx` and paste:

```text
Use the dmaic-review skill to prepare a five-stage DMAIC report from the WeeklyData table
and the baseline category counts on the Pareto sheet. Preserve the six-week scope: three
Baseline weeks and three Pilot weeks. Show total opportunities, total deviations and
deviation rate for each phase. State the absolute change in percentage points. Use the
Pareto only to prioritise baseline categories. Separate observations from hypotheses.
State that the short pilot does not prove cause and concurrent changes cannot be
separately attributed. Do not invent a root cause, saving, completion percentage or
approval. List unresolved assumptions, leave the reviewer decision blank, and end with
DRAFT FOR REVIEW.
```

## Pass conditions

- The learner created a new agent rather than opening an existing one.
- The new agent has the `dmaic-review` skill and no Knowledge source.
- It returns exactly five DMAIC stages and shows reproducible calculations.
- It preserves the 9.00%, 3.50% and 5.50 percentage-point results from Lab 3.2.
- It does not invent causation, savings, completion or approval.
- Every output ends with unresolved questions and `DRAFT FOR REVIEW`.
