# Ready-to-use trainer demonstrations

These are original synthetic teaching examples. No live agent deployment is required.
Use the original LP module timings; these demonstrations replace discussion examples, not add lab time.

## Module 4 — FMEA assistant (within the 25-minute demonstration)
Open Lab-01-SPC/Worked-Reference.xlsx. Show FMEA_Input, ScoringNote and Evidence.
Prepared instructions:
Act as an engineering drafting assistant. Use only the supplied case records and rating guidance.
For one selected mode, return failure mode, effect, possible cause, current control and missing evidence.
Retain the supplied scores. Separate observed facts from hypotheses. Do not invent an approval.
Test question: Review FM01, the low-delivery row. What remains unproven?
Illustrative expected response: Low delivery was observed. A restriction is a possible explanation.
Evidence that the removed strainer was blocked is still needed. The current records do not isolate one cause.
Trainer check: open FM01 and the evidence records, then inspect the score definitions.
If Copilot is available, run this as a prompt or through a prepared assistant. Identify the surface used.
If not, show the illustrative response and label it a worked example.

## Module 4 — report writer (within the workflow demonstration)
Source note: Later tests recorded lower delivery. Strainer replacement and verification occurred together.
Pilot results improved. Review of the removed strainer remains open.
Prompt: Turn these facts into Status / Evidence / Next action. Do not label an open action completed.
Illustrative response:
Status: Pilot delivery results improved.
Evidence: Results improved after strainer replacement and verification.
Next action: Complete the removed-strainer review before attributing the improvement to one cause.
Trainer check: ask which sentence would become wrong if “open” were changed to “completed”.

## Module 5 — grounded document answer (within the 20-minute demonstration)
Use TR-401-Training-Extract.pdf in this folder, or place it in an approved demonstration library before class.
Prompt: Using only TR-401 revision 1, which measurement fields must a test record contain?
Give the supporting clause. If the extract does not answer a question, say so.
Illustrative response: Clause 1 lists test ID, timestamp, collected volume in litres and duration in seconds.
Check: open clause 1 and compare all four fields. Clause 2 adds setting, operator role and observed issues.
Follow-up: What delivery limit does this extract approve?
Expected response: The extract does not specify or approve a delivery limit.
A real SharePoint demo requires an approved library and appropriate access. If unavailable, use this local
document walkthrough and label it accordingly. Do not claim permission testing has occurred without testing it.
