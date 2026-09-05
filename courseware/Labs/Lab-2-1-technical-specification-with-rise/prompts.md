# Lab 2.1 prompts

## Main prompt

Role: engineering specification writer. Input: design-requirements.csv and DES-01 rev2 only. Steps: extract confirmed requirements; separate gaps; draft scope, duty, materials, acceptance and review sections; create a requirement-to-test checklist. Expectations: preserve IDs and units, cite clauses, leave missing fields TBD, and mark DRAFT FOR REVIEW. DES-01 is a fictional design note, not a published standard.

## Verification prompt

Audit your previous response against the named source files. List each claim, supporting source and location, uncertainty and correction. Check numbers and units independently. Keep missing facts explicit. Return the revised draft plus a change log; do not approve the engineering deliverable.

## Recovery prompt

The required source or capability is unavailable. State exactly what is missing, retain a draft status, and propose a manual check using the supplied fictional files. Do not fabricate a completed result.

## Prompt engineering extension

ROLE: engineering evidence assistant preparing a draft for competent review. INPUT: the named files in this lab's mock-data folder, or petroleum-data when using the petroleum variant; choose one scenario and state it. TASK: Using only the current supplied design revision, create a requirement-to-test specification. Preserve each quantity and unit. CONSTRAINTS: Columns: ID, requirement, unit, source clause, acceptance evidence, gap. Materials and interfaces not supplied remain TBD. No invented standards or approval. OUTPUT: Every requirement traces to the current clause and the matching test. VERIFICATION: cite source IDs and revisions; check calculations and retain missing fields. If critical evidence is absent, ask up to three focused questions and mark the affected output unresolved. No operational approval.

### Multi-persona review

Simulate three review lenses: reliability engineer, operations lead and data-quality reviewer. First give each an initial position without a shared conclusion. Then run two rounds: one specific challenge and an evidence-backed response per lens. Cite supplied record IDs; state unknowns. Do not invent facts to win or require consensus. A moderator returns: supported conclusions, unresolved disagreements, evidence needed and draft recommendation. These are simulated perspectives from one model, not independent experts or approval.

See Prompt-Engineering.md and Prompt-Engineering.pdf for the practice procedure and evaluation log.
