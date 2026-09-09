# Lab 5.2 - Grounded Agent Chain

**Purpose:** Pass a verified SharePoint excerpt into the Report Writer agent while preserving a human review gate between retrieval and drafting.

**Output:** A cited source excerpt, reviewer check record and grounded report draft.

## What you will do

1. Ask the Lab 5.1 Knowledge Agent for a requirement.
2. Open and verify the citation.
3. Record the approved excerpt and reviewer.
4. Pass only that checked excerpt to the Lab 4.2 Report Writer.
5. Generate a draft that preserves the source and limitation.
6. Trace the final report back through both agent stages.
7. Reject any unchecked or invented context.

## Required agents

- The private **IES Engineering Knowledge Assistant** created in Lab 5.1.
- The private **IES Report Writer** created in Lab 4.2.

If either agent was not created successfully, stop and use the trainer demonstration rather than pretending the chain ran.

## Detailed steps

1. Open the Lab 5.1 Knowledge Agent in a fresh chat.
2. Ask: `Which fields must TR-401 record? Cite the exact source location.`
3. Open every citation used for the answer.
4. Compare the cited passage with the returned fields.
5. Copy only the supported excerpt into a review record containing:
   - source filename;
   - revision or version if stated;
   - section or clause;
   - exact supported fields;
   - reviewer name;
   - review date;
   - decision: Approved as drafting context / Revise / Reject.
6. Continue only if the decision is **Approved as drafting context**.
7. Open the Lab 4.2 Report Writer in a new chat.
8. Paste the checked excerpt and review record. Do not paste the Knowledge Agent's unchecked narrative.
9. Paste this request:

```
Using only the checked excerpt and review record below, draft a short engineering
report section with Source requirement, Current evidence, Missing evidence,
Next action and blank Reviewer decision. Preserve the source filename, revision,
clause and reviewer record exactly. Do not add facts from general knowledge.
End with DRAFT FOR REVIEW.
```

10. Compare the final draft with the checked excerpt.
11. Confirm that every factual statement traces to the approved context.
12. Test the boundary by asking for the approved delivery limit. The chain must preserve NOT FOUND rather than inventing a value.

## Traceability chain

`SharePoint source -> Knowledge Agent answer -> opened citation -> human-approved excerpt -> Report Writer draft -> final human review`

## Pass conditions

- The retrieved citation was opened before handoff.
- The handoff contains only checked context.
- Source filename, revision and location are preserved.
- The final draft does not introduce an approved limit or new evidence.
- The reviewer decision remains blank.
- Both agents remain within their approved access boundaries.

All records are fictional classroom data.
