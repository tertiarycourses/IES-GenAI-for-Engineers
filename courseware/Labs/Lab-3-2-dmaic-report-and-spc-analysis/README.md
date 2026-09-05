# Lab 3.2 DMAIC report and SPC analysis

IES | 25 minutes | LO1, LO2, LO3

All records are fictional training data. They describe no actual facility, person or organisation. Values are teaching assumptions, not approved design criteria. Do not use outputs to operate, maintain or approve real equipment.

## Files

Open Lab-Handout.pdf, prompts.md and the files in mock-data. Each lab is self-contained; earlier outputs may be reused but are not required. Save your work under outputs.

## Procedure

1. Open process-data.csv in Excel and save as a workbook. Baseline samples are 1-30 (rows 2-31); samples 31-35 are monitoring data. Fill volume is in litres. Confirm all 35 records are present and numeric.

2. Create column F called MR. Leave F2 blank; in F3 enter =ABS(B3-B2) and fill through F31 only for the baseline estimate. In H2 enter =AVERAGE(B2:B31); H3 =AVERAGE(F3:F31); H4 =H3/1.128; H5 =H2-3*H4; H6 =H2+3*H4.

3. Create an individuals line chart in sample order for all 35 values. Add constant series for the baseline mean, LCL and UCL from H2, H5 and H6. Do not recompute limits using the monitoring signal. Label litres, sample order and baseline window.

4. Calculate teaching Cp in H7 =(10.6-9.4)/(6*H4) and Cpk in H8 =MIN(10.6-H2,H2-9.4)/(3*H4). Treat these as provisional estimates: the small baseline, stability, independence, distribution and measurement system need review. A Cp value alone cannot establish stability.

5. Open defects.csv. Sort counts descending and compute cumulative share using =SUM($B$2:B2)/SUM($B$2:$B$5), filling down. Ask Copilot for a Pareto interpretation, fishbone hypotheses and a 5-Whys chain with evidence requests, not asserted causes.

6. Use dmaic-template.md to assemble a concise report in Word, then a management-summary slide in PowerPoint. Record the monitoring signal, a proposed trial and a control plan. Compare calculations with expected-output.md before accepting the AI analysis.

## Acceptance checks

- Baseline n=30, monitoring n=5; sample 33 signals above UCL.
- Cp and Cpk use the stated within-process estimate and the 9.4-10.6 L teaching limits.
- Pareto top two categories total 66.7%; causation is unproven.

## If access is unavailable

Use approved paired access or the local source files to prepare a draft and configuration blueprint. Record live agent or permission tests as not executed. Do not use personal accounts to bypass organisational controls.

## Petroleum transfer pathway (v1.1)

Petroleum transfer pathway: choose this scenario instead of the original lab within the same time allocation. Additional explanations are reference reading. All petroleum records, limits, outputs and scores here are original fictional teaching examples; no operating action is authorised.

[Open the petroleum lab variant](Petroleum-Variant.md), [PDF handout](Petroleum-Variant.pdf) and [prompts](petroleum-prompts.md). Inputs are self-contained in petroleum-data.
