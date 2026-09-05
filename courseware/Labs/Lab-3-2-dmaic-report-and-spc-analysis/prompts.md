# Lab 3.2 prompts

## Main prompt

Use baseline samples 1-30 only to estimate an individuals chart with MRbar/1.128. Keep monitoring samples 31-35 separate. Show formulas, units, sample counts, missing-value checks and baseline limits. Flag signals without inventing a cause. Summarise defects using Pareto; label fishbone and 5-Whys statements as hypotheses. Draft all five DMAIC sections, a trial and control plan. Capability estimates are provisional, not certification.

## Verification prompt

Audit your previous response against the named source files. List each claim, supporting source and location, uncertainty and correction. Check numbers and units independently. Keep missing facts explicit. Return the revised draft plus a change log; do not approve the engineering deliverable.

## Recovery prompt

The required source or capability is unavailable. State exactly what is missing, retain a draft status, and propose a manual check using the supplied fictional files. Do not fabricate a completed result.

## Prompt engineering extension

ROLE: engineering evidence assistant preparing a draft for competent review. INPUT: the named files in this lab's mock-data folder, or petroleum-data when using the petroleum variant; choose one scenario and state it. TASK: Use the selected process dataset: rows 1–30 baseline and 31–35 monitoring. Calculate the individuals chart using MR/1.128 and draft a DMAIC brief. CONSTRAINTS: Keep the original time order and units. Do not recompute limits from monitoring rows. Treat capability as conditional and a signal as evidence for investigation. OUTPUT: Reproducible statistics, signal identification and no invented root cause. VERIFICATION: cite source IDs and revisions; check calculations and retain missing fields. If critical evidence is absent, ask up to three focused questions and mark the affected output unresolved. No operational approval.

### Multi-persona review

Simulate three review lenses: reliability engineer, operations lead and data-quality reviewer. First give each an initial position without a shared conclusion. Then run two rounds: one specific challenge and an evidence-backed response per lens. Cite supplied record IDs; state unknowns. Do not invent facts to win or require consensus. A moderator returns: supported conclusions, unresolved disagreements, evidence needed and draft recommendation. These are simulated perspectives from one model, not independent experts or approval.

See Prompt-Engineering.md and Prompt-Engineering.pdf for the practice procedure and evaluation log.
