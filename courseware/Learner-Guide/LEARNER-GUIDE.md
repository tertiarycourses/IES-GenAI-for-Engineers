# GenAI for Engineers Learner Guide

IES | Version 1.1

All records are fictional training data. They describe no actual facility, person or organisation. Values are teaching assumptions, not approved design criteria. Do not use outputs to operate, maintain or approve real equipment.

## Module 1 The Copilot ecosystem for engineers

### From language generation to engineering evidence

A language model composes a response from the context supplied to it. Its fluency does not establish that an equipment condition, calculation or source is correct. In this course, Copilot is used to structure evidence and draft documents while the engineer retains responsibility for interpretation and release. PS-17 has an intermittent indicated-flow event, but the source does not establish a failed pump. This distinction is the central review habit throughout the day.

### Choosing the working surface

Use Copilot Chat to structure a short source text or question. Use Word to develop a document, Excel to inspect data and calculations, and PowerPoint to communicate the reviewed conclusion. Agents package instructions and selected knowledge for repeated tasks. SharePoint provides a controlled source location. These roles complement each other; a chat session does not automatically create a scheduled workflow or a permission boundary.

### Access and participation

Use the corporate account and approved tenant. Confirm licence, application access, agent policy and source permissions before beginning. Microsoft navigation and capability availability vary across tenants. The current Microsoft guide uses New agent, Configure and Try it in Microsoft 365 Copilot; the supplied proposal calls this Copilot Studio agent builder. The lab uses the current entry point while retaining the intended agent-building outcome. If a capability is unavailable, use approved paired work or the local source files and record the live outcome as incomplete.

### Measuring useful productivity

Compare the same input, deliverable and quality criteria for manual and AI-assisted work. Record drafting, review and correction time separately. A faster first draft with more unsupported claims is not evidence of a productivity gain. Lab 1.2 provides a classroom benchmark; it is not a general industry statistic. Record the number of facts that needed correction and the evidence that remains missing.

### Map the petroleum evidence lifecycle

Exploration combines seismic interpretation, well logs and geological models; drilling adds time-series measurements; production adds rates, pressures, water cut and maintenance histories. Each dataset represents a different physical question and sampling scale. A language model can summarise an approved interpretation, but that does not make it a reservoir simulator. Begin by naming the asset, decision, evidence owner and required review. The ebook motivates this lifecycle perspective in Chapters 3–7.

### Predictive AI and generative AI have different contracts

Regression estimates a numerical target such as production rate; classification assigns a defined category; clustering groups similar records without proving a physical mechanism. Generative AI drafts new content conditioned on a prompt and context. A useful combined workflow is a validated analytical result followed by a source-linked explanation. Do not ask a language model to invent a forecast and present it as a trained predictive model. A table of plausible values is not model validation.

### Establish the decision time

For a maintenance forecast made at 08:00, only information available by 08:00 is eligible as an input. A repair completion note written the following day leaks future information even if it is on the same asset row. Record event time and availability time separately. Define the prediction horizon and target before choosing inputs, and evaluate on later periods or unseen assets according to the intended deployment.

### Lab 1.1 Copilot onboarding and access check

[Open the complete lab](../Labs/Lab-1-1-copilot-onboarding-and-access-check/README.md). 10 minutes.

### Lab 1.2 AI versus engineer challenge

[Open the complete lab](../Labs/Lab-1-2-ai-versus-engineer-challenge/README.md). 15 minutes.

## Module 2 Prompting for engineering documents

### RISE and EMAP

R.I.S.E. means Role, Input, Steps and Expectations. It describes the writing task, names permissible evidence, specifies a reasoning or checking sequence and states the output criteria. E-MAP means Engineering, Metrics, Assumptions and Parameters. It makes the engineering context, measurable acceptance, unknowns and operating boundaries explicit. Use R.I.S.E. for a source-to-document task and E-MAP when uncertainty or constraints are central. Both require a verification pass.

### Requirements and traceability

A defensible requirement includes an identifier, value, unit, source version, source location and acceptance evidence. In DES-01 revision 2, nominal delivery is 50 m3/h at 30 m head. The teaching tolerance is plus or minus 5 percent, giving a band of 47.5 to 52.5 m3/h. These are synthetic design-note values, not statutory or industry requirements. Wetted material, supply voltage and ambient conditions are deliberately unresolved; the correct draft preserves those gaps.

