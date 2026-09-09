# Lab 4.4 - Researcher and Analyst

**Purpose:** Use Microsoft's built-in Researcher and Analyst agents for two different tasks and independently check their evidence.

**Output:** One cited research comparison and one checked analysis of the supplied CSV.

## What you will do

1. Open the built-in Researcher agent.
2. Run the supplied comparison prompt and open at least one citation.
3. Record whether the cited passage supports the associated claim.
4. Open the built-in Analyst agent.
5. Attach `mock-data.csv` and request a calculation and limitation statement.
6. Reproduce the important values yourself.
7. Compare the strengths and limits of Researcher and Analyst.

## Files used

| File | Use |
|---|---|
| `Lab-Instructions.pdf` | Detailed instructions. |
| `mock-data.csv` | File analysed by Analyst. |

## Part A - Researcher

1. Open Microsoft 365 Copilot and select **Researcher** from the available agents.
2. Start a new research task using the complete Researcher prompt below.
3. Require a comparison table, citations and a limitations section.
4. Wait for the research response to finish.
5. Select one important factual claim and open its citation.
6. Compare the exact source passage with the claim.
7. Record one of these outcomes: **Supported**, **Partly supported**, **Not supported**, or **Citation inaccessible**.
8. If unsupported, revise or remove the claim rather than accepting the citation marker.

### Researcher prompt

```text
Act as an engineering research assistant. Compare how NIST AI RMF 1.0 and ISO/IEC 42001
address evidence, human oversight and risk treatment for AI-assisted engineering work.
Use primary or official sources. Return a comparison table with Claim, Source, Date,
Direct support and Limitation. Cite every factual claim. Separate source statements from
your interpretation and list unresolved differences for human review.
```

## Part B - Analyst

1. Open the built-in **Analyst** agent in a fresh conversation.
2. Attach `mock-data.csv`.
3. Paste the complete Analyst prompt below.
4. Require it to preserve 59.4 L/h and 62.0 L/h, calculate their difference and identify the missing approved limit.
5. Check the row count, values, units and missing field against the CSV.
6. Reproduce the calculation yourself: `62.0 - 59.4 = 2.6 L/h`.
7. Reject any claim that the test failed an approved limit because that limit is not supplied.

### Analyst prompt

```text
Analyse only the attached mock-data.csv. State the row count and preserve every supplied
value, unit, source and status. Calculate the difference between the delivery test result
and reference target, showing the formula. Identify all missing values. Do not describe the
difference as a violation because the approved operating limit is not supplied. Return
Observed facts, Calculation, Missing evidence and Reviewer caution.
```

## Compare the agents

| Agent | Appropriate use | Required human check |
|---|---|---|
| Researcher | Multi-source external research | Open citations and compare source passages with claims |
| Analyst | File-based calculation and interpretation | Reproduce formulas, row counts, units and missing-value handling |

## Pass conditions

- Researcher returns cited claims and the learner opens at least one citation.
- The selected citation is classified against the actual passage.
- Analyst uses exactly three data rows and preserves the units.
- The 2.6 L/h difference is independently reproduced.
- No approved limit, cause or safety conclusion is invented.
- The learner records which agent fits which task.

All supplied records are fictional classroom data.
