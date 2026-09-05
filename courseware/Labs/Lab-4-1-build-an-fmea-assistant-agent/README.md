# Lab 4.1 Build an FMEA Assistant agent

IES | 25 minutes | LO4

All records are fictional training data. They describe no actual facility, person or organisation. Values are teaching assumptions, not approved design criteria. Do not use outputs to operate, maintain or approve real equipment.

## Files

Open Lab-Handout.pdf, prompts.md and the files in mock-data. Each lab is self-contained; earlier outputs may be reused but are not required. Save your work under outputs.

## Procedure

1. Open Microsoft 365 Copilot and choose New agent (some tenants expose agent creation through Agents). Select Configure or Skip to configure. The lesson proposal calls this Copilot Studio agent builder; current navigation uses Agent Builder.

2. Name the agent IES FMEA Assistant. Add a description of its drafting role. Paste the agent instructions in prompts.md and add starter prompts for reviewing an FMEA and listing missing evidence.

3. Add the training system, rating scale and template as knowledge using the available file or SharePoint source controls. If local file grounding is unavailable, upload only these synthetic files to the approved training library and select that source. Record exact source versions.

4. Use Try it to run a normal system request. Then remove rating information from the request and ask about a system absent from the source. Check that it requests missing data rather than inventing ratings.

5. Run the conflicting-source and embedded-instruction tests in agent-test-cases.csv. Record actual output and pass or fail. Refine instructions and rerun the failed case.

6. Create or save the agent and share only with the approved class group if tenant policy permits. Test with a second authorised learner; sharing an agent does not grant access to its source files. Save instructions, source list, test log and approved sharing scope.

## Acceptance checks

- Normal and missing-source tests are recorded.
- Ratings and multiplication are checked independently.
- Sharing scope and source permissions are recorded.

## If access is unavailable

Use approved paired access or the local source files to prepare a draft and configuration blueprint. Record live agent or permission tests as not executed. Do not use personal accounts to bypass organisational controls.

## Petroleum transfer pathway (v1.1)

Petroleum transfer pathway: choose this scenario instead of the original lab within the same time allocation. Additional explanations are reference reading. All petroleum records, limits, outputs and scores here are original fictional teaching examples; no operating action is authorised.

[Open the petroleum lab variant](Petroleum-Variant.md), [PDF handout](Petroleum-Variant.pdf) and [prompts](petroleum-prompts.md). Inputs are self-contained in petroleum-data.
