# LO5 guided activity - Microsoft Researcher and Analyst

IES | GenAI for Engineers | Synthetic classroom case | 20 minutes inside Module 4

This is a guided activity, not a fourth lab. Researcher and Analyst do different jobs and require different checks.

## Part A - Researcher: cited technical comparison

Open Microsoft 365 Copilot, select **Agents**, then **Researcher**. Attach or reference `TR-401-Training-Extract.pdf`. If web research is permitted, keep it enabled only for approved public sources.

### RISE prompt

**Role:** Act as an engineering evidence researcher preparing a short comparison for a pump delivery-test review.

**Input:** Use the supplied fictional `TR-401-Training-Extract.pdf` and approved public primary sources. Treat TR-401 as synthetic training material, not a published standard.

**Steps:** (1) State what TR-401 says about the delivery target, comparison range and evidence gap. (2) Find two primary technical sources that explain why calibration status and test conditions matter when comparing flow measurements. (3) Separate source facts, interpretation and recommendations. (4) List unresolved questions.

**Expectations:** Produce a one-page comparison table with Claim, Source, Evidence and Limitation. Cite every external claim with a working link. Do not invent a standard clause, operating limit, root cause or approval.

### Researcher acceptance check

1. Open at least one cited source.
2. Confirm that the source supports the adjacent claim.
3. Confirm that TR-401 is labelled fictional and that missing calibration evidence remains unresolved.
4. Reject any recommendation written as an approved engineering decision.

## Part B - Analyst: calculate and interpret the DMAIC data

Open **Analyst** under Agents. Attach `../Labs/Lab-02-DMAIC/Starter.xlsx` or its CSV in `mock-data/weekly-data.csv`.

### RISE prompt

**Role:** Act as an engineering data analyst supporting a DMAIC review.

**Input:** Use only the six rows in `WeeklyData`. Baseline is W1-W4; Pilot is W5-W6. Opportunities and deviations are counts.

**Steps:** (1) Check row count, phases, units and missing values. (2) Sum opportunities and deviations by phase. (3) Calculate deviation rate = deviations / opportunities. (4) Calculate the absolute percentage-point change and relative reduction. (5) Create a simple phase comparison table and chart. (6) State one limitation and one next evidence check.

**Expectations:** Show formulas and totals. Separate observed results from hypotheses. Do not claim that the pilot caused the change or that improvement is sustained.

### Analyst acceptance check

- Baseline: `36 / 400 = 9.0%`
- Pilot: `7 / 200 = 3.5%`
- Change: `3.5% - 9.0% = -5.5 percentage points`
- Relative reduction: `(9.0% - 3.5%) / 9.0% = 61.1%`
- Limitation: only two pilot weeks; the data do not prove cause or sustained performance.

## Evidence to retain

- Researcher prompt, response, one opened citation and one correction or confirmed limitation.
- Analyst prompt, attached file name, response and the four independent calculations above.
- Actual tool availability. If an agent is unavailable, mark it **not executed** and use the supplied expected checks for discussion.

## Official Microsoft guidance

- [Get started with Researcher](https://learn.microsoft.com/en-us/microsoft-365/copilot/researcher-agent)
- [Get started with Analyst](https://support.microsoft.com/en-US/Microsoft-365-Copilot/get-started-with-analyst-in-microsoft-365-copilot)
- [Agents built by Microsoft](https://support.microsoft.com/en-us/Microsoft-365-Copilot/agents-built-by-microsoft)
