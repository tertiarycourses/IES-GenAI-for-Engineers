# Lab 2.2 prompts

## Main prompt

Convert INS-04 revision 1 into a structured inspection report. Distinguish direct observation, reported observation, hypothesis and missing evidence. Do not label a non-conformance without a requirement. Include an executive summary, evidence requests and a responsible review role. Do not invent photographs, readings, permits or completion claims.

## Verification prompt

Audit your previous response against the named source files. List each claim, supporting source and location, uncertainty and correction. Check numbers and units independently. Keep missing facts explicit. Return the revised draft plus a change log; do not approve the engineering deliverable.

## Recovery prompt

The required source or capability is unavailable. State exactly what is missing, retain a draft status, and propose a manual check using the supplied fictional files. Do not fabricate a completed result.

## Prompt engineering extension

ROLE: engineering evidence assistant preparing a draft for competent review. INPUT: the named files in this lab's mock-data folder, or petroleum-data when using the petroleum variant; choose one scenario and state it. TASK: Turn the inspection notes into a concise report for an engineering reviewer. Label observed, reported and hypothesised statements. CONSTRAINTS: Do not call a finding a non-conformance without citing its requirement. Retain missing calibration evidence and uncertain liquid identity. OUTPUT: Observation/source/gap/review-action table with a bounded summary. VERIFICATION: cite source IDs and revisions; check calculations and retain missing fields. If critical evidence is absent, ask up to three focused questions and mark the affected output unresolved. No operational approval.

### Multi-persona review

Simulate three review lenses: reliability engineer, operations lead and data-quality reviewer. First give each an initial position without a shared conclusion. Then run two rounds: one specific challenge and an evidence-backed response per lens. Cite supplied record IDs; state unknowns. Do not invent facts to win or require consensus. A moderator returns: supported conclusions, unresolved disagreements, evidence needed and draft recommendation. These are simulated perspectives from one model, not independent experts or approval.

See Prompt-Engineering.md and Prompt-Engineering.pdf for the practice procedure and evaluation log.