### Observation and inference

An inspection report separates direct observations, reported statements, hypotheses and missing evidence. The site notes describe liquid near a coupling but do not identify it. A suggested seal leak remains a hypothesis. To record a non-conformance, cite both the observed condition and the requirement it violates; otherwise identify a potential issue requiring review. The executive summary must preserve this uncertainty even when technical detail is shortened.

### Risk and method statement boundaries

Lab 2.3 is a planning desk exercise. Chemical identity, SDS and approved isolation details are missing. The risk table must therefore expose evidence gaps and competent-person review gates. It cannot prescribe chemical-specific PPE, exposure limits or operational isolation steps. A method-statement planning outline should point to approved site procedures and state prerequisites, hold points and handback responsibilities. No training output authorises physical work.

### A petroleum data contract

Record asset ID, timestamp with time zone, physical quantity, unit, sampling interval, measurement method, missing-value codes and source version. A pressure number without a unit cannot safely be combined with another pressure column. In the teaching case, 20 bar and 2000 kPa are equivalent, using 100 kPa per bar. The missing pressure remains unknown. Preserve raw readings and record every transformation in a cleaning ledger.

### Missing values and outliers need engineering context

An empty field may mean sensor outage, not zero process pressure. Repeated timestamps may represent ingestion duplicates or separate instruments; inspect keys before deduplication. An abrupt 200 bar reading may be a unit error, instrumentation issue or real event. Flag it for review rather than replacing it just because it is far from the average. The ebook discusses imputation and outlier treatment in Chapter 3; this course adds a raw-data preservation gate.

### Turn observations into a reviewable report

Separate a measured pressure, an operator comment, a hypothesis and an approved finding. A sheen in a photograph does not establish hydrocarbon identity or source. Ask the model for an evidence table with record IDs, uncertainties and follow-up questions. Require the report to retain contradictory evidence and missing calibration records. A polished document may still be incomplete for engineering release.

### Lab 2.1 Technical specification with RISE

[Open the complete lab](../Labs/Lab-2-1-technical-specification-with-rise/README.md). 20 minutes.

### Lab 2.2 Site notes to an engineering report

[Open the complete lab](../Labs/Lab-2-2-site-notes-to-an-engineering-report/README.md). 15 minutes.

### Lab 2.3 Risk assessment and method statement with EMAP

[Open the complete lab](../Labs/Lab-2-3-risk-assessment-and-method-statement-with-emap/README.md). 20 minutes.

## Module 3 Engineering methodologies and document automation

### FMEA from function to action

Failure Mode and Effects Analysis examines how a function could fail, what effect follows, what could cause it and which current controls exist. Keep a failure mode distinct from its effect: no flow is a mode, underdose is an effect. The provided scale uses provisional severity, occurrence and detection ratings from 1 to 10; higher detection scores mean poorer detection. F01 gives 8 x 4 x 6 = 192; F02 gives 9 x 3 x 7 = 189; F03 gives 7 x 5 x 5 = 175. High-severity rows need attention even when their RPN is not the largest. A proposed action cannot justify reduced residual ratings before implementation and effectiveness evidence.

### DMAIC connects a problem to a control plan

Define identifies the problem, scope and critical-to-quality characteristic. Measure establishes units, data quality and baseline. Analyse distinguishes signals and causal hypotheses from demonstrated causes. Improve proposes a controlled trial, owner and review gate. Control defines the metric, cadence, reaction plan and responsible person. A Pareto chart ranks counts; a fishbone organises possible causes; a 5-Whys chain requires evidence at each link. None of these tools alone establishes causation.

### Individuals charts and the teaching dataset

The fill dataset contains 30 baseline readings and five later monitoring readings in litres. Preserve time order. Estimate short-term sigma from the average absolute difference between successive baseline observations divided by 1.128. The centre is 10.01333 L, average moving range 0.18621 L and sigma estimate 0.16508 L. The individuals limits are the centre plus or minus three sigma: 9.51810 and 10.50856 L. Sample 33 is 10.8 L and exceeds the upper limit. Investigate the signal; do not infer a root cause or redraw limits to hide it. The lab introduces a single beyond-limit rule rather than a complete control-chart interpretation system.

