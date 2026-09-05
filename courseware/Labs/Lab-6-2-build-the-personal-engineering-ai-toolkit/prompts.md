# Lab 6.2 prompts

## Main prompt

Turn my tested prompts and agent notes into a personal engineering AI toolkit. For each workflow include approved inputs, source versions, prompt, output, acceptance test, human reviewer and failure response. Keep untested capabilities clearly marked. Propose a one-week trial with review-inclusive timing and error tracking.

## Verification prompt

Audit your previous response against the named source files. List each claim, supporting source and location, uncertainty and correction. Check numbers and units independently. Keep missing facts explicit. Return the revised draft plus a change log; do not approve the engineering deliverable.

## Recovery prompt

The required source or capability is unavailable. State exactly what is missing, retain a draft status, and propose a manual check using the supplied fictional files. Do not fabricate a completed result.

## Standalone framework example 2.1

Role: engineering specification writer. Input: design-requirements.csv and DES-01 rev2 only. Steps: extract confirmed requirements; separate gaps; draft scope, duty, materials, acceptance and review sections; create a requirement-to-test checklist. Expectations: preserve IDs and units, cite clauses, leave missing fields TBD, and mark DRAFT FOR REVIEW. DES-01 is a fictional design note, not a published standard.

## Standalone framework example 2.3

Engineering: planning-stage replacement of the fictional dosing pump. Metrics: cover every hazard in hazard-checklist.csv and expose all missing evidence. Assumptions: no chemical identity, SDS or approved isolation details are available. Parameters: desk exercise only; no work is authorised. Draft a risk assessment and method-statement planning outline. Include hold points and competent review. Do not prescribe chemical-specific PPE, exposure limits or live-work instructions.
