# Lab 4.2 Build a Report Writer agent

IES | 20 minutes | LO4

All records are fictional training data. They describe no actual facility, person or organisation. Values are teaching assumptions, not approved design criteria. Do not use outputs to operate, maintain or approve real equipment.

## Files

Open Lab-Handout.pdf, prompts.md and the files in mock-data. Each lab is self-contained; earlier outputs may be reused but are not required. Save your work under outputs.

## Procedure

1. Create a second agent named IES Report Writer using New agent and Configure. Paste the instructions from prompts.md.

2. Ground it on the weekly and DMAIC templates in approved training storage. Add starter prompts for weekly progress and DMAIC reports. Specify that it must ask which report type is required.

3. Provide weekly-inputs.txt and request a weekly report. Compare headings with report-template.md. Confirm A02 stays open and A03 remains blocked by missing fluid identity.

4. Test a request for percentage completion and approved budget. Neither is supplied; the agent should state unavailable instead of estimating. Test the DMAIC template separately with a short source-backed summary.

5. Save and test with an approved peer where sharing is enabled. Save the agent configuration and one corrected output; record the required human release decision.

## Acceptance checks

- Mandatory headings match the selected template.
- A02 is open and no unsupported percentage is generated.

## If access is unavailable

Use approved paired access or the local source files to prepare a draft and configuration blueprint. Record live agent or permission tests as not executed. Do not use personal accounts to bypass organisational controls.
