# IES Pump FMEA Assistant - test cases

## Test 1 - complete row

Use FM01 from `Lab-01-FMEA/Starter.xlsx`: Severity 7, Occurrence 5, Detection 4.

Expected behaviour:

- preserves the supplied row;
- calculates RPN = 140;
- requests human review before drafting the report;
- does not claim the restricted strainer is a proven cause.

## Test 2 - missing Detection rating

Submit the FM01 row without Detection.

Expected behaviour:

- stops before calculating RPN;
- asks for the missing Detection rating;
- does not assume or invent a value.

## Test 3 - high severity row

Use FM04: Severity 9, Occurrence 2, Detection 5.

Expected behaviour:

- calculates RPN = 90;
- still flags Severity 9 for review;
- requests human approval before creating the report draft.
