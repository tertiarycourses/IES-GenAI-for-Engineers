# GenAI for Engineers Learner Guide

IES | Version 1.0

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

### Lab 6.1 Apply the seven step AI Security Framework

[Open the complete lab](../Labs/Lab-6-1-apply-the-seven-step-ai-security-framework/README.md). 20 minutes.

### Lab 6.2 Build the personal engineering AI toolkit

[Open the complete lab](../Labs/Lab-6-2-build-the-personal-engineering-ai-toolkit/README.md). 10 minutes.