### Capability is conditional

Specification limits come from the requirement; control limits come from observed process behaviour. Teaching specifications here are 9.4 and 10.6 L. Cp is specification width divided by six estimated sigma; Cpk is the smaller distance from the mean to a specification limit divided by three sigma. The illustrative values are Cp 1.212 and Cpk 1.185. They are provisional because the sample is small and stability, independence, measurement suitability and the distribution model require review. Do not declare the full dataset stable or the process certified capable. See the NIST sources in REFERENCES.md.

### Transfer across disciplines

The specification, design checklist, SOP planning outline and troubleshooting guide express the same evidence in four forms. Transfer the document pattern across disciplines but do not transfer irrelevant numeric criteria. For example, an electrical panel needs approved supply and protection information; a pump design note cannot provide those ratings. Preserve the missing fields and ask a domain reviewer to identify the correct authority.

### Reliability analysis links several evidence types

A vibration excursion is a condition-monitoring signal. A diagnosis attributes that signal to a cause. A remaining-useful-life estimate forecasts a failure horizon and needs a validated model and uncertainty assessment. They are distinct claims. FMEA remains useful for mapping the function, possible failure mode, effect, hypothesised cause and current control. Proposed inspection does not count as an effective existing control.

### Evaluate alarm quality beyond accuracy

The synthetic review set contains 20 labelled events: 6 true positives, 2 false negatives, 3 false positives and 9 true negatives. Accuracy is 15/20 = 75%; precision is 6/9 = 66.7%; recall is 6/8 = 75%; F1 is 12/17 = 70.6%. An always-negative classifier is 60% accurate here and misses every positive. This small deliberately balanced exercise is not a deployment benchmark. Discuss the consequences of a missed event and unnecessary inspection separately.

### Forecast error retains its physical unit

The synthetic six-well holdout has actual rates 100,120,80,150,90,110 and predicted rates 110,100,85,145,100,100 bbl/day. Absolute errors sum to 60; MAE is 10 bbl/day. Squared errors sum to 750; RMSE is sqrt(750/6) = 11.18 bbl/day. Mean signed error, prediction minus actual, is -1.67 bbl/day. These predictions are supplied mock outputs, not a model trained in class. The six rows cannot establish generalisation.

### Process control and model monitoring answer different questions

SPC monitors process behaviour against a defined baseline. Model monitoring checks whether prediction errors, input distributions or missingness change over time. A stable pressure process does not establish accurate failure prediction, and accurate forecasts do not establish safe operation. Keep the original DMAIC/SPC exercise; use the petroleum variant to compare data quality and model evaluation. Recalibration needs a governed change, not silently moving limits to remove a signal.

### Lab 3.1 FMEA document generation

[Open the complete lab](../Labs/Lab-3-1-fmea-document-generation/README.md). 30 minutes.

### Lab 3.2 DMAIC report and SPC analysis

[Open the complete lab](../Labs/Lab-3-2-dmaic-report-and-spc-analysis/README.md). 25 minutes.

### Lab 3.3 Discipline specific specification pack

[Open the complete lab](../Labs/Lab-3-3-discipline-specific-specification-pack/README.md). 20 minutes.

## Module 4 Copilot agents and reasoning agents

### Agents make a task reusable

An agent combines a purpose, instructions, knowledge sources and reusable starting prompts. It does not remove the need for review. The FMEA Assistant must ask for missing rating scales, preserve the difference between controls and proposals, and return sources with provisional ratings. The Report Writer must follow the selected weekly or DMAIC template and preserve open actions. Grounding the agent on an obsolete or incomplete template can repeat the same mistake on every run.

### Build and test the contract

In Microsoft 365 Copilot, use New agent and Configure or the available equivalent. Add a descriptive name, task instructions, selected training knowledge and starter prompts. Use Try it to test a normal request, missing source, conflicting versions and an embedded instruction to bypass review. Record observed responses, not only intended behaviour. Create or save the agent and share only within approved policy. A shared agent does not automatically grant the recipient access to its source files.

