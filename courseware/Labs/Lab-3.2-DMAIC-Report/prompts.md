# Lab 3.2 — DMAIC Improvement Report

Structured with RISE and E-MAP. The rendered version with framework labels is `Lab-3.2-Prompt.pdf`.

```
ROLE
Act as a Six Sigma project assistant preparing a draft for a competent reviewer.

INPUT
Use only the named Excel table WeeklyData and the category counts on the Pareto sheet.
Three weeks are Baseline and three are Pilot. Do not use outside knowledge.

STEPS
1. Calculate total opportunities, total deviations and the deviation rate for each phase,
   using deviations divided by opportunities. Show each formula and its result.
2. State the absolute change in percentage points between the phases.
3. Build the Pareto of baseline deviation categories with a cumulative percentage column
   and insert the Pareto chart.
4. Draft a five-row DMAIC summary: Define, Measure, Analyse, Improve, Control.
5. In Analyse, separate what the data shows from what is only a hypothesis.

ENGINEERING CONTEXT (E-MAP)
Engineering context: a chemical dosing skid whose delivered dose is checked weekly.
Metrics: deviation rate as deviations divided by opportunities, in percent, to two decimals.
Assumptions: the deviation definition is unchanged across all six weeks and every week
was counted the same way. State this assumption in the output.
Parameters: six weeks only, three per phase. No other period is in scope.

EXPECTATIONS
Show every formula, unit and row count so a reviewer can reproduce the numbers by hand.
State plainly that a three-week pilot does not prove the cause of the change and that two
concurrent changes cannot be separately attributed. Do not invent a root cause, a cost saving
or a completion percentage. Return one next evidence check.
End with DRAFT FOR REVIEW.

INDEPENDENT CHECK
Verify the baseline rate by hand: 36 divided by 400 = 9.00 percent.
Verify the pilot rate: 7 divided by 200 = 3.50 percent. The absolute change is 5.50
percentage points, not a 61 percent improvement claim.
```
