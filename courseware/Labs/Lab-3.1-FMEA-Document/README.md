# Lab 3.1 — FMEA Document and RPN Table

**Outcome:** LO1 · LO2  ·  **Time box:** 30 minutes  ·  **Prompt framework:** RISE

**Goal:** Build a complete FMEA for the CW-401 dosing skid and calculate RPN with Copilot in Excel.

**You will produce:** A ranked FMEA table with RPN, a severity escalation list, an RPN chart and an action list.

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

- FM-01 RPN by hand: 7 × 5 × 4 = 140
- FM-02 RPN = 192, the highest of the four
- FM-04 has the LOWEST RPN (54) but Severity 9 — it still escalates
- No fifth failure mode appeared; every supplied rating is unchanged

## Stuck? Ask a class agent

| Agent | Ask it about | Open |
|---|---|---|
| **IES Engineering Methods Tutor** | FMEA, DMAIC and SPC concepts | [Open in Copilot](https://m365.cloud.microsoft/chat/?titleId=T_a665bf4c-cf77-eca0-07f2-b9c156672efe) |
| **IES AI Security Advisor** | PDPA, data leakage, ownership, lifecycle, sensitivity labels, accountability | [Open in Copilot](https://m365.cloud.microsoft/chat/?titleId=T_be5547ee-5c46-4e82-66af-e45cbdf7facd) |

Both agents explain and teach. Neither approves an engineering decision, and neither will do the lab for you.

## Complete prompt to use

```text
ROLE
Act as an FMEA facilitator supporting a competent engineer. You draft; you never approve.

INPUT
Use only the named Excel table FMEAInput on the FMEA_Input sheet, and the classroom
scale on the Rating_Guide sheet. Do not use outside knowledge and do not add rows.

STEPS
1. Preserve all four supplied rows and every supplied S, O and D rating exactly.
2. Calculate RPN = Severity x Occurrence x Detection for each row and show the arithmetic.
3. Rank the four rows from highest to lowest RPN.
4. Separately flag every row with Severity 9 or higher under ESCALATE FOR SEPARATE REVIEW.
5. Insert a clustered column chart of RPN by failure mode ID.
6. Give one evidence request and one practical follow-up action per row.

EXPECTATIONS
Return the completed table, ranked list, escalation list and actions. Do not invent incidents,
causes, owners or dates. Do not change a rating. A high Detection number means poor
detectability. End with unresolved questions and DRAFT FOR REVIEW.

INDEPENDENT CHECK
Verify FM-01: 7 x 5 x 4 = 140. Confirm FM-04 is escalated on Severity 9 even though
its RPN is the lowest.
```

---

All records in this lab are fictional training data. They describe no actual facility, person or
organisation. Values are teaching assumptions, not approved design criteria. Do not use any output
to operate, maintain or approve real equipment.