### Interactive chaining and recurring operation

Lab 4.3 performs a minutes-to-tracker-to-report chain interactively. Action IDs support deduplication: A03 appears twice in the minutes but becomes one tracker row. A04 has no owner or date and must retain TBD fields. A recurring production workflow additionally needs a configured trigger, approved input storage, review and release gates, duplicate handling, logging, failure notification and an accountable owner. Discuss these requirements without claiming that a prompt has deployed a scheduled flow.

### Researcher and Analyst

Use Researcher for a bounded comparison with verifiable primary sources. Open the citations and check that the relevant claim is supported; a publisher catalogue entry cannot establish a full standard clause. Use Analyst with an explicit data contract: units, selected baseline rows, monitoring rows, missing-value treatment and estimator. Compare the returned results with independent Excel calculations. If the specialised agents are unavailable, document the fallback and do not claim a live specialised-agent result.

### Build agents around bounded decisions

A petroleum reliability assistant should draft an FMEA from approved evidence and identify gaps; it should not issue shutdown instructions. A report agent should preserve source clauses and status. A Researcher request can compare published methods while an Analyst request checks supplied data. Tool availability and actual execution must be recorded. Do not label a manual prompt chain as an autonomous operating system.

### Test with positive, negative and conflicting cases

Use a current source, an obsolete revision, an unknown question and an embedded instruction attack. Score whether the output cites the current clause, preserves TBDs, refuses unsupported diagnosis and treats retrieved instructions as data. Repeat tests after source or instruction changes. A useful acceptance criterion is all required facts traceable with zero invented approvals; fluent style alone is insufficient.

### Give an analyst a reproducible evaluation contract

Specify the 20 event rows, the positive class, actual and predicted columns and formulas. Ask for TP, FN, FP and TN counts before derived metrics. Independently inspect the row IDs in each count. For regression, retain units and the sign convention for bias. Require the agent to identify that mock predictions are supplied, with no training or live validation demonstrated.

### Lab 4.1 Build an FMEA Assistant agent

[Open the complete lab](../Labs/Lab-4-1-build-an-fmea-assistant-agent/README.md). 25 minutes.

### Lab 4.2 Build a Report Writer agent

[Open the complete lab](../Labs/Lab-4-2-build-a-report-writer-agent/README.md). 20 minutes.

### Lab 4.3 Minutes to action tracker to report

[Open the complete lab](../Labs/Lab-4-3-minutes-to-action-tracker-to-report/README.md). 15 minutes.

### Lab 4.4 Researcher and Analyst

[Open the complete lab](../Labs/Lab-4-4-researcher-and-analyst/README.md). 15 minutes.

## Module 5 SharePoint integration with Copilot

### Controlled knowledge for grounded answers

A SharePoint agent should use a deliberately selected library or set of current references. The teaching library contains a current design note, an obsolete revision, O&M information and a past-project summary. The current design note supports duty values; the past-project summary does not establish the cause of the current fault. Good retrieval depends on source scope, readable content, versions and document ownership.

### Verify citations and conflicts

For each critical claim, record the document title, revision, clause or page, supported statement and source URL when available. Open the original source. DES-01 revision 1 says 45 m3/h but is explicitly obsolete; revision 2 says 50 m3/h. The answer should use the current reference and explain the conflict. Where materials remain TBD, the agent should say that evidence is missing rather than supply a likely grade.

### Test the recipient boundary

The trainer creates a separate restricted test library containing only a synthetic sentinel. A learner test account without access should fail direct access and should not obtain the content through the agent. Do not put the sentinel file in the learner-accessible training library during that test. If a separate account is unavailable, mark the test not executed. A successful answer to an ordinary question does not establish correct permission behaviour.

### Keep provenance during handoff

Before a retrieved answer is passed to FMEA Assistant or Report Writer, complete a handoff record with the supported statement, source version, location and uncertainty. Review the downstream draft for lost qualifiers or new unsupported facts. Reverse-trace a sentence from the final document to the handoff and original clause. Source and agent owners should retest whenever a relevant document, instruction or access policy changes.

