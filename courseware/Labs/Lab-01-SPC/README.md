# Copilot in Excel: data quality and SPC

140 minutes | IES | Original synthetic CW-401 engineering case. Values and limits are fictional teaching assumptions, not plant operating instructions. Generated references are independently calculated examples, not recorded Copilot executions.

Open Starter.xlsx. Lab-Handout.pdf contains the full procedure; prompts.md and the workbook Prompts sheet contain the prompts. Attempt the lab before opening Worked-Reference.xlsx. All source files are local in mock-data.

## 1 Prepare the workbook

Save a working copy of Starter.xlsx to your approved OneDrive or SharePoint location. Open it in Excel with your work/school account and use the Copilot side pane. Select the named table before prompting. If Copilot cannot edit, request the formula and insert it manually; record the fallback. Confirm tenant entitlement and supported workbook format before class. Keep the local raw files unchanged. Open ReadMe, Parameters, RawTests and Prompts. The workbook starts with source tables and blank output sheets.

## 2 Audit without deleting evidence

Select RawTests and submit prompt SPC1 from Prompts. Inspect TEST-068 (missing volume), TEST-083 (110-second invalid test) and duplicate TEST-088. Keep one copy of the duplicate; exclude the two invalid tests from the comparable analysis. Retain121 raw rows,120 unique tests and118 valid tests. Write decisions into QualityAudit.

## 3 Build the analysis table

Ask Copilot to filter and sort the valid unique records into Analysis. ValidTests is the prepared comparison source if cleaning stalls. Keep test_id, timestamp, phase, shift, pump, collected_L and differential pressure. Add delivery_L_h using collected_L*3600/Parameters duration. Spot-check one baseline and one monitoring row with a calculator.

## 4 Calculate a fixed baseline

Submit SPC2. Only60 baseline records estimate the centre and moving ranges. First baseline MR is blank; next59 are absolute successive differences. Mean62.00250 L/h; MRbar0.73881; sigma0.65498; LCL60.03757; UCL63.96743. Compare formulas with the reference after attempting the task.

## 5 Chart process behaviour

Submit SPC3. Use time order and phase labels; add constant mean, UCL and LCL series. Keep baseline limits for monitoring and pilot. There are28 valid monitoring and30 pilot tests. Seventeen monitoring points TEST-073–090 except083 are outside the limits. The missing record and invalid duration remain in the quality ledger.

## 6 Discuss capability and evidence

Submit SPC4. Conditional baseline Cp1.57766 and Cpk1.57639 use supplied specs. Check baseline behaviour and measurement assumptions before interpreting them. Do not transfer that conclusion to the shifted monitoring period. Note the differential-pressure association and the two changes before pilot; neither establishes a sole cause.

## 7 Retain the result

Save your workbook, prompts, chart, quality decisions, checks and a100-word interpretation. Record what Copilot actually did and what you calculated manually. Use the lab evaluation checklist and compare with the worked reference only after your attempt.