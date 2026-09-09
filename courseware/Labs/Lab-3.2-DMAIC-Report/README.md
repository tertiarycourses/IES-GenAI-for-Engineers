# Lab 3.2 — DMAIC Improvement Report

**Outcome:** LO1 · LO2  ·  **Time box:** 30 minutes  ·  **Prompt framework:** RISE + E-MAP

**Goal:** Turn six weeks of deviation data into a five-phase DMAIC summary with a Pareto chart.

**You will produce:** Phase rates with formulas shown, a Pareto chart, and a five-row DMAIC summary.

## Files in this folder

| File | What it is |
|---|---|
| `Lab-Instructions.pdf` | Complete step-by-step instructions and copyable prompt - start here |
| `Starter.xlsx` | Your working file — open this one |
| `Worked-Reference.xlsx` | Model answer — open only after your own attempt |
| `mock-data.csv` | The same data as plain CSV |

## How to run this lab

1. Open **Lab-Instructions.pdf** and follow it from Step 1.
2. Open **Starter.xlsx**. Do not open the worked reference yet.
3. Select the named table, open Copilot in Excel, and paste the prompt under **Complete prompt to use** below.
4. Check the numbers by hand before you accept them.
5. Only then compare against **Worked-Reference.xlsx**.

## Check your own work

- Baseline rate: 36 ÷ 400 = 9.00%
- Pilot rate: 7 ÷ 200 = 3.50%
- Absolute change is 5.50 percentage points, not "a 61% improvement"
- Pareto counts sum to 36 and reconcile with the baseline deviations

## Stuck? Ask a class agent

| Agent | Ask it about | Open |
|---|---|---|
| **IES Engineering Methods Tutor** | FMEA, DMAIC and SPC concepts | [Open in Copilot](https://m365.cloud.microsoft/chat/?titleId=T_a665bf4c-cf77-eca0-07f2-b9c156672efe) |
| **IES AI Security Advisor** | PDPA, data leakage, ownership, lifecycle, sensitivity labels, accountability | [Open in Copilot](https://m365.cloud.microsoft/chat/?titleId=T_be5547ee-5c46-4e82-66af-e45cbdf7facd) |

Both agents explain and teach. Neither approves an engineering decision, and neither will do the lab for you.

## Complete prompt to use

```text
ROLE
Act as a Six Sigma project assistant preparing a draft for a competent reviewer.

INPUT
Use only the named Excel table WeeklyData and the category counts on the Pareto sheet.
Three weeks are Baseline and three are Pilot. Do not use outside knowledge.

STEPS
1. Calculate total opportunities, total deviations and deviation rate for each phase.
2. State the absolute change in percentage points.
3. Build the Pareto of baseline categories with a cumulative percentage column and chart.
4. Draft a five-row DMAIC summary: Define, Measure, Analyse, Improve, Control.
5. In Analyse, separate what the data shows from what is only a hypothesis.

ENGINEERING CONTEXT - E-MAP
Engineering context: delivered-dose checks on a chemical dosing skid.
Metrics: deviations divided by opportunities, in percent, to two decimals.
Assumptions: the deviation definition and counting method are unchanged across six weeks.
Parameters: six weeks only, three weeks per phase.

EXPECTATIONS
Show every formula, unit and row count. State that a three-week pilot does not prove cause
and concurrent changes cannot be separately attributed. Do not invent root cause, savings
or completion percentage. Return one next evidence check. End with DRAFT FOR REVIEW.

INDEPENDENT CHECK
Baseline: 36 / 400 = 9.00%. Pilot: 7 / 200 = 3.50%.
Absolute change: 5.50 percentage points.
```

---

All records in this lab are fictional training data. They describe no actual facility, person or
organisation. Values are teaching assumptions, not approved design criteria. Do not use any output
to operate, maintain or approve real equipment.
