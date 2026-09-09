# Lab 3.3 — SPC Control Chart and Capability

**Outcome:** LO1 · LO2  ·  **Time box:** 30 minutes  ·  **Prompt framework:** RISE + E-MAP

**Goal:** Build an Xbar-R control chart from a frozen baseline and read the monitoring signal.

**You will produce:** Xbar and R per subgroup, frozen baseline limits, a plotted chart, and Cp/Cpk with a caution.

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

- Subgroup 1: Xbar = 61.950, R = 0.900
- Limits from subgroups 1–12 only, then frozen
- Subgroup 13 Xbar = 61.275, below the LCL of 61.547
- Cp ≈ 3.13 vs Cpk ≈ 1.01 means off centre, not incapable

## Stuck? Ask a class agent

| Agent | Ask it about | Open |
|---|---|---|
| **IES Engineering Methods Tutor** | FMEA, DMAIC and SPC concepts | [Open in Copilot](https://m365.cloud.microsoft/chat/?titleId=T_a665bf4c-cf77-eca0-07f2-b9c156672efe) |
| **IES AI Security Advisor** | PDPA, data leakage, ownership, lifecycle, sensitivity labels, accountability | [Open in Copilot](https://m365.cloud.microsoft/chat/?titleId=T_be5547ee-5c46-4e82-66af-e45cbdf7facd) |

Both agents explain and teach. Neither approves an engineering decision, and neither will do the lab for you.

## Complete prompt to use

```text
ROLE
Act as an SPC analyst preparing a control-chart review for a competent engineer.

INPUT
Use only the named Excel table SPCData. Subgroup size n = 4. Subgroups 1-12 are
Baseline and 13-16 are Monitoring. Use A2 = 0.729, D4 = 2.282 and d2 = 2.059.
The classroom specification band is LSL 57.0 and USL 63.0 L/h.

STEPS
1. Calculate Xbar and R for every subgroup.
2. Use Baseline subgroups only to calculate Xbarbar and Rbar.
3. Calculate UCL = Xbarbar + A2 x Rbar and LCL = Xbarbar - A2 x Rbar.
4. Freeze those limits and plot all 16 subgroups on one Xbar chart.
5. Flag every Monitoring subgroup outside the limits.
6. Estimate sigma = Rbar / d2, then calculate Cp and Cpk.

EXPECTATIONS
Never recalculate limits using Monitoring data. Show formulas and units to three decimals.
Report Cp and Cpk together. A point outside a limit is a signal to investigate, not a
diagnosis or proof that equipment is unsafe. End with DRAFT FOR REVIEW.

INDEPENDENT CHECK
Subgroup 13 Xbar = (61.5 + 61.2 + 61.4 + 61.0) / 4 = 61.275 L/h.
Confirm it is below the frozen LCL.
```

---

All records in this lab are fictional training data. They describe no actual facility, person or
organisation. Values are teaching assumptions, not approved design criteria. Do not use any output
to operate, maintain or approve real equipment.
