# CW-401 dosing consistency investigation 

Original synthetic IES training case. Fictional assets, people, observations and engineering requirements. No real operating limits or work authorisation. Trainer-authored prompts are included in the workbook.

A fictional industrial cooling-water utility uses duty/standby metering pumps DP-401A/B. The workshop CTQ is measured delivery during a standardised collection test at fixed commanded setting. The design-note teaching target is 62.0 L/h with an acceptance band of 58.9–65.1 L/h; this is a delivery-test specification, not a chemical dose or water-quality compliance limit. Chemical identity and operating procedures are deliberately outside the case.

A repeatability study and comparison of pump delivery are needed before a maintenance recommendation. The team has 60 baseline collection tests, 30 subsequent monitoring tests and 30 post-intervention pilot tests. Collection volume is measured over 120 seconds; delivery L/h = collected litres × 30. The command setting is fixed for comparability; shift and pump identity are retained to detect confounding.

The monitoring period includes a sustained delivery reduction coinciding with a differential-pressure increase. A work order records inspection and a strainer replacement before the pilot. This temporal association does not isolate root cause: the pilot also follows a verification check, so intervention effects are confounded. No randomised causal claim is justified.

Three seeded data-quality issues are preserved in the raw export: a missing collection volume, one invalid-test flag and an exact duplicate event. Do not delete a process excursion because it is an outlier. Keep the baseline fixed and investigate instability before interpreting capability.
