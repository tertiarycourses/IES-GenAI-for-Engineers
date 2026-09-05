# Lab 4.4 prompts

## Main prompt

Analyse the supplied synthetic fill dataset. Use samples 1-30 as baseline and 31-35 as monitoring. Estimate sigma with average successive baseline moving range divided by 1.128. Report n, mean, limits and provisional Cp/Cpk using 9.4 and 10.6 L. Detect monitoring signals and show calculations. Do not infer root cause from correlation. Separately summarise the defect Pareto.

## Verification prompt

Audit your previous response against the named source files. List each claim, supporting source and location, uncertainty and correction. Check numbers and units independently. Keep missing facts explicit. Return the revised draft plus a change log; do not approve the engineering deliverable.

## Recovery prompt

The required source or capability is unavailable. State exactly what is missing, retain a draft status, and propose a manual check using the supplied fictional files. Do not fabricate a completed result.

## Prompt engineering extension

ROLE: engineering evidence assistant preparing a draft for competent review. INPUT: the named files in this lab's mock-data folder, or petroleum-data when using the petroleum variant; choose one scenario and state it. TASK: For research, compare methods using primary sources and limitations. For analysis, calculate the requested metrics from the named CSV columns. CONSTRAINTS: Separate external research from local data. State formulas, units, rows and missing-value treatment. Label mock predictions as supplied examples, not a trained model. OUTPUT: Source-linked comparison and independently checked numerical results. VERIFICATION: cite source IDs and revisions; check calculations and retain missing fields. If critical evidence is absent, ask up to three focused questions and mark the affected output unresolved. No operational approval.

### Multi-persona review

Simulate three review lenses: reliability engineer, operations lead and data-quality reviewer. First give each an initial position without a shared conclusion. Then run two rounds: one specific challenge and an evidence-backed response per lens. Cite supplied record IDs; state unknowns. Do not invent facts to win or require consensus. A moderator returns: supported conclusions, unresolved disagreements, evidence needed and draft recommendation. These are simulated perspectives from one model, not independent experts or approval.

See Prompt-Engineering.md and Prompt-Engineering.pdf for the practice procedure and evaluation log.
