# Lab 2.3 prompts

## Main prompt

Engineering: planning-stage replacement of the fictional dosing pump. Metrics: cover every hazard in hazard-checklist.csv and expose all missing evidence. Assumptions: no chemical identity, SDS or approved isolation details are available. Parameters: desk exercise only; no work is authorised. Draft a risk assessment and method-statement planning outline. Include hold points and competent review. Do not prescribe chemical-specific PPE, exposure limits or live-work instructions.

## Verification prompt

Audit your previous response against the named source files. List each claim, supporting source and location, uncertainty and correction. Check numbers and units independently. Keep missing facts explicit. Return the revised draft plus a change log; do not approve the engineering deliverable.

## Recovery prompt

The required source or capability is unavailable. State exactly what is missing, retain a draft status, and propose a manual check using the supplied fictional files. Do not fabricate a completed result.

## Prompt engineering extension

ROLE: engineering evidence assistant preparing a draft for competent review. INPUT: the named files in this lab's mock-data folder, or petroleum-data when using the petroleum variant; choose one scenario and state it. TASK: Use E-MAP to prepare a desk-review risk register from the supplied work activity and hazard evidence. CONSTRAINTS: Include hazard, evidence, missing information, proposed control and reviewer. Do not invent fluid identity, isolation instructions or operational permission. OUTPUT: Traceable hazards and explicit hold points, with controls marked proposed. VERIFICATION: cite source IDs and revisions; check calculations and retain missing fields. If critical evidence is absent, ask up to three focused questions and mark the affected output unresolved. No operational approval.

### Multi-persona review

Simulate three review lenses: reliability engineer, operations lead and data-quality reviewer. First give each an initial position without a shared conclusion. Then run two rounds: one specific challenge and an evidence-backed response per lens. Cite supplied record IDs; state unknowns. Do not invent facts to win or require consensus. A moderator returns: supported conclusions, unresolved disagreements, evidence needed and draft recommendation. These are simulated perspectives from one model, not independent experts or approval.

See Prompt-Engineering.md and Prompt-Engineering.pdf for the practice procedure and evaluation log.
