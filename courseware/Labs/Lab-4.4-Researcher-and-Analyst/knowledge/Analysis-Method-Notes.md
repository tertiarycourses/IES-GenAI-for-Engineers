# Analysis Method Notes

Fictional training reference. Use these definitions when calculating.

## Control limits from a moving range

- Estimate sigma as the average successive moving range of the baseline divided by 1.128.
- UCL = mean + 3 sigma. LCL = mean - 3 sigma. Show both formulas.
- Use only the baseline rows to set limits. Monitoring rows are then compared against them.

## Capability

- Cp compares the specification width to the process spread.
- Cpk also accounts for centring, so Cpk is never greater than Cp.
- Capability figures from a short run are provisional. Say so.

## What a signal means

A point outside a control limit is a signal to investigate. It is not a diagnosis, not a root cause, and not evidence that equipment is unsafe.

## Limits of inference

- Correlation is not cause.
- A short pilot cannot demonstrate a sustained improvement.
- Two changes made at once cannot be separately attributed.
- A supplied example prediction is a teaching artefact, never the output of a trained model.