### Petroleum knowledge has version and asset scope

Design basis, inspection observations and operating procedures have different authority. A document for another train or field must not silently determine the current asset requirement. Use asset tags, document IDs, revisions, approval status and effective dates in the library. The fictional PET-DES rev2 establishes a classroom pressure band; rev1 is obsolete. Neither constitutes a real operating envelope.

### Retrieval quality is more than a plausible citation

Check that the cited clause actually supports the answer, that the revision is current and that the reader has permission to access it. An answer that cites the right document but invents material compatibility still fails. If the evidence says fluid composition is unknown, the downstream agent must preserve that gap. Unsupported statements should become an evidence request, not an averaged compromise.

### Preserve uncertainty across agent handoffs

Transfer the claim, exact source location, revision, unit, known gap and review status together. Then reverse-trace the final report sentence to the original clause. Test retrieval and handoff separately so a summarisation error is distinguishable from an access or search failure. Re-run the affected tests whenever source scope or ownership changes.

### Lab 5.1 SharePoint knowledge agent

[Open the complete lab](../Labs/Lab-5-1-sharepoint-knowledge-agent/README.md). 25 minutes.

### Lab 5.2 End to end agent workflow

[Open the complete lab](../Labs/Lab-5-2-end-to-end-agent-workflow/README.md). 15 minutes.

## Module 6 AI security and the engineering toolkit

### Seven controls with evidence

The framework in the supplied proposal comprises data classification; data governance and access control; secure prompting; output verification and hallucination detection; human-in-the-loop sign-off; traceability and audit; and security awareness and incident response. Each control needs evidence or an explicit gap. The classroom classification categories are examples and must be mapped to the organisation policy before workplace use.

### Verify before release

The seeded draft contains unsupported diagnosis, an obsolete duty, invented material compatibility, incorrect RPN, unjustified severity reduction, a false stability claim, invented certificate completion and false approval. A polished format does not mitigate these issues. The reviewer must check sources, calculations, units and unresolved assumptions. Record preparer, competent reviewer, evidence checked, release decision and reviewed version; the AI response itself cannot grant authority.

### Respond to untrusted instructions

The injection fixture asks the reader to omit evidence and mark a report approved. Treat that instruction as untrusted source content. Stop using affected output, preserve the source, prompt, response and timestamps, and report through the organisation approved channel. Do not invent an internal contact or discard the evidence. Resume only after controlled correction and retesting.

### Create a toolkit that can be evaluated

Retain tested R.I.S.E. and E-MAP prompts, source versions, agent ownership and access scope, acceptance checks and a human release gate. Choose one bounded trial for next week. Measure total time including review and correction, and count unsupported claims. State a stop condition such as untraceable evidence or unapproved access. Keep blueprint-only agents and unexecuted tests visibly distinct from completed live work.

### Environmental signals require corroboration

Pressure imbalance, an image and an operator report can support investigation, but none alone establishes leak composition or quantity. False negatives and false positives have different consequences. Do not convert the absence of an alarm into a claim of safety. Keep generated text separate from operational alarms and follow approved incident procedures outside this classroom scenario.

### Govern the complete evidence chain

Classify geological, production and inspection data before use; restrict agent access to approved sources; redact unnecessary identifiers; validate outputs; retain competent sign-off; preserve the audit trail; define an incident response owner. A malicious instruction in a retrieved document must not change these boundaries. Correcting the output is one step; preserve the original evidence and record the affected version.

### Measure a bounded petroleum trial

Select one repeatable reporting task and compare total preparation, review and correction time at equal acceptance criteria. Record unsupported claims, unit errors and missed evidence as well as minutes saved. Stop the trial if access is unapproved or critical claims cannot be traced. The ebook offers broad industry cases, but this course does not treat those narratives as independently verified company performance results.

### Lab 6.1 Apply the seven step AI Security Framework

[Open the complete lab](../Labs/Lab-6-1-apply-the-seven-step-ai-security-framework/README.md). 20 minutes.

### Lab 6.2 Build the personal engineering AI toolkit

[Open the complete lab](../Labs/Lab-6-2-build-the-personal-engineering-ai-toolkit/README.md). 10 minutes.
