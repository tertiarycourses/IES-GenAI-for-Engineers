# Prompt bank: optional after-class extension

In class use only SPC3. Other prompts are reference material and carry no class-time requirement.


Prompts are also in Starter.xlsx > Prompts. Use them in the Copilot side pane in Excel.

## SPC1 Audit the source

Using RawTests, audit test_id uniqueness, missing collected_L, duration_s and quality_flag. Do not modify RawTests. Create a QualityAudit table with record ID, issue, inclusion decision and reason. Use one unique record per test, require VALID and 120 seconds, and never discard an excursion solely because it is extreme. Report raw, unique and valid counts.

## SPC2 Calculate the baseline

Use ValidTests in time order. In Analysis create delivery_L_h = collected_L*3600/120. Use only the 60 baseline records to calculate mean and successive moving ranges; do not bridge across phases. Estimate sigma = MRbar/1.128 and individuals limits mean +/-3*sigma. Put constants and specifications in Parameters and show formulas, units and referenced rows.

## SPC3 Plot and interpret

Review the existing Analysis and SPC_Summary chart. Keep the prepared formulas and fixed baseline limits unchanged. Identify valid monitoring points outside the limits and check one example against the source row. Return only three sentences: observed signal, supporting evidence, and an unresolved limitation. Do not rebuild the chart or calculate capability.

## SPC4 Check capability

Using fictional test specifications 58.9–65.1 L/h, calculate baseline Cp and Cpk from the stated within-process estimator. State assumptions: stable baseline, adequate measurement, suitable distribution and independence. Do not use a good Cp to claim the later monitoring period is stable. Review potential shift/measurement effects and compare with Worked-Reference.xlsx.

## Open Microsoft 365 Copilot

- [Microsoft 365 Copilot](https://m365.cloud.microsoft/chat) — sign in with your work or school account.
- [Get started with Copilot in Excel](https://support.microsoft.com/en-us/office/get-started-with-copilot-in-excel) — Excel analysis help.
- [How Copilot Chat works in Microsoft 365 apps](https://support.microsoft.com/en-us/microsoft-365-copilot/how-copilot-chat-works-in-microsoft-365-apps) — Word, Excel and PowerPoint guidance.

If the Copilot button is missing, use the approved manual-formula fallback and tell the trainer. Availability depends on your organisation’s licence and settings.
