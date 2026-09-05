# Lab 3.3 prompt engineering practice

Use these prompts within the existing lab allocation. Select one improvement to the original prompt, then compare the outputs against the same evidence checks. Longer examples are reference material. Persona dialogue is a simulated review in one model, not independent expert approval.

## Activity prompt

ROLE: engineering evidence assistant preparing a draft for competent review. INPUT: the named files in this lab's mock-data folder, or petroleum-data when using the petroleum variant; choose one scenario and state it. TASK: Build a specification, checklist, review-only procedure outline and troubleshooting guide from the same current sources. CONSTRAINTS: A design reviewer checks requirements; an operations reviewer checks usability; a quality reviewer reverse-traces claims. Preserve unknowns across all four documents. OUTPUT: Four consistent documents plus a cross-document discrepancy log. VERIFICATION: cite source IDs and revisions; check calculations and retain missing fields. If critical evidence is absent, ask up to three focused questions and mark the affected output unresolved. No operational approval.

## Multi-persona review prompt

Simulate three review lenses: reliability engineer, operations lead and data-quality reviewer. First give each an initial position without a shared conclusion. Then run two rounds: one specific challenge and an evidence-backed response per lens. Cite supplied record IDs; state unknowns. Do not invent facts to win or require consensus. A moderator returns: supported conclusions, unresolved disagreements, evidence needed and draft recommendation. These are simulated perspectives from one model, not independent experts or approval. Apply this review to the activity draft and its source files.

## Constraint repair prompt

Audit the draft for violations of these constraints: A design reviewer checks requirements; an operations reviewer checks usability; a quality reviewer reverse-traces claims. Preserve unknowns across all four documents. Return violation, exact source evidence, correction and unresolved gap. Revise only supported claims.

## Procedure

1. Choose the original or petroleum scenario and open its local files. Use the tool setup in the main lab handout.
2. Save the original prompt and result as version A.
3. Run the activity prompt above as version B in a fresh session with the same inputs.
4. Add the persona review when the task has meaningful trade-offs; retain separate positions, challenges and disagreements.
5. Independently check sources and calculations. Score fidelity, completeness, uncertainty and format from 0–2 each. Any invented approval fails the release gate.
6. Save prompt versions, outputs, corrections and elapsed draft/review time in prompt-evaluation.csv. Do not claim a live test if only a blueprint was prepared.

## Expected evidence

Four consistent documents plus a cross-document discrepancy log.

## Reflection

Which specific instruction changed the output? Did persona review add useful evidence or just more words? What cannot be settled from these sources?
