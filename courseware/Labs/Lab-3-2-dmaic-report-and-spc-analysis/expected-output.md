# Expected output example

Illustrative teaching example, not a recorded Copilot run or an approved engineering result.

Baseline mean 10.01333 L; MRbar 0.18621 L; sigma estimate 0.16508 L; LCL 9.51810 L; UCL 10.50856 L; Cp 1.212; Cpk 1.185. Sample 33 is 10.8 L, above UCL. Top two defect categories are 20/30 = 66.7%. Small training sample only.

## Acceptance checks

- Baseline n=30, monitoring n=5; sample 33 signals above UCL.
- Cp and Cpk use the stated within-process estimate and the 9.4-10.6 L teaching limits.
- Pareto top two categories total 66.7%; causation is unproven.

## Worked DMAIC report

### Define

CTQ: fill volume in litres. Scope: the synthetic process only. Teaching specifications are 9.4-10.6 L. The question is whether the monitoring sequence has departed from the baseline behaviour.

### Measure

There are 30 baseline readings and five monitoring readings. The CSV contains no missing fill values. Baseline mean is 10.013333 L. Measurement-system suitability is not established by the data file.

### Analyse

Average successive baseline moving range is 0.186207 L. Sigma estimate is 0.165077 L. Individuals limits are 9.518102-10.508564 L. Sample 33 is 10.8 L and exceeds UCL. Cp=1.211556 and Cpk=1.184632 are provisional illustrations. The signal prevents an unqualified stability claim for the full series.

Calibration-evidence and blocked-strainer categories total 20 of 30 defect records, or 66.7 percent. This ranks investigation categories but does not prove the fill signal has either cause. Fishbone alternatives include measurement, machine, method and material. A 5-Whys branch about measurement drift must stop pending calibration and independent-reading evidence.

### Improve

Propose a controlled investigation comparing an approved reference measurement with process readings. The process reviewer must approve its safe scope and acceptance criteria. Do not change equipment or operating parameters on the basis of this classroom report.

### Control

Retain time order, source versions and baseline estimates. Define a named reviewer, agreed sampling cadence and response to future signals. Preserve the signal record. Revise limits only through an evidence-backed process review, not to conceal an outlier.

### Management slide outline

Finding: monitoring sample 33 exceeds UCL. Evidence: 30 baseline and five monitoring values. Constraint: root cause and measurement validity are unresolved. Decision request: review a controlled investigation with a named owner. Status: draft for professional review.
