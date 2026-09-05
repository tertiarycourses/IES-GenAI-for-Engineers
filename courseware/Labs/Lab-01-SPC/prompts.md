# Copilot in Excel: data quality and SPC

Prompts are also in Starter.xlsx > Prompts. Use them in the Copilot side pane in Excel.

## SPC1 Audit the source

Using RawTests, audit test_id uniqueness, missing collected_L, duration_s and quality_flag. Do not modify RawTests. Create a QualityAudit table with record ID, issue, inclusion decision and reason. Use one unique record per test, require VALID and 120 seconds, and never discard an excursion solely because it is extreme. Report raw, unique and valid counts.

## SPC2 Calculate the baseline

Use ValidTests in time order. In Analysis create delivery_L_h = collected_L*3600/120. Use only the 60 baseline records to calculate mean and successive moving ranges; do not bridge across phases. Estimate sigma = MRbar/1.128 and individuals limits mean +/-3*sigma. Put constants and specifications in Parameters and show formulas, units and referenced rows.

## SPC3 Plot and interpret

Create an Excel line chart of delivery_L_h by timestamp for baseline, monitoring and pilot, with the fixed baseline mean/UCL/LCL. Flag points outside the limits without refitting them. Report phase counts and affected IDs. Explain the monitoring shift as a signal requiring investigation, not a proven restriction diagnosis. Keep invalid and missing tests visible in QualityAudit.

## SPC4 Check capability

Using fictional test specifications 58.9–65.1 L/h, calculate baseline Cp and Cpk from the stated within-process estimator. State assumptions: stable baseline, adequate measurement, suitable distribution and independence. Do not use a good Cp to claim the later monitoring period is stable. Review potential shift/measurement effects and compare with Worked-Reference.xlsx.