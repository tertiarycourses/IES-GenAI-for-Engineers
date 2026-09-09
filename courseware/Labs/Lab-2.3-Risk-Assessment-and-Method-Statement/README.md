# Lab 2.3 - Risk Assessment and Method Statement

**Purpose:** Use E-MAP to draft a bounded risk and method statement while preserving the competent-person approval gate.

**Output:** A preliminary hazard table, method sequence, missing-information list and blank approval section.

## What you will do

1. Review the supplied classroom records.
2. Open Word and establish the engineering context with E-MAP.
3. Ask Copilot for hazards, controls and method steps using only supplied facts.
4. Mark missing task conditions and approved criteria.
5. Check that proposed controls are not described as existing.
6. Reject any risk-acceptance or safety approval claim.
7. Save the result as a preliminary draft.

## Files used

| File | Use |
|---|---|
| `Lab-Instructions.pdf` | Detailed instructions. |
| `mock-data.csv` | Limited classroom context for the drafting exercise. |

## Detailed steps

1. Open `mock-data.csv`. Note that it provides a system, delivery result and target but does not provide the task, work area, substances, exposure route, isolation method, risk matrix or approving person.
2. Open Word and create **CW-401 - Preliminary Risk Assessment and Method Statement**.
3. Add an E-MAP context block:

| E-MAP field | Entry |
|---|---|
| Engineering context | Chemical dosing skid classroom scenario |
| Metrics | 59.4 L/h test result; 62.0 L/h reference target |
| Assumptions | None may be treated as approved facts |
| Parameters missing | Task scope, hazards, limits, isolations, PPE, matrix and competent person |

4. Open Copilot in Word and paste:

```
Act as a risk-document drafting assistant. Use only the supplied E-MAP context.
Create: task boundary, preliminary hazard register, existing controls, proposed controls,
method sequence, hold points, missing evidence, and blank competent-person approval.
Do not invent chemicals, exposure routes, isolation points, PPE, risk ratings or approvals.
Label every unsupported item INFORMATION REQUIRED.
```

5. Review the hazard register. Remove any specific hazard or control not supported by the input.
6. Confirm that **proposed controls** are not presented as existing controls.
7. Confirm that no numerical risk rating is assigned because an approved matrix is not supplied.
8. Add hold points requiring task definition, approved risk matrix and competent-person review before work.
9. Save the document as **PRELIMINARY - NOT FOR WORK EXECUTION**.

## Independent checks

- The result and target differ by 2.6 L/h, but that does not establish a hazard or safe operating limit.
- No risk score can be approved without the organisation's matrix and evidence.
- A generated method sequence is not authority to perform work.

## Pass conditions

- Missing task and safety information is explicit.
- Unsupported hazards, PPE, isolations and ratings are not invented.
- Existing and proposed controls are separated.
- Hold points and a blank approval section are present.
- The document is clearly marked not for execution.

All supplied records are fictional classroom data.
