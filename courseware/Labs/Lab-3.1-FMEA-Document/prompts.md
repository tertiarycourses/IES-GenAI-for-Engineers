# Lab 3.1 — FMEA Document and RPN Table

Structured with RISE. The rendered version with framework labels is `Lab-3.1-Prompt.pdf`.

```
ROLE
Act as an FMEA facilitator supporting a competent engineer. You draft; you never approve.

INPUT
Use only the named Excel table FMEAInput on the FMEA_Input sheet, and the classroom scale on
the Rating_Guide sheet. Do not use outside knowledge and do not add rows.

STEPS
1. Preserve all four supplied rows and every supplied S, O and D rating exactly as given.
2. Calculate RPN = Severity x Occurrence x Detection for each row and show the arithmetic,
   for example 7 x 5 x 4 = 140.
3. Rank the four rows from highest to lowest RPN.
4. Separately flag every row with Severity 9 or higher under the heading
   ESCALATE FOR SEPARATE REVIEW, whatever its RPN.
5. Insert a clustered column chart of RPN by failure mode ID.
6. For each row give one evidence request and one practical follow-up action.

EXPECTATIONS
Return a table with the supplied columns plus RPN and Severity flag, then the ranked list,
then the escalation list, then the actions. Show the RPN formula once in words. Do not invent
incidents, causes, owners or dates. Do not change a rating. Do not state that the skid is safe
or fit for service. Note that a high Detection number means POOR detectability.
End with the unresolved questions and the words DRAFT FOR REVIEW.

INDEPENDENT CHECK
Verify FM-01 by hand: 7 x 5 x 4 = 140. Confirm FM-04 is escalated on Severity 9 even though
its RPN is the lowest of the four.
```
