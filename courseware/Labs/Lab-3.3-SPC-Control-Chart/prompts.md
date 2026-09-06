# Lab 3.3 — SPC Control Chart and Capability

Structured with RISE and E-MAP. The rendered version with framework labels is `Lab-3.3-Prompt.pdf`.

```
ROLE
Act as an SPC analyst preparing a control chart review for a competent engineer.

INPUT
Use only the named Excel table SPCData. Subgroup size is n = 4. Subgroups 1 to 12 are
Baseline and subgroups 13 to 16 are Monitoring. Use the constants A2 = 0.729, D4 = 2.282
and d2 = 2.059 for n = 4. The classroom specification band is LSL 57.0 and USL 63.0 L/h.

STEPS
1. Calculate Xbar and R for every subgroup.
2. Using the BASELINE subgroups only, calculate Xbarbar and Rbar.
3. Calculate UCL = Xbarbar + A2 x Rbar and LCL = Xbarbar - A2 x Rbar. Show both formulas.
4. Hold those baseline limits fixed and plot all 16 subgroups on one Xbar chart with the
   centre line, UCL and LCL drawn.
5. Flag every monitoring subgroup that falls outside the limits.
6. Estimate sigma as Rbar divided by d2, then calculate Cp and Cpk. Show both formulas.

ENGINEERING CONTEXT (E-MAP)
Engineering context: delivery test on a chemical dosing skid, measured in L/h.
Metrics: Xbar, R, control limits, Cp and Cpk, all to three decimal places.
Assumptions: the measurement system is capable and the subgroups are in time order.
State both assumptions in the output.
Parameters: n = 4, 12 baseline subgroups, limits frozen before monitoring begins.

EXPECTATIONS
Never recalculate the limits using the monitoring data. Report Cp and Cpk together and
explain that Cp much larger than Cpk means the process is off centre rather than incapable.
State that capability is only meaningful while the process is stable, and that these
monitoring points show it is not. A point outside a control limit is a signal to investigate,
never a diagnosis and never proof that equipment is unsafe.
End with DRAFT FOR REVIEW.

INDEPENDENT CHECK
Verify subgroup 13 by hand: Xbar = (61.5 + 61.2 + 61.4 + 61.0) / 4 = 61.275 L/h, which is
below the lower control limit. Confirm all four monitoring subgroups fall below the LCL and
that they trend steadily downwards rather than jumping once.
```
