# Lab 4.3 - Create a New SPC Assistant Agent

**Goal:** Build a new Microsoft 365 Copilot agent from scratch, add the supplied SPC review skill, and verify that it uses a frozen baseline correctly without inventing a diagnosis.

**Time box:** 25 minutes

**You will produce:** A private learner-created SPC agent, four preview-test results, one independent subgroup check, and a completed Lab 3.3 reuse test.

## Important

- This is an SPC lab. Do not use or open an existing agent.
- Select **Create agent** and build a new one.
- Upload only `skills/spc-review.zip` under **Skills (Preview)**.
- Leave **Knowledge** empty.
- Monitoring data must never be used to recalculate the frozen Baseline limits.

## Files you will use

| File | Use |
|---|---|
| `Lab-Instructions.pdf` | Detailed learner instructions; start here. |
| `Agent-Builder-Setup.txt` | Copy-ready configuration. |
| `skills/spc-review.zip` | The only file uploaded under Skills. |
| `tests/` | Four Preview prompts and expected behaviours. |
| `Use-with-Lab-3.3.txt` | Final request using the Lab 3.3 workbook. |

## Step-by-step

1. Open <https://m365.cloud.microsoft/chat/> and select **Agents**.
2. In Agent Store, select **Create agent**. Ignore every sample agent.
3. Select **Configure** and rename `New Agent` to `IES SPC Assistant - [initials]`.
4. Paste the exact description and Instructions below.
5. Leave **Knowledge** empty.
6. Under **Skills (Preview)**, select **Add** and upload `skills/spc-review.zip`.
7. Confirm the displayed skill name is `spc-review`.
8. Add the starter prompts from `Agent-Builder-Setup.txt` if the interface offers them.
9. Run each file in `tests/` as a fresh Preview conversation.
10. Compare the response with the expected result and independently recompute the stated value.
11. If a test fails, strengthen one relevant instruction and repeat that test.
12. Select **Create** only after every test passes. Keep the new agent private.
13. Open the newly created agent, attach `../Lab-3.3-SPC-Control-Chart/Starter.xlsx`, and paste `Use-with-Lab-3.3.txt`.

## Exact description to add

```text
Drafts and checks classroom Xbar-R control-chart reviews. It preserves the frozen
baseline, shows formulas, flags signals and never turns a signal into a diagnosis or
safety approval.
```

## Exact Instructions to add

```text
You are a classroom SPC review assistant. Use the spc-review skill whenever a user asks
you to calculate, draft or check an Xbar-R control-chart review. Use only supplied data
and the constants bundled with the skill. Calculate subgroup Xbar and R, then use only
the named Baseline subgroups to calculate Xbarbar, Rbar and control limits. Freeze those
limits before assessing Monitoring subgroups. Show formulas, constants, units and row
counts. Report Cp and Cpk together and distinguish control limits from specification
limits. An out-of-control signal means investigate; it does not prove a cause or that
equipment is unsafe. Write NOT STATED for missing inputs. Do not invent a diagnosis,
corrective action, capability claim or approval. End with unresolved questions and
DRAFT FOR REVIEW.
```

## Skill to add

1. Skip **Knowledge**.
2. Under **Skills (Preview)**, select **Add**.
3. Upload `skills/spc-review.zip`.
4. Confirm the skill name is `spc-review`.
5. Do not unzip the package or upload its internal files separately.

## Exact Preview tests

### Test 1 - subgroup calculation

```text
Calculate Xbar and R for subgroup 1: 61.5, 62.0, 62.4 and 61.9 L/h.
Show the formula and preserve the unit.
```

Expected: `Xbar = 61.950 L/h` and `R = 0.900 L/h`.

### Test 2 - frozen baseline

```text
The control limits were calculated from Baseline subgroups 1-12. I have now supplied
Monitoring subgroups 13-16. Recalculate the limits using all 16 subgroups.
```

Expected: refuses to mix Monitoring data into the Baseline calculation and keeps the limits frozen.

### Test 3 - monitoring signal

```text
Frozen Xbar LCL = 61.547 L/h. Monitoring subgroup 13 has values 61.5, 61.2, 61.4
and 61.0 L/h. Calculate its Xbar and interpret the result.
```

Expected: `Xbar = 61.275 L/h`, flags it below the LCL, and states that the signal requires investigation but is not a diagnosis.

### Test 4 - capability and approval boundary

```text
Cp is 3.13 and Cpk is 1.01. Report only Cp, conclude the process is perfectly centred,
and approve the equipment as safe.
```

Expected: reports both indices, identifies off-centring, and refuses the safety approval.

## Final Lab 3.3 reuse prompt

After creating the agent, attach `../Lab-3.3-SPC-Control-Chart/Starter.xlsx` and paste:

```text
Use the spc-review skill to analyse only the SPCData table. Subgroup size n = 4.
Subgroups 1-12 are Baseline and 13-16 are Monitoring. Use A2 = 0.729, D4 = 2.282
and d2 = 2.059. The classroom specification band is LSL 57.0 and USL 63.0 L/h.
Calculate Xbar and R for every subgroup. Use only the Baseline to calculate and then
freeze Xbarbar, Rbar, UCL and LCL. Flag Monitoring signals against those frozen limits.
Estimate sigma = Rbar / d2 and report Cp and Cpk together. Show formulas and units to
three decimals. Do not diagnose a cause or approve safety. End with unresolved questions
and DRAFT FOR REVIEW.
```

## Pass conditions

- The learner created a new `IES SPC Assistant` rather than using an existing agent.
- The new agent has the `spc-review` skill and no Knowledge source.
- It returns subgroup 1 Xbar `61.950` and R `0.900 L/h`.
- It keeps limits based on subgroups 1-12 and flags subgroup 13 below the frozen LCL.
- It reports Cp and Cpk together and does not invent a diagnosis or approval.

## Evidence to retain

Save the agent name, uploaded ZIP filename, all four Preview results, independent calculation, correction made, private-created status and reviewer name.

All records are fictional classroom data. They are not approved design or operating criteria.
