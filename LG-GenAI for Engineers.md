# GenAI for Engineers — Learner Guide

**Course:** GenAI for Engineers  |  **Conducted by:** IES Academy  |  **Version v2.4 · 19 October 2026**

## Contents

- [Introduction](#introduction)
- [Course Learning Outcomes](#course-learning-outcomes)
- [Before You Start — Preparation](#before-you-start--preparation)
- [Topic 1 — Fundamentals of Microsoft 365 Copilot](#topic-1--fundamentals-of-microsoft-365-copilot)
  - [The Microsoft 365 Copilot Interface](#the-microsoft-365-copilot-interface)
  - [Grounding Across Microsoft 365](#grounding-across-microsoft-365)
  - [Work-Order Grain and Reporting Measures](#work-order-grain-and-reporting-measures)
  - [Lab 1 · Excel to Word — Prepare Work Orders and Draft the Operations Brief](#lab-1--excel-to-word--prepare-work-orders-and-draft-the-operations-brief)
  - [Prompts and Verified App Handoffs](#prompts-and-verified-app-handoffs)
  - [Outlook Drafting and Operational Decisions](#outlook-drafting-and-operational-decisions)
  - [Lab 2 · Word to PowerPoint and Outlook — Create the Cross-App Maintenance Update](#lab-2--word-to-powerpoint-and-outlook--create-the-cross-app-maintenance-update)
  - [Topic 1 Recap - Mapped to Learning Outcomes](#topic-1-recap---mapped-to-learning-outcomes)
- [Topic 2 — Personalisation, .Rules and Skills for Excel](#topic-2--personalisation-rules-and-skills-for-excel)
  - [Account Personalisation and Specific Requests](#account-personalisation-and-specific-requests)
  - [Lab 3 · Personalisation — Personalise Copilot in Excel for Consistent Service Reports](#lab-3--personalisation--personalise-copilot-in-excel-for-consistent-service-reports)
  - [Visible Workbook .Rules and Formula Results](#visible-workbook-rules-and-formula-results)
  - [Lab 4 · Workbook .Rules — Create and Test Workbook .Rules for Water Service Reporting](#lab-4--workbook-rules--create-and-test-workbook-rules-for-water-service-reporting)
  - [What Is a Skill? Inside SKILL.md](#what-is-a-skill-inside-skillmd)
  - [Built-in and Custom Skills](#built-in-and-custom-skills)
  - [Pareto Skill: Find the Vital Few Failure Modes](#pareto-skill-find-the-vital-few-failure-modes)
  - [Lab 5 · Custom Pareto Chart Skill — Find the Vital Few Failure Modes with a Pareto Skill](#lab-5--custom-pareto-chart-skill--find-the-vital-few-failure-modes-with-a-pareto-skill)
  - [Skills, Prompts and Workbook Rules](#skills-prompts-and-workbook-rules)
  - [Custom Skill Discovery in Each App](#custom-skill-discovery-in-each-app)
  - [Repeatability and Safe Skill Reruns](#repeatability-and-safe-skill-reruns)
  - [Assignment Proposals and Capacity Evidence](#assignment-proposals-and-capacity-evidence)
  - [Lab 6 · Reporting Skill — Build a Maintenance Report with Two Skills](#lab-6--reporting-skill--build-a-maintenance-report-with-two-skills)
  - [PowerPoint Design Skill: From Plain to Professional](#powerpoint-design-skill-from-plain-to-professional)
  - [Lab 7 · PowerPoint Design Skill — Create a PowerPoint Design Skill: From Plain to Professional](#lab-7--powerpoint-design-skill--create-a-powerpoint-design-skill-from-plain-to-professional)
  - [Topic 2 Recap - Mapped to Learning Outcomes](#topic-2-recap---mapped-to-learning-outcomes)
- [Topic 3 — Interactive Dashboards with Custom Skills](#topic-3--interactive-dashboards-with-custom-skills)
  - [Custom Dashboard Skill as a Reusable Contract](#custom-dashboard-skill-as-a-reusable-contract)
  - [Dashboard Measures and Denominators](#dashboard-measures-and-denominators)
  - [Visual Dashboard Design for Maintenance](#visual-dashboard-design-for-maintenance)
  - [Lab 8 · Custom Dashboard Skill — Build an Interactive Dashboard with a Custom Skill](#lab-8--custom-dashboard-skill--build-an-interactive-dashboard-with-a-custom-skill)
  - [One Filter Scope for Every Visual](#one-filter-scope-for-every-visual)
  - [Refresh Tests and Static Snapshots](#refresh-tests-and-static-snapshots)
  - [Lab 9 · Interactive Filters and Refresh — Test Dashboard Filters and a Data Refresh](#lab-9--interactive-filters-and-refresh--test-dashboard-filters-and-a-data-refresh)
  - [Topic 3 Recap - Mapped to Learning Outcomes](#topic-3-recap---mapped-to-learning-outcomes)
- [Topic 4 — Create a Professional Presentation with PowerPoint Copilot](#topic-4--create-a-professional-presentation-with-powerpoint-copilot)
  - [From Dashboard Evidence to a Decision Story](#from-dashboard-evidence-to-a-decision-story)
  - [Charts, Templates and Source Provenance](#charts-templates-and-source-provenance)
  - [Lab 10 · Dashboard to presentation — Turn Dashboard Evidence into a Management Story](#lab-10--dashboard-to-presentation--turn-dashboard-evidence-into-a-management-story)
  - [Professional Refinement and Rehearsal](#professional-refinement-and-rehearsal)
  - [Reviewed Handoff and Artifact Lifecycle](#reviewed-handoff-and-artifact-lifecycle)
  - [Lab 11 · Professional handoff — Refine and Present the Maintenance Decision Deck](#lab-11--professional-handoff--refine-and-present-the-maintenance-decision-deck)
  - [Topic 4 Recap - Mapped to Learning Outcomes](#topic-4-recap---mapped-to-learning-outcomes)
- [Topic 5 — Copilot Agents and Mini Capstone](#topic-5--copilot-agents-and-mini-capstone)
  - [What Is Agent Builder?](#what-is-agent-builder)
  - [Lab 12 · Copilot Agent Builder — Build a Work-Order Agent with Agent Builder](#lab-12--copilot-agent-builder--build-a-work-order-agent-with-agent-builder)
  - [Mini Capstone: From Your Data to a Decision](#mini-capstone-from-your-data-to-a-decision)
  - [Lab 13 · Mini Capstone — Mini Capstone: Group Dashboard and Decision Deck](#lab-13--mini-capstone--mini-capstone-group-dashboard-and-decision-deck)
  - [Topic 5 Recap - Mapped to Learning Outcomes](#topic-5-recap---mapped-to-learning-outcomes)
- [Closing: 5 Principles of AI Security](#closing-5-principles-of-ai-security)
- [Next Steps](#next-steps)
- [Glossary](#glossary)


## Introduction

This masterclass follows Northstar Water Services, a fictional water-pipe maintenance and service company, from a dirty service-work-order export to a reviewed management decision pack. Work-order IDs, categories, sites, current assignments and status definitions stay consistent across every app. The purpose is to make evidence travel accurately through the workflow, while using Copilot for drafting, analysis, reusable instructions and visual communication.

Study each topic’s concepts before its connected labs. Topic 2 has five labs; Topics 1, 3 and 4 have two each; Topic 5 has the agent lab and the group mini capstone. Each lab has its own instruction PDF and a lean data folder: the lab workbook and only the templates that lab uses. Copy-ready prompts are on the linked web page, step by step. Every lab is self-contained: work directly on the files in its own data folder, so you can start any lab without finishing the one before. The detailed procedures are here and in labs; the slides teach concepts and show outcomes.


## Course Learning Outcomes

- LO1: Integrate Word, Excel, PowerPoint and Outlook Copilot in a coherent maintenance workflow with explicit source grounding and verified prompts.
- LO2: Distinguish account Personalisation, workbook .Rules and reusable Skills; configure, create, apply and verify Pareto and maintenance-reporting Skills using water-service evidence.
- LO3: Create and apply a custom interactive-dashboard Skill with verified measures, shared filter scope, editable charts and controlled refresh and rerun tests.
- LO4: Continue from the dashboard to a professional management presentation, with evidence-based headlines, source notes, rehearsal and a reviewed handoff draft.
- LO5: Build and test a grounded work-order agent with Agent Builder, then apply the full data-to-decision workflow to your own mock or sanitised data in a group capstone.


## Before You Start — Preparation

**What you need**

- Assigned Microsoft 365 account with Copilot in Word, Excel, PowerPoint and Outlook; licence and tenant settings checked before class.
- Desktop Excel on Windows or Mac (current version) with English display language for Excel custom skills; workbooks stay in the downloaded lab folders, with no OneDrive upload.
- The downloaded lab folders; you work directly on the files in each lab’s data folder. All sample data is synthetic.
- Copilot skills access in both Excel and PowerPoint. If unavailable, the lab supplies a clearly labelled manual-instruction practice route.

**Verify your setup**

Open one workbook and one Word/PowerPoint template; find each Copilot button. Open a lab workbook from its data folder and confirm Excel Copilot answers on it; in Word Copilot confirm + > Upload images and files can upload it (a local file cannot be found with / or @). Use the app-created custom skills folder rather than guessing a path. Keep Formulas > Calculation Options > Automatic. Never paste account passwords into a prompt.

**Conventions used in every lab**

- App-labelled prompts run in the named app; a prompt in one app is not automatically visible to another.
- Use Chat only for inspection, Plan for reviewed proposals, and Allow editing for authorised workbook changes when these modes are available.
- All comparisons use the same source table, reporting date and filter scope. Missing values remain UNKNOWN; zero closed denominator is N/A.


## Topic 1 — Fundamentals of Microsoft 365 Copilot

One verified maintenance workflow across four apps

**Key concepts**

- Large language models — Understand your request and generate natural-language answers.
- Grounding — Answers anchored in your work data: emails, files, meetings.
- Permissions & privacy — Shows only data you can access; prompts do not train the models.
- Prompts — State the goal, context, source and expectations.

Concepts for Lab 1: The Microsoft 365 Copilot Interface, Grounding Across Microsoft 365, Work-Order Grain and Reporting Measures.


### The Microsoft 365 Copilot Interface

Copilot in the browser and in each Office app shares one set of controls. Microsoft Copilot (copilot.cloud.microsoft) and the Copilot pane in Word, Excel, PowerPoint and Outlook offer a model selector, new chat and chat history, a + menu to reference files and choose skills, settings for Personalization and Manage plugins & skills, and in Excel a mode switch between Chat only, Plan and Allow editing. Agents & Skills in the left pane opens your agents and Agent Builder.

Knowing where each control lives lets you choose how much reasoning, context and authority Copilot gets for a task. A new chat starts a clean context; a reference adds a specific file; a mode decides whether Copilot only answers, proposes a plan or edits the file. The green shield confirms enterprise data protection for work data.

**How it works**

- Pick the model and start a new chat.
- Reference the file or choose a skill.
- Choose Chat only, Plan or Allow editing.
- Review history, settings and skills.

**Two Ways to Give Copilot a File: Local or OneDrive**

| Aspect | Local file (this course) | OneDrive / SharePoint file |
|---|---|---|
| Where it lives | Your computer, e.g. the downloaded lab folder. | OneDrive or SharePoint in Microsoft 365. |
| In Excel | Desktop Excel Copilot works on the open workbook; no upload needed. | Excel desktop or web; AutoSave keeps the cloud copy current. |
| In Word, PowerPoint, Outlook | + > Upload images and files, then pick the file on your device. | Type / or use + > Attach cloud files and pick the file. |
| / or @ mention | Not available: / lists only cloud files; @ calls skills and agents. | / lists the OneDrive and SharePoint files you can open. |
| After you edit | The upload is a copy: upload again after changing the file. | The reference reads the latest saved cloud version. |
| Use it for | Training labs and files you do not want in the cloud. | Shared team files, agent knowledge and folder references. |

**Worked example**

- Auto is the default model; Think deeper suits multi-step analysis.
- Local file: upload it with +. OneDrive file: reference it with /.
- Chat only for inspection, Plan before edits, Allow editing to apply.

**Decision guide**

| Use when | Avoid when |
|---|---|
| You need to control context, reasoning depth or edit permissions. | You assume a chat in one app is visible in another. |

**Authoritative references**

- https://learn.microsoft.com/en-us/microsoft-365/copilot/microsoft-365-copilot-overview
- https://support.microsoft.com/en-us/excel/copilot/copilot-in-excel-skills

---


### Grounding Across Microsoft 365

Grounding gives an AI request the specific evidence it should use. A work-grounded Copilot experience can use permitted organisational content; a file-grounded request uses selected files or supplied text. Neither makes an inaccessible file available merely because its local path is typed into a prompt. Word, Excel, PowerPoint and Outlook have different current-document and file-reference experiences. Treat each app handoff as a new grounding task.

A maintenance figure can be correct in Excel yet become wrong in an email when the source, reporting date or filter scope changes. Explicit grounding prevents unsupported owner assignments, stale reporting periods and invented approvals from entering the pack. A Copilot response is a draft or hypothesis until the underlying evidence has been checked.

**How it works**

- Identify the authoritative work-order table.
- Provide goal, context, source and expected output.
- Review against the named evidence.
- Pass a verified snapshot to the next app.

**Worked example**

- Excel analyses tblWorkOrders; Word receives the checked summary.
- PowerPoint receives the reviewed Word brief; Outlook receives the same checked values.
- An Excel chat transcript is not an automatic PowerPoint data source.

**Decision guide**

| Use when | Avoid when |
|---|---|
| The source is accessible and the output has an explicit audience. | The prompt assumes access to another app chat or local path. |

**Authoritative references**

- https://support.microsoft.com/en-us/microsoft-365-copilot/file-formats-supported-by-microsoft-365-copilot
- https://support.microsoft.com/en-gb/word/copilot/draft-and-add-content-with-copilot-in-word

---


### Work-Order Grain and Reporting Measures

A row represents one work order, identified by Work_Order_ID. Site, job category, priority, status and current assignment are dimensions used to group or filter records. Measures are defined calculations. The source is a snapshot at 30 September 2026: current backlog excludes Closed and Cancelled; overdue backlog also has a Due_Date before that date. Closed orders are counted separately from jobs still in the queue.

An exact duplicated export row changes counts and cost without representing new work. Normalising a category spelling must not change the business meaning or assign a missing owner. Named Excel tables and structured references let formulas expand when legitimate new rows are appended. Preserve the raw export so a cleaning decision can be traced.

**How it works**

- Define one ID per work order.
- Find exact repeated export records.
- Standardise labels without inventing facts.
- Reconcile cleaned counts and cost.

**Worked example**

- 122 raw rows contain 120 distinct work-order IDs.
- Total = Closed + Cancelled + Backlog after exact duplicate removal.
- Due on 30 September is not overdue at the 30 September snapshot.

**Decision guide**

| Use when | Avoid when |
|---|---|
| You have consistent IDs and a fixed reporting date. | Duplicate IDs contain conflicting records or reporting scope is unknown. |

**Authoritative references**

- https://support.microsoft.com/en-us/excel/create-and-share-a-dashboard-with-excel-and-microsoft-groups

---


### Lab 1 · Excel to Word — Prepare Work Orders and Draft the Operations Brief

Learning outcome: LO1: integrate verified Word, Excel, PowerPoint and Outlook outputs.

Goal: You are the maintenance coordinator at Northstar Water Services, a fictional water-pipe maintenance company. Clean a messy work-order export with Copilot in Excel, add check formulas, then turn the clean data into a one-page Word brief.

You are the maintenance coordinator at Northstar Water Services, a fictional water-pipe maintenance company. Clean a messy work-order export with Copilot in Excel, add check formulas, then turn the clean data into a one-page Word brief.

**What you'll build**

A clean Northstar_Work_Orders.xlsx (120 rows and a Checks sheet) and Northstar_Operations_Brief.docx.   (Tools: Microsoft 365 Copilot · Excel · Word · PowerPoint · Outlook.)

**Prerequisites**

- Microsoft 365 account with Copilot available in Word, Excel, PowerPoint and Outlook. Availability depends on the assigned licence and tenant settings; confirm access with the trainer before class.
- Desktop Excel on Windows or Mac. Download this lab folder and open the files straight from its data folder; save any new file in the same folder. All data is fictional.

**Step-by-step**

1. Look at the data. Open data/Northstar_Work_Orders.xlsx in Excel and open Copilot from the Copilot button on the Home tab. Choose Chat only (answers, no changes) and send the prompt. Copilot should find 122 rows, 2 repeated IDs (WO-2026-0005 and WO-2026-0020) and 2 job categories spelt differently.

   ```text
   EXCEL - CHAT ONLY:
   Describe this work-order table for me. How many rows are there? Are there any repeated Work_Order_IDs, or Job_Category names spelt in different ways? Don’t change anything.
   ```

2. Clean the table. Switch to Allow editing and send the prompt. Select Done to keep the change, or Undo to reverse it. The table should now have 120 rows and 5 job categories.

   ```text
   EXCEL - ALLOW EDITING:
   Copy the table to a new sheet named Raw_Export. Then remove the repeated rows, keeping one row for each Work_Order_ID, and fix the Job_Category spelling. Leave empty Assigned_To cells empty.
   ```

3. Add check formulas. Send the prompt and select Done. You should see 120 total, 48 closed, 12 cancelled, 60 backlog, 50 overdue, 6 unassigned, cost S$35,827.50. Save the workbook (Ctrl+S / Cmd+S).

   ```text
   EXCEL - ALLOW EDITING:
   In the Checks sheet, add formulas that count the total work orders, closed, cancelled, backlog (not Closed or Cancelled), overdue backlog (due before the date in Control!B2) and unassigned backlog, and add up Cost_SGD.
   ```

4. Write the brief in Word. Open data/templates/Northstar_Operations_Brief_Template.docx in Word and save it as Northstar_Operations_Brief.docx. In Copilot select + > Upload images and files and choose Northstar_Work_Orders.xlsx from this lab’s data folder, then send the prompt.

   ```text
   WORD COPILOT:
   Write a one-page operations brief in this document from the uploaded Northstar_Work_Orders.xlsx. Include the reporting date, the key numbers from the Checks sheet, the backlog and overdue findings, the unassigned jobs, proposed next actions and open questions. Use only numbers from the workbook, and write UNKNOWN for anything it does not show.
   ```

5. Check the brief. Send the prompt in the same chat and fix any number it lists. Save the brief.

   ```text
   WORD COPILOT:
   Check every number in this brief against the uploaded workbook. List any number that is different, with the correct value.
   ```


**Test it**

| Check | Expected result |
|---|---|
| Clean table | 120 rows, one per Work_Order_ID; 5 job categories. |
| Checks | 120 total, 48 closed, 12 cancelled, 60 backlog, 50 overdue, 6 unassigned, cost S$35,827.50. |
| Word brief | Same numbers as the Checks sheet; empty owners left empty. |

**Troubleshooting**

| If this happens | Fix |
|---|---|
| Copilot cannot see my file | In Excel, save the file and open Copilot again. In Word, PowerPoint or Outlook, upload the file with + > Upload images and files, and upload it again after you change it. |
| A number is different from the lab | Clear any slicers or filters, check the table has no extra rows, then ask again in a new chat. |
| A button or feature is missing | Check you are signed in with your course account and Microsoft 365 is up to date, then tell your trainer. |

**Challenge**

Repeat the task for one different site and explain how the filter scope changes the result. Keep the original verified output.

**Reflection**

Which evidence proves the output is correct, and which decision still needs a person?

> **Note:** The lab folder labs/lab-01-*/ holds the instruction PDF with sample prompts, a data folder with the lab workbook and any templates (data/Northstar_Work_Orders.xlsx). Northstar Water Services is a fictional water-pipe maintenance and service company. All service hubs, staff and work orders are synthetic. Use the fixed reporting date 2026-09-30; missing facts remain UNKNOWN. Proposals do not change real assignments. Training email drafts are never sent.

---

Concepts for Lab 2: Prompts and Verified App Handoffs, Outlook Drafting and Operational Decisions.


### Prompts and Verified App Handoffs

A useful prompt combines the intended goal, operational context, named source and output expectations. The handoff object is a verified artifact, such as a Word brief with a checked metric table and source links. It is not an assumption that another app can remember the preceding conversation. For maintenance, expectations should specify exact dates, status vocabulary, current versus proposed assignments and missing-value behaviour.

The same number may have different meaning when a chart counts all work orders while an email calls it open backlog. A cross-app evidence register records the claim, value, source table, filter scope and date. This provides a small reproducible contract for each output and lets a reviewer identify a mismatch before it becomes a management decision.

**How it works**

- Write the goal and audience.
- Upload the local file or paste the verified source.
- Specify definitions and missing-value behaviour.
- Reconcile the returned claims.

**Worked example**

- Goal: draft a maintenance update for the operations manager.
- Source: reviewed Northstar operations brief, all filters All, 30 September.
- Expectation: label assignment suggestions as proposals and leave unknown approvals UNKNOWN.

**Decision guide**

| Use when | Avoid when |
|---|---|
| A reviewed brief can be selected or its checked text pasted. | Only an unverified summary is available. |

**Authoritative references**

- https://support.microsoft.com/en-gb/word/copilot/draft-and-add-content-with-copilot-in-word
- https://support.microsoft.com/en-us/powerpoint/copilot/add-a-slide-from-a-file-with-copilot-in-powerpoint
- https://support.microsoft.com/en-us/microsoft-365-copilot/file-formats-supported-by-microsoft-365-copilot

---


### Outlook Drafting and Operational Decisions

Copilot can help structure a draft email from supplied context. A synthetic text thread is quoted context, not a live Outlook conversation; the course explicitly uses it that way. The writer remains responsible for recipients, claims, attachments, tone and the distinction between a proposed action and an approved instruction. Saving a draft does not send it or authorise a work-order change.

An apparently routine update can accidentally promise technician reassignment or imply that a manager approved a recovery plan. Current assignment is recorded data; proposed assignment is a separate planning output. Available hours are one input to planning, not evidence of approval or guaranteed productivity. The final email should request the decision rather than claim it has happened.

**How it works**

- Provide the synthetic thread and checked facts.
- Draft a concise update.
- Review recipients, facts and action wording.
- Save the unsent draft and evidence.

**Worked example**

- Current owner blank; proposed owner Aisha remains unapproved.
- A draft addressed to example.invalid is a training artifact.
- The handoff says decision requested, not decision approved.

**Decision guide**

| Use when | Avoid when |
|---|---|
| You can check the evidence and review the draft before use. | The task would imply a real approval or send without review. |

**Authoritative references**

- https://support.microsoft.com/en-us/microsoft-365-copilot/file-formats-supported-by-microsoft-365-copilot

---


### Lab 2 · Word to PowerPoint and Outlook — Create the Cross-App Maintenance Update

Learning outcome: LO1: integrate verified Word, Excel, PowerPoint and Outlook outputs.

Goal: Turn the Northstar operations brief into a 4-slide PowerPoint update and an Outlook email draft, then check that all three show the same numbers.

Turn the Northstar operations brief into a 4-slide PowerPoint update and an Outlook email draft, then check that all three show the same numbers.

**What you'll build**

Northstar_Initial_Update.pptx (4 slides) and an unsent Outlook email draft.   (Tools: Microsoft 365 Copilot · Excel · Word · PowerPoint · Outlook.)

**Prerequisites**

- Microsoft 365 account with Copilot available in Word, Excel, PowerPoint and Outlook. Availability depends on the assigned licence and tenant settings; confirm access with the trainer before class.
- Desktop Excel on Windows or Mac. Download this lab folder and open the files straight from its data folder; save any new file in the same folder. All data is fictional.

**Step-by-step**

1. Read the brief. Open data/Northstar_Operations_Brief.docx in Word, open Copilot and send the prompt. You don’t need to select any text. The table should show 120 total, 60 backlog, 50 overdue and 6 unassigned.

   ```text
   WORD COPILOT:
   Make a short table of the key numbers in this document: date, total, closed, cancelled, backlog, overdue, unassigned backlog and cost. Show it here in the chat and don’t change the document.
   ```

2. Make the slides. Open data/templates/Northstar_Management_Deck_Template.pptx in PowerPoint and save it as Northstar_Initial_Update.pptx. In Copilot select + > Upload images and files and choose Northstar_Operations_Brief.docx from this lab’s data folder, then send the prompt.

   ```text
   POWERPOINT COPILOT:
   Fill these 4 slides from the uploaded Northstar_Operations_Brief.docx: 1 scope and totals, 2 backlog and overdue work, 3 unassigned jobs and proposed actions, 4 the decision needed. Keep the design and use only numbers from the brief.
   ```

3. Check the slides. Send the prompt in the same chat, fix any wrong number on the slides and save.

   ```text
   POWERPOINT COPILOT:
   Check these 4 slides against the uploaded brief. List any number that is wrong and give the correct number.
   ```

4. Draft the email. In Outlook start a new email to operations.manager@example.invalid. Select Copilot > Draft with Copilot, paste the prompt and select Generate. Select Keep it, then close the email without sending it: it stays in your Drafts folder.

   ```text
   OUTLOOK COPILOT:
   Write a short reply to the email below. Use these numbers for 30 September 2026: 120 total, 48 closed, 12 cancelled, 60 backlog, 50 overdue, 6 unassigned, cost S$35,827.50. Say what we found, what we propose next and what decision we need. Say that any new assignment is only a proposal, not approved.
   EMAIL (fictional):
   2026-09-29 09:00 Operations manager: Please prepare the 30 September portfolio snapshot; show open work by site, category and current assignment. 2026-09-29 10:15 Supervisor: Check overdue jobs before proposing reassignment. Available hours are planning inputs, not approval. 2026-09-30 08:30 Analyst: The source export is in the workbook. No new assignment has been approved. Please produce a Word brief and a short PowerPoint update, then prepare a draft reply.
   ```

5. Compare all three. The brief, the slides and the email must show the same numbers. Fix anything that is different.

   ```text
   Total : 120
   Backlog : 60
   Overdue : 50
   Unassigned : 6
   Cost : S$35,827.50
   ```


**Test it**

| Check | Expected result |
|---|---|
| Same numbers | Brief, slides and email all show 120 total, 60 backlog, 50 overdue and 6 unassigned. |
| Draft only | The email stays in Drafts; nothing is approved. |

**Troubleshooting**

| If this happens | Fix |
|---|---|
| Copilot cannot see my file | In Excel, save the file and open Copilot again. In Word, PowerPoint or Outlook, upload the file with + > Upload images and files, and upload it again after you change it. |
| A number is different from the lab | Clear any slicers or filters, check the table has no extra rows, then ask again in a new chat. |
| A button or feature is missing | Check you are signed in with your course account and Microsoft 365 is up to date, then tell your trainer. |

**Challenge**

Repeat the task for one different site and explain how the filter scope changes the result. Keep the original verified output.

**Reflection**

Which evidence proves the output is correct, and which decision still needs a person?

> **Note:** The lab folder labs/lab-02-*/ holds the instruction PDF with sample prompts, a data folder with the lab workbook and any templates (data/Northstar_Work_Orders.xlsx). Northstar Water Services is a fictional water-pipe maintenance and service company. All service hubs, staff and work orders are synthetic. Use the fixed reporting date 2026-09-30; missing facts remain UNKNOWN. Proposals do not change real assignments. Training email drafts are never sent.

---


### Topic 1 Recap - Mapped to Learning Outcomes

Use this recap to explain what you can now do and identify any lab evidence you still need to repair.

| Learning outcome | Evidence from this topic |
|---|---|
| LO1 | Same work-order evidence across four apps. |
| Verify | 120 clean IDs and reconciled brief/update/draft. |

---


## Topic 2 — Personalisation, .Rules and Skills for Excel

Account preferences, workbook conventions and reusable methods

**Key concepts**

- Personalisation — Your account preferences, applied across every workbook.
- .Rules — Visible column-A instructions that travel with the workbook.
- Skills — Reusable methods: built-in @chart-design, or your own SKILL.md such as Pareto and dashboard Skills.

Concepts for Lab 3: Account Personalisation and Specific Requests.


### Account Personalisation and Specific Requests

Excel Copilot Personalisation stores account-level preferences for display, writing style and formula conventions. Saved preferences apply to subsequent prompts across workbooks and devices using that account. They are not stored in or shared with a workbook. A specific task instruction can supersede a preference for that task.

Consistent S$ display and short explanations reduce repetitive requests without changing numeric values. Preferences must not replace the workbook’s business definitions. A private before-state note lets learners restore their previous account settings after the controlled exercise.

**How it works**

- Choose recurring display preferences.
- Save them to the account.
- Compare two workbook outputs.
- Test a specific request and restore.

**Worked example**

- A value of 35827.5 can display as S$35,827.50 or S$35,827.5000.
- Changing a number format does not change its numeric value.
- Another user opening the file does not receive your account preferences.

**Decision guide**

| Use when | Avoid when |
|---|---|
| The preference applies to many reports on your account. | The instruction is a workbook-specific business rule or source change. |

**Authoritative references**

- https://support.microsoft.com/en-us/excel/copilot/copilot-in-excel-personalization

---


### Lab 3 · Personalisation — Personalise Copilot in Excel for Consistent Service Reports

Learning outcome: LO2: distinguish account Personalisation, workbook .Rules and reusable Skills; configure, apply and verify each using water-service evidence..

Goal: Save personal preferences in Copilot, see Excel use them without being asked, change one for a single prompt, then put your settings back.

Save personal preferences in Copilot, see Excel use them without being asked, change one for a single prompt, then put your settings back.

**What you'll build**

A Preference_Check sheet that follows your saved preferences, and your original settings restored.   (Tools: Microsoft 365 Copilot in Excel.)

**Prerequisites**

- Microsoft 365 account with Copilot available in Word, Excel, PowerPoint and Outlook. Availability depends on the assigned licence and tenant settings; confirm access with the trainer before class.
- Desktop Excel on Windows or Mac. Download this lab folder and open the files straight from its data folder; save any new file in the same folder. All data is fictional.

**Step-by-step**

1. Save four preferences. Open data/Northstar_Work_Orders.xlsx in Excel. In Copilot select Settings (...) > Personalization. Write down your current settings so you can put them back later, then add the four preferences below and select Save.

   ```text
   Money : show S$ with two decimals
   Dates : show as DD-MMM-YYYY
   Formulas : use structured references
   Answers : start with a one-line summary
   ```

2. See them work. Select New chat, choose Allow editing and send the prompt. Select Done to keep the change, or Undo to reverse it. The date shows as 30-Sep-2026 and the cost as S$35,827.50, although the prompt did not ask for these formats.

   ```text
   EXCEL - ALLOW EDITING:
   Add a sheet named Preference_Check that shows the reporting date from Control!B2, the number of work orders and the total Cost_SGD, using formulas.
   ```

3. Change a preference once. Send the prompt and select Done. The cost now shows S$35,827.5000: a prompt can override a preference for one task.

   ```text
   EXCEL - ALLOW EDITING:
   Just for this task, show the total cost on Preference_Check with four decimal places. Keep the same formula.
   ```

4. Ask what applies where. Choose Chat only and send the prompt.

   ```text
   EXCEL - CHAT ONLY:
   In this exercise, which settings belong to my account, which belong to this workbook, and which applied to one prompt only? Answer in three short points.
   ```

5. Put your settings back. Select Settings (...) > Personalization, restore the settings you wrote down and select Save.

   ```text
   Excel : Copilot > Settings (...) > Personalization
   Check : your original settings are back
   ```


**Test it**

| Check | Expected result |
|---|---|
| Preferences used | Date 30-Sep-2026 and cost S$35,827.50 without asking in the prompt. |
| One-off change | S$35,827.5000 shown; saved preferences unchanged. |
| Restored | Your original Personalization settings are back. |

**Troubleshooting**

| If this happens | Fix |
|---|---|
| Copilot cannot see my file | In Excel, save the file and open Copilot again. In Word, PowerPoint or Outlook, upload the file with + > Upload images and files, and upload it again after you change it. |
| A number is different from the lab | Clear any slicers or filters, check the table has no extra rows, then ask again in a new chat. |
| A button or feature is missing | Check you are signed in with your course account and Microsoft 365 is up to date, then tell your trainer. |

**Challenge**

Repeat the task for one different site and explain how the filter scope changes the result. Keep the original verified output.

**Reflection**

Which evidence proves the output is correct, and which decision still needs a person?

> **Note:** The lab folder labs/lab-03-*/ holds the instruction PDF with sample prompts, a data folder with the lab workbook and any templates (data/Northstar_Work_Orders.xlsx). Northstar Water Services is a fictional water-pipe maintenance and service company. All service hubs, staff and work orders are synthetic. Use the fixed reporting date 2026-09-30; missing facts remain UNKNOWN. Proposals do not change real assignments. Training email drafts are never sent.

---

Concepts for Lab 4: Visible Workbook .Rules and Formula Results.


### Visible Workbook .Rules and Formula Results

A visible worksheet named exactly .Rules, including the dot, supplies workbook-specific Copilot instructions in column A. Use one idea per cell and English for fully supported behaviour. The sheet travels with a copied workbook. Rules provide guidance for Copilot; they do not enforce formulas, permissions or security controls.

The workbook can carry stable scope, status, cost-display and preservation instructions alongside the source. A formula cell may supply a reporting-date instruction: Copilot reads its recalculated result on the next request. That does not automatically recalculate or update every AI-created output.

**How it works**

- Name the visible sheet exactly .Rules.
- Place one instruction per column-A cell.
- Recalculate a formula-driven rule.
- Check the next output and copied workbook.

**Worked example**

- The date rule returns Reporting date: 2026-09-30 from Control!B2.
- Hidden .Rules is not used; keep the final sheet visible.
- No universal precedence among rules, preferences and Skills is assumed.

**Decision guide**

| Use when | Avoid when |
|---|---|
| Conventions belong to this workbook and should travel with it. | You need a security boundary or are assuming hidden rules apply. |

**Authoritative references**

- https://support.microsoft.com/en-us/excel/copilot/copilot-in-excel-rules
- https://support.microsoft.com/en-us/excel/copilot/copilot-in-excel-personalization
- https://support.microsoft.com/en-us/excel/copilot/copilot-in-excel-skills

---


### Lab 4 · Workbook .Rules — Create and Test Workbook .Rules for Water Service Reporting

Learning outcome: LO2: distinguish account Personalisation, workbook .Rules and reusable Skills; configure, apply and verify each using water-service evidence..

Goal: Give a workbook its own rules with a .Rules sheet, then see Copilot follow them without being told.

Give a workbook its own rules with a .Rules sheet, then see Copilot follow them without being told.

**What you'll build**

A workbook with a visible .Rules sheet and a Rules_Test sheet that follows it.   (Tools: Microsoft 365 Copilot in Excel.)

**Prerequisites**

- Microsoft 365 account with Copilot available in Word, Excel, PowerPoint and Outlook. Availability depends on the assigned licence and tenant settings; confirm access with the trainer before class.
- Desktop Excel on Windows or Mac. Download this lab folder and open the files straight from its data folder; save any new file in the same folder. All data is fictional.

**Step-by-step**

1. Add the rules sheet. Open data/Northstar_Work_Orders.xlsx in Excel. In Copilot choose Allow editing, send the prompt and select Done. A sheet named .Rules appears as the last tab, with one rule in each cell of column A.

   ```text
   EXCEL - ALLOW EDITING:
   Add a visible worksheet named exactly .Rules (with the leading dot) as the last tab; if it exists, clear column A and reuse it. Fill column A only, one cell per line below, entering only the text after each "A#: " label. Do not change any other sheet.
   A1: ## SOURCE AND SCOPE
   A2: Preserve Work_Orders, tblWorkOrders, Technicians, current Assigned_To values and source IDs.
   A3: Use the reporting date from Control!B2. State the selected Site, Job_Category, Status and Assigned_To scope beside every report.
   A4: Backlog excludes Closed and Cancelled. Overdue backlog has Due_Date strictly before Control!B2.
   A5: On-time closure rate uses Closed rows only, with Closed_Date <= Due_Date. Display N/A when no Closed rows remain.
   A6: ## FORMATS AND VISUALS
   A7: Display recorded Cost_SGD as S$ with two decimals; keep underlying values exact. Show dates as DD-MMM-YYYY.
   A8: Use white backgrounds, navy titles, blue and teal accents, readable labels and named units; never use colour alone.
   A9: ## DASHBOARD LAYOUT
   A10: Dashboard sheet: title in A1; Site, Job_Category, Status and Assigned_To dropdowns in B2:B5 (All plus source values); the six measures in B7:B12; data-as-at date and selected scope in D2.
   A11: Six KPI tiles in D4:I7, one column per tile: title in row 4, large value in row 5, short definition in row 6 and "Checks: PASS" in row 7.
   A12: Charts in a grid below the tiles: work orders by status and by job category side by side, then a full-width stacked bar by site (overdue backlog, other backlog, Closed, Cancelled).
   A13: Slicers for Site, Job_Category, Status and Assigned_To on the right of the tiles, connected to tblWorkOrders. KPI formulas use SUBTOTAL visibility so slicers and dropdowns both filter every tile and chart.
   A14: Put chart summaries, chart-title formulas and KPI checks on Dashboard_Summaries. Never merge cells. Hide gridlines on Dashboard.
   A15: ## DASHBOARD STYLE
   A16: Tiles: white bold text on solid navy #1F4E79 (totals and rates), blue #2E75B6 (backlog, overdue) or teal #2A9D8F (Closed, cost).
   A17: Every chart title states the finding from a cell formula, e.g. "Changi Workshop has the most overdue backlog (18 of 50)".
   A18: Show data labels on bars; no gridlines; rates as % with one decimal. Each chart total must equal B7.
   A19: ## OUTPUT AND REVIEW
   A20: Use structured table references. Preserve the visible .Rules sheet and unrelated sheets, charts and Prompt_Log.
   A21: Keep current owners separate from unapproved assignment proposals. Missing facts and approvals remain UNKNOWN.
   A22: Ask before replacing named output sheets. Reconcile every count, rate and chart against source rows; do not duplicate outputs on rerun.
   ```

2. Add a date rule yourself. On the .Rules sheet click the first empty cell in column A, type the formula below and press Enter. It shows Reporting date: 2026-09-30.

   ```text
   ="Reporting date: "&TEXT(Control!B2,"yyyy-mm-dd")
   ```

3. Test the rules. Select New chat, choose Allow editing and send the prompt, then select Done. The prompt does not mention formats, but Rules_Test follows the rules: 120 total, 60 backlog, 50 overdue, on-time 30/48 = 62.5%, cost S$35,827.50.

   ```text
   EXCEL - ALLOW EDITING:
   Add a sheet named Rules_Test with the total work orders, backlog, overdue backlog, on-time closure rate and total cost from tblWorkOrders, using formulas.
   ```

4. Check the rules travel with the file. Save, then use File > Save As to save a copy named Northstar_Rules_Copy.xlsx. In the copy choose Chat only and send the prompt: Copilot lists the same rules.

   ```text
   EXCEL - CHAT ONLY:
   What rules does this workbook give you? List them briefly.
   ```


**Test it**

| Check | Expected result |
|---|---|
| .Rules sheet | Named exactly .Rules, visible, one rule per cell in column A. |
| Rules followed | Rules_Test: 120 total, 60 backlog, 50 overdue, 30/48 = 62.5%, S$35,827.50. |
| Copy | The saved copy still has the .Rules sheet. |

**Troubleshooting**

| If this happens | Fix |
|---|---|
| Copilot cannot see my file | In Excel, save the file and open Copilot again. In Word, PowerPoint or Outlook, upload the file with + > Upload images and files, and upload it again after you change it. |
| A number is different from the lab | Clear any slicers or filters, check the table has no extra rows, then ask again in a new chat. |
| A button or feature is missing | Check you are signed in with your course account and Microsoft 365 is up to date, then tell your trainer. |

**Challenge**

Repeat the task for one different site and explain how the filter scope changes the result. Keep the original verified output.

**Reflection**

Which evidence proves the output is correct, and which decision still needs a person?

> **Note:** The lab folder labs/lab-04-*/ holds the instruction PDF with sample prompts, a data folder with the lab workbook and any templates (data/Northstar_Work_Orders.xlsx). Northstar Water Services is a fictional water-pipe maintenance and service company. All service hubs, staff and work orders are synthetic. Use the fixed reporting date 2026-09-30; missing facts remain UNKNOWN. Proposals do not change real assignments. Training email drafts are never sent.

---

Concepts for Lab 5: What Is a Skill? Inside SKILL.md, Built-in and Custom Skills, Pareto Skill: Find the Vital Few Failure Modes.


### What Is a Skill? Inside SKILL.md

A skill is a folder with a SKILL.md file. The file starts with metadata between two --- lines: a name, which must match the folder name, and a description that says when to use the skill. The body below it holds the steps and procedure Copilot follows. The folder can also hold reference files, such as a template, an example or a data list, that the steps point to.

Skills are triggered on demand: Copilot reads a skill only when you call it with @name or your request matches its description, so skills do not crowd every chat. Write a method once, install it once, and it runs the same way in every file. Excel and PowerPoint both use this format.

**How it works**

- Name the skill and describe when to use it.
- Write the steps, rules and checks.
- Add reference files to the folder if needed.
- Install it, then call it with @name.

**Worked example**

- name: water-service-pareto (the same as its folder name).
- description: Use when I ask for a Pareto chart or failure-mode analysis.
- Steps: count, sort high to low, add Cumulative %, list the vital few.

**Decision guide**

| Use when | Avoid when |
|---|---|
| You repeat the same method in many files. | The task is a one-off question a single prompt can answer. |

**Authoritative references**

- https://support.microsoft.com/en-us/excel/copilot/copilot-in-excel-skills
- https://support.microsoft.com/en-us/powerpoint/copilot/copilot-in-powerpoint-skills

---


### Built-in and Custom Skills

Copilot in Excel ships with built-in skills you call with @, such as @chart-design for charts. @chart-design applies the Excel design team’s chart guidance and @theme-design handles workbook formatting. Built-in skills are turned on in Settings (...) > Manage plugins & skills; chart-design sits under Visualization and is off by default. A custom skill is your own SKILL.md for a method Excel does not know, such as the water-service Pareto or dashboard.

Start with a built-in skill when the task is generic, such as making a clear chart. Write a custom skill when the method carries your own rules: which rows count, how ties sort, which outputs may be replaced and which checks must pass. Both are reusable; only the custom one knows Northstar.

**How it works**

- Turn on chart-design under Visualization.
- Call @chart-design for a generic chart.
- Spot the rules it cannot know.
- Write a custom SKILL.md for those rules.

**Worked example**

- @chart-design draws a clean bar chart of work orders by failure mode.
- It does not add the cumulative line or the vital-few list.
- water-service-pareto adds both, the same way every time.

**Decision guide**

| Use when | Avoid when |
|---|---|
| A generic design task or your own repeatable method. | You expect a built-in skill to know your business rules. |

**Authoritative references**

- https://support.microsoft.com/en-us/excel/copilot/copilot-in-excel-built-in-skills
- https://support.microsoft.com/en-us/excel/copilot/copilot-in-excel-skills

---


### Pareto Skill: Find the Vital Few Failure Modes

A Pareto chart sorts categories from highest to lowest count and adds a cumulative-percentage line. Engineers use it to find the vital few failure modes or root-cause categories that account for most of the work, so improvement effort goes where it matters most. Here each Northstar work order records its Failure_Mode.

The water-service-pareto Skill turns the method into reusable instructions: count, sort high to low, add Share % and Cumulative %, chart it and list the categories needed to reach 80%. Counts must reconcile to the source rows. A Pareto shows where work concentrates; the engineer still confirms the root cause on site before acting.

**How it works**

- Choose the table and the column to analyse.
- Count and sort from highest to lowest.
- Add Share % and Cumulative %.
- List the vital few that reach 80%.

**Worked example**

- All 120 work orders: Corrosion 42, Joint seal leak 30, Valve seat wear 22.
- These 3 of 8 failure modes cause 78% of the work.
- Overdue jobs only: Joint seal leak moves to the top (14 of 50).

**Decision guide**

| Use when | Avoid when |
|---|---|
| You need to decide which failure modes to tackle first. | A count is treated as a proven cause without checking on site. |

**Authoritative references**

- https://support.microsoft.com/en-us/excel/copilot/copilot-in-excel-skills

---


### Lab 5 · Custom Pareto Chart Skill — Find the Vital Few Failure Modes with a Pareto Skill

Learning outcome: LO2: distinguish account Personalisation, workbook .Rules and reusable Skills; configure, apply and verify each using water-service evidence..

Goal: Engineers use Pareto charts to find the vital few failure modes behind most of the work. Make a chart with Excel’s built-in @chart-design skill, then install a custom Pareto skill that sorts failure modes from highest to lowest.

Engineers use Pareto charts to find the vital few failure modes behind most of the work. Make a chart with Excel’s built-in @chart-design skill, then install a custom Pareto skill that sorts failure modes from highest to lowest.

**What you'll build**

A ChartDesign_Demo sheet, a Pareto_Failure_Mode chart for all work orders and one for the overdue jobs.   (Tools: Excel Copilot · Microsoft 365 Copilot web · OneDrive (Skills folder only).)

**Prerequisites**

- Microsoft 365 account with Copilot available in Word, Excel, PowerPoint and Outlook. Availability depends on the assigned licence and tenant settings; confirm access with the trainer before class.
- Desktop Excel on Windows or Mac. Download this lab folder and open the files straight from its data folder; save any new file in the same folder. All data is fictional.

**Step-by-step**

1. Turn on the built-in chart skill. Open data/Northstar_Work_Orders.xlsx in Excel. In Copilot select Settings (...) > Manage plugins & skills and turn on chart-design under Visualization.

   ```text
   Excel : Copilot > Settings (...) > Manage plugins & skills
   Turn on : chart-design (under Visualization)
   ```

2. Use it. Choose Allow editing and send the prompt. Select Done to keep the change, or Undo to reverse it. The bars run from highest to lowest, starting with Corrosion.

   ```text
   EXCEL - ALLOW EDITING:
   @chart-design Make a bar chart of the number of work orders for each Failure_Mode on a new sheet named ChartDesign_Demo, sorted from highest to lowest.
   ```

3. Upload the skill to OneDrive. In Excel open Copilot and select Settings (...) > Manage plugins & skills > Custom skills. Turn Custom skills on and select Add in OneDrive (or Create OneDrive folder, then Open skills folder). OneDrive opens at your skills folder. Select Create or upload > Folder upload and choose the water-service-pareto folder in this lab’s data/templates folder.

   ```text
   OneDrive : Documents > Copilot > Microsoft Excel > skills > water-service-pareto > SKILL.md
   ```

4. Turn the skill on. Back in Excel select Settings (...) > Manage plugins & skills > Custom skills > Refresh, then turn water-service-pareto on. Close the dialog and type @wat in the Copilot prompt box: water-service-pareto should appear. If not, wait a minute and select Refresh again.

   ```text
   Check : water-service-pareto appears when you type @
   ```

5. Find the vital few. Select New chat, choose Allow editing, send the prompt and select Done. You should see Corrosion 42, Joint seal leak 30, Valve seat wear 22, Pump bearing wear 10, Pressure surge 8, Meter fault 4, Blockage 2, Third-party damage 2. The top 3 failure modes cause 78% of all work orders.

   ```text
   EXCEL - ALLOW EDITING:
   @water-service-pareto Make a Pareto chart of Failure_Mode for all work orders in tblWorkOrders.
   ```

6. Look at the overdue jobs. Send the prompt and select Done. Among the 50 overdue jobs the order changes: Joint seal leak 14, Corrosion 13, Valve seat wear 8, Pump bearing wear 7, Pressure surge 3, Blockage 2, Meter fault 2, Third-party damage 1. A Pareto shows where to look first; confirm the root cause on site.

   ```text
   EXCEL - ALLOW EDITING:
   @water-service-pareto Now make the same Pareto chart for the overdue work orders only.
   ```


**Test it**

| Check | Expected result |
|---|---|
| Built-in skill | chart-design turned on; ChartDesign_Demo sorted highest to lowest. |
| All work orders | Corrosion 42, Joint seal leak 30, Valve seat wear 22, Pump bearing wear 10, Pressure surge 8, Meter fault 4, Blockage 2, Third-party damage 2; top 3 = 78%. |
| Overdue only | Joint seal leak 14, Corrosion 13, Valve seat wear 8, Pump bearing wear 7, Pressure surge 3, Blockage 2, Meter fault 2, Third-party damage 1. |

**Troubleshooting**

| If this happens | Fix |
|---|---|
| Copilot cannot see my file | In Excel, save the file and open Copilot again. In Word, PowerPoint or Outlook, upload the file with + > Upload images and files, and upload it again after you change it. |
| A number is different from the lab | Clear any slicers or filters, check the table has no extra rows, then ask again in a new chat. |
| A button or feature is missing | Check you are signed in with your course account and Microsoft 365 is up to date, then tell your trainer. |

**Challenge**

Ask Microsoft 365 Copilot on the web to write your own Pareto SKILL.md and compare it with the supplied one.

**Reflection**

Which evidence proves the output is correct, and which decision still needs a person?

> **Note:** The lab folder labs/lab-05-*/ holds the instruction PDF with sample prompts, a data folder with the lab workbook and any templates (data/Northstar_Work_Orders.xlsx), plus data/templates/water-service-pareto/SKILL.md (Reviewed Pareto Skill fallback). Northstar Water Services is a fictional water-pipe maintenance and service company. All service hubs, staff and work orders are synthetic. Use the fixed reporting date 2026-09-30; missing facts remain UNKNOWN. Proposals do not change real assignments. Training email drafts are never sent.

---

Concepts for Lab 6: Skills, Prompts and Workbook Rules, Custom Skill Discovery in Each App, Repeatability and Safe Skill Reruns, Assignment Proposals and Capacity Evidence.


### Skills, Prompts and Workbook Rules

A prompt is one request. A custom skill is a reusable set of instructions that tells Copilot when and how to perform a recurring task. SKILL.md contains required YAML name and description followed by the instructions. Each skill needs its own folder with a matching name. Workbook-specific rules describe constraints for one workbook; a skill can carry the same maintenance process across repeated reports and supported apps.

The skill makes stable definitions and review boundaries reusable: backlog excludes two terminal statuses, overdue uses a fixed date, missing owners stay missing and output reruns do not duplicate sheets. It does not supply absent work-order data or turn an unsupported app feature into an available one. Skill availability must be verified separately in the app where it will run.

**How it works**

- Identify a recurring task.
- Separate stable rules from current inputs.
- Write name, description and instructions.
- Install, invoke and inspect the result.

**Worked example**

- maintenance-reporting contains definitions and output boundaries.
- Each request still supplies this month’s source, date and scope.
- Native skill use and pasted manual instructions are recorded differently.

**Decision guide**

| Use when | Avoid when |
|---|---|
| The same reporting method recurs and can be tested. | Inputs or desired behaviour are still undefined. |

**Authoritative references**

- https://support.microsoft.com/en-us/excel/copilot/copilot-in-excel-skills
- https://support.microsoft.com/en-us/powerpoint/copilot/copilot-in-powerpoint-skills

---


### Custom Skill Discovery in Each App

Excel uses its Manage plugins & skills interface and an app-created OneDrive skills folder. PowerPoint uses Choose skills and Manage skills with an Add skill/upload route or its own custom skills folder. The app UI resolves the supported folder; a guessed universal path is unreliable. Refresh and enable the skill, then verify the exact name in each app before invoking it by @mention or the menu.

Folder-name/frontmatter mismatches, an extra .txt extension, unavailable licence features and disabled skills can all prevent discovery. A web Copilot authoring conversation can produce the complete Markdown text, but the learner still saves, installs and tests it. Excel cannot log the web chat automatically. Clear installation evidence prevents confusing a manually pasted policy with a native reusable skill.

**How it works**

- Save complete UTF-8 SKILL.md.
- Use the app-created skills location.
- Refresh and verify the matching name.
- Run and record a smoke test.

**Worked example**

- Folder maintenance-reporting matches YAML name maintenance-reporting.
- Excel and PowerPoint both show the skill before native invocation.
- If a menu is absent, manual practice is labelled feature unavailable.

**Decision guide**

| Use when | Avoid when |
|---|---|
| The app exposes its supported skill installation controls. | A missing menu is being treated as successful installation. |

**Authoritative references**

- https://support.microsoft.com/en-us/excel/copilot/copilot-in-excel-skills
- https://support.microsoft.com/en-us/powerpoint/copilot/copilot-in-powerpoint-skills

---


### Repeatability and Safe Skill Reruns

Repeatability means the same verified inputs and method yield equivalent business measures and a controlled output structure. A safe rerun preserves source IDs, statuses, assignments and unrelated sheets. It creates or replaces only explicitly named outputs after review. The concept is similar to idempotence: rerunning should not append duplicate summaries, inflate totals or silently destroy a learner’s unrelated work.

Reporting skills may be used every week or month, so uncontrolled output accumulation quickly creates conflicting summaries. An input guard asks for missing data; a replacement guard identifies the output to change. Test those guards using a copy and compare row count, sums, sheet inventory and output measures before and after, rather than relying on Copilot saying it was careful.

**How it works**

- Capture the source fingerprint and outputs.
- Request a reviewed rerun plan.
- Replace only named output areas.
- Compare source and measures again.

**Worked example**

- 120 source IDs remain 120 after rerunning Maintenance_Summary.
- Missing report date causes a clarification request, not invented numbers.
- A second output sheet is a defect when replacement was requested.

**Decision guide**

| Use when | Avoid when |
|---|---|
| Named output boundaries and reconciliation checks exist. | The skill can overwrite source rows or unrelated sheets. |

**Authoritative references**

- https://support.microsoft.com/en-us/excel/copilot/copilot-in-excel-skills
- https://support.microsoft.com/en-us/powerpoint/copilot/copilot-in-powerpoint-skills

---


### Assignment Proposals and Capacity Evidence

Assignment planning combines the work category, existing owner, estimated hours, technician primary category and available hours. These inputs help generate a proposal; they do not prove complete operational suitability, approved schedules or safety authorisation. Keep Current_Assigned_To separate from Proposed_Assigned_To and use an explicit manager-decision field. Missing evidence is UNKNOWN, not a confident allocation.

The same skill can improve Excel analysis and PowerPoint wording by preserving this boundary. Excel shows category/capacity checks and assumptions in a proposals sheet; PowerPoint explains the findings and requests a decision. A polished visual must not conceal uncertain capacity or make the proposed owner look like the current owner.

**How it works**

- Identify unassigned backlog.
- Compare category and available hours.
- Record the proposal and assumptions.
- Request the manager decision.

**Worked example**

- Unassigned work is counted only within nonterminal statuses.
- Available hours minus proposed effort is a planning check.
- The source Assigned_To stays unchanged until a real authorised operational update.

**Decision guide**

| Use when | Avoid when |
|---|---|
| A manager can review the proposal and missing constraints. | The report claims automatic approval or verified safety qualification. |

**Authoritative references**

- https://support.microsoft.com/en-us/excel/copilot/copilot-in-excel-skills
- https://support.microsoft.com/en-us/powerpoint/copilot/copilot-in-powerpoint-skills

---


### Lab 6 · Reporting Skill — Build a Maintenance Report with Two Skills

Learning outcome: LO2: distinguish account Personalisation, workbook .Rules and reusable Skills; configure, apply and verify each using water-service evidence..

Goal: Install two skills, water-service-pareto and maintenance-reporting, and use them together to build a maintenance report in Excel, then use the reporting skill in PowerPoint.

Install two skills, water-service-pareto and maintenance-reporting, and use them together to build a maintenance report in Excel, then use the reporting skill in PowerPoint.

**What you'll build**

Maintenance_Summary with a failure-mode Pareto, Assignment_Proposals, and an improved Northstar_Initial_Update.pptx.   (Tools: Excel and PowerPoint Copilot · Microsoft 365 Copilot web · OneDrive (Skills folder only).)

**Prerequisites**

- Labs 1–2 verified brief and four-slide update; Lab 5 Skill-authoring method.
- Desktop Excel on Windows or Mac. Download this lab folder and open the files straight from its data folder; save any new file in the same folder. All data is fictional.

**Step-by-step**

1. Upload the skill to OneDrive. In Excel open Copilot and select Settings (...) > Manage plugins & skills > Custom skills. Turn Custom skills on and select Add in OneDrive (or Create OneDrive folder, then Open skills folder). OneDrive opens at your skills folder. Select Create or upload > Folder upload and choose the water-service-pareto and maintenance-reporting folders in this lab’s data/templates folder.

   ```text
   OneDrive : Documents > Copilot > Microsoft Excel > skills > water-service-pareto > SKILL.md
   OneDrive : Documents > Copilot > Microsoft Excel > skills > maintenance-reporting > SKILL.md
   ```

2. Turn the skills on. Back in Excel select Settings (...) > Manage plugins & skills > Custom skills > Refresh, then turn water-service-pareto and maintenance-reporting on. Close the dialog and type @ in the Copilot prompt box: water-service-pareto and maintenance-reporting should appear. If not, wait a minute and select Refresh again.

   ```text
   Check : water-service-pareto appears when you type @
   Check : maintenance-reporting appears when you type @
   ```

3. Build the summary. Open data/Northstar_Work_Orders.xlsx, select New chat, choose Allow editing and send the prompt. Select Done to keep the change, or Undo to reverse it. You should see 120 total, 48 closed, 12 cancelled, 60 backlog, 50 overdue, on-time 30/48 = 62.5% and cost S$35,827.50.

   ```text
   EXCEL - ALLOW EDITING:
   @maintenance-reporting Build a Maintenance_Summary sheet for 30 September 2026 with the total, closed, cancelled, backlog, overdue, on-time closure rate and cost.
   ```

4. Add the failure-mode Pareto. Send the prompt and select Done. The chart is sorted from highest to lowest: Corrosion 42, Joint seal leak 30, Valve seat wear 22, Pump bearing wear 10, Pressure surge 8, Meter fault 4, Blockage 2, Third-party damage 2.

   ```text
   EXCEL - ALLOW EDITING:
   @water-service-pareto Make a Pareto chart of Failure_Mode for all work orders and place it on the Maintenance_Summary sheet, to the right of the numbers.
   ```

5. Suggest owners. Send the prompt and select Done. Assignment_Proposals lists 6 jobs, each marked as a proposal, and Assigned_To on Work_Orders is unchanged. Save the workbook.

   ```text
   EXCEL - ALLOW EDITING:
   @maintenance-reporting Add an Assignment_Proposals sheet for the backlog jobs with no owner. Suggest an owner from tblTechnicians with the same job category and free hours, and mark each one as a proposal. Don’t change Assigned_To.
   ```

6. Use the skill in PowerPoint. Open data/Northstar_Initial_Update.pptx. In Copilot select + > Choose skills > Manage skills > Add skill and upload data/templates/maintenance-reporting/SKILL.md, then send the prompt. Every number must stay the same.

   ```text
   POWERPOINT COPILOT:
   @maintenance-reporting Improve these 4 slides with clearer headlines and less text. Keep every number and keep 4 slides.
   ```


**Test it**

| Check | Expected result |
|---|---|
| Summary | 120 total; 60 backlog; 50 overdue; 30/48 = 62.5%; S$35,827.50. |
| Pareto | Corrosion 42, Joint seal leak 30, Valve seat wear 22, Pump bearing wear 10, Pressure surge 8, Meter fault 4, Blockage 2, Third-party damage 2. |
| Proposals | 6 proposals; Assigned_To unchanged. |
| PowerPoint | 4 slides, same numbers, clearer headlines. |

**Troubleshooting**

| If this happens | Fix |
|---|---|
| Copilot cannot see my file | In Excel, save the file and open Copilot again. In Word, PowerPoint or Outlook, upload the file with + > Upload images and files, and upload it again after you change it. |
| A number is different from the lab | Clear any slicers or filters, check the table has no extra rows, then ask again in a new chat. |
| A button or feature is missing | Check you are signed in with your course account and Microsoft 365 is up to date, then tell your trainer. |

**Challenge**

Open a new blank workbook and ask @maintenance-reporting for last month’s report: a good skill asks for the data instead of inventing numbers.

**Reflection**

Which evidence proves the output is correct, and which decision still needs a person?

> **Note:** The lab folder labs/lab-06-*/ holds the instruction PDF with sample prompts, a data folder with the lab workbook and any templates (data/Northstar_Work_Orders.xlsx), plus data/templates/maintenance-reporting/SKILL.md (Reviewed reporting Skill fallback). Northstar Water Services is a fictional water-pipe maintenance and service company. All service hubs, staff and work orders are synthetic. Use the fixed reporting date 2026-09-30; missing facts remain UNKNOWN. Proposals do not change real assignments. Training email drafts are never sent.

---

Concepts for Lab 7: PowerPoint Design Skill: From Plain to Professional.


### PowerPoint Design Skill: From Plain to Professional

A design skill holds your brand rules, fonts, colours, header bar, footer, KPI cards and spacing, as steps Copilot in PowerPoint follows. Called on a plain deck, it redesigns every slide the same way while keeping every slide, number and fact.

Most decks start plain: black text, no header, no branding. Restyling slide by slide is slow and inconsistent. A design skill makes a professional look one prompt away and the same for every deck the team produces.

**How it works**

- Write the brand rules as a SKILL.md.
- Add it with + > Choose skills > Manage skills > Add skill.
- Call it on a plain deck.
- Check every number is unchanged.

**Worked example**

- Title slide: navy background, white title, teal subtitle.
- Content slides: navy header bar, KPI cards, footer with slide number.
- Numbers such as 120 work orders and 50 overdue stay the same.

**Decision guide**

| Use when | Avoid when |
|---|---|
| Many decks need the same professional look. | The skill is allowed to change numbers or add facts. |

**Authoritative references**

- https://support.microsoft.com/en-us/powerpoint/copilot/copilot-in-powerpoint-skills

---


### Lab 7 · PowerPoint Design Skill — Create a PowerPoint Design Skill: From Plain to Professional

Learning outcome: LO2: create and improve a reusable maintenance skill in Excel and PowerPoint.

Goal: Northstar_Professional_Update.pptx, redesigned by your own northstar-deck-design skill.

Turn a plain, unbranded PowerPoint deck into a professional Northstar deck by creating a design skill once and calling it with @.

**What you'll build**

Northstar_Professional_Update.pptx, redesigned by your own northstar-deck-design skill.   (Tools: Microsoft 365 Copilot · PowerPoint · Microsoft 365 Copilot web.)

**Prerequisites**

- Microsoft 365 account with Copilot available in Word, Excel, PowerPoint and Outlook. Availability depends on the assigned licence and tenant settings; confirm access with the trainer before class.
- Desktop Excel on Windows or Mac. Download this lab folder and open the files straight from its data folder; save any new file in the same folder. All data is fictional.

**Step-by-step**

1. Look at the plain deck. Open data/Northstar_Plain_Update.pptx in PowerPoint and save it as Northstar_Professional_Update.pptx. The numbers are right, but the slides are plain: black text, no header, no branding.

   ```text
   Slides : 6
   Look : plain black text, no colours, no header, no footer
   ```

2. Write the skill. Go to https://copilot.cloud.microsoft, start a new chat, paste the prompt and send it. Read the reply: it starts with --- and the name northstar-deck-design. Copy the whole reply.

   ```text
   MICROSOFT 365 COPILOT WEB:
   Write a complete SKILL.md for a Copilot in PowerPoint skill named northstar-deck-design. Start with --- front matter: name: northstar-deck-design and description: Use when I ask to make a presentation look professional or apply the Northstar brand. Then write numbered steps: 1) Keep every slide, number and fact; change only the design. 2) Fonts: Segoe UI Semibold for titles, Segoe UI for body text. 3) Colours: navy #1F4E79, blue #2E75B6, teal #2A9D8F, light grey #F2F4F7 cards, white background. 4) Slide 1: navy background, large white title, teal subtitle. 5) Every other slide: a navy header bar with a white title and a thin teal line under it. 6) Turn key numbers into KPI cards with a big bold number and a short label. 7) At most 4 short bullets per slide, with plenty of white space. 8) A footer on every slide except slide 1: Northstar Water Services | 30 September 2026, and the slide number. 9) Check every slide and list anything you could not fix. Return only the SKILL.md text, starting with ---, without code fences.
   ```

3. Add the skill to PowerPoint. In PowerPoint open Copilot and select + > Choose skills > Manage skills > Add skill. Paste the reply into the form and select Add. Short of time? Open data/templates/northstar-deck-design/SKILL.md in Notepad or TextEdit, copy all of it and paste that instead.

   ```text
   Check : northstar-deck-design appears when you type @nor
   ```

4. Transform the deck. Send the prompt and watch every slide change: a navy title slide, a header bar on each slide, KPI cards for the numbers and a footer.

   ```text
   POWERPOINT COPILOT:
   @northstar-deck-design Redesign this whole deck in the Northstar style. Keep every slide and every number.
   ```

5. Check the result. Send the prompt and fix anything it lists. The numbers must not change: 120 total, 60 backlog, 50 overdue and 6 unassigned, cost S$35,827.50. Save the deck.

   ```text
   POWERPOINT COPILOT:
   @northstar-deck-design Check every slide against the skill. List any slide missing the header bar, footer, Northstar fonts or colours, and fix it. Do not change any number.
   ```


**Test it**

| Check | Expected result |
|---|---|
| Skill | northstar-deck-design added in PowerPoint and called with @. |
| Design | Navy title slide; header bar, KPI cards and footer on the other slides; Segoe UI fonts. |
| Facts unchanged | 6 slides; 120 total, 60 backlog, 50 overdue and 6 unassigned; S$35,827.50. |

**Troubleshooting**

| If this happens | Fix |
|---|---|
| Copilot cannot see my file | In Excel, save the file and open Copilot again. In Word, PowerPoint or Outlook, upload the file with + > Upload images and files, and upload it again after you change it. |
| A number is different from the lab | Clear any slicers or filters, check the table has no extra rows, then ask again in a new chat. |
| A button or feature is missing | Check you are signed in with your course account and Microsoft 365 is up to date, then tell your trainer. |

**Challenge**

Add a reference file such as brand-colours.md to the skill folder in OneDrive, mention it in SKILL.md, and apply the skill to a plain deck of your own.

**Reflection**

Which evidence proves the output is correct, and which decision still needs a person?

> **Note:** The lab folder labs/lab-07-*/ holds the instruction PDF with sample prompts, a data folder with the lab workbook and any templates (data/Northstar_Plain_Update.pptx). Northstar Water Services is a fictional water-pipe maintenance and service company. All service hubs, staff and work orders are synthetic. Use the fixed reporting date 2026-09-30; missing facts remain UNKNOWN. Proposals do not change real assignments. Training email drafts are never sent.

---


### Topic 2 Recap - Mapped to Learning Outcomes

Use this recap to explain what you can now do and identify any lab evidence you still need to repair.

| Learning outcome | Evidence from this topic |
|---|---|
| LO2 | Personalisation, .Rules, built-in @chart-design, Pareto and reporting Skills tested. |
| Verify | Preserved source plus missing-input and rerun tests. |

---


## Topic 3 — Interactive Dashboards with Custom Skills

Create the Skill, build the dashboard and prove interactions

**Key concepts**

- Measures — Six formula KPIs with clear denominators and N/A rules.
- Visual design — KPI tiles and charts whose titles state the finding.
- Interactions — Dropdowns and slicers filter every tile and chart.
- Refresh — Known deltas in an isolated test copy.

Concepts for Lab 8: Custom Dashboard Skill as a Reusable Contract, Dashboard Measures and Denominators, Visual Dashboard Design for Maintenance.


### Custom Dashboard Skill as a Reusable Contract

water-service-dashboard is a separate custom Skill whose instructions define inputs, six KPI formulas, four shared filter selectors, three editable charts and controlled output boundaries. Visible .Rules carries workbook conventions. The request still supplies the actual source, fixed date and chosen scope. Installing another reporting Skill does not install this dashboard method.

A reusable contract makes every KPI and chart obey the same AND filter logic and allows a safe refresh using table references. Input and replacement guards protect the source and existing Pareto evidence. Rerun evidence includes sheet/chart inventory and source checks, not just a claim that the Skill ran successfully.

**How it works**

- Author and review the complete SKILL.md.
- Install and verify the dashboard name.
- Invoke a plan and build the reviewed output.
- Test common filters, append refresh and reruns.

**Worked example**

- Dashboard B2:B5 select site, category, status and owner.
- B7:B12 and all chart summaries use the identical selected rows.
- A 122-row sandbox is separate from the untouched 120-row baseline.

**Decision guide**

| Use when | Avoid when |
|---|---|
| A recurring dashboard needs consistent measures and review guards. | Tenant Skill access or source preservation is being assumed. |

**Authoritative references**

- https://support.microsoft.com/en-us/excel/copilot/copilot-in-excel-skills
- https://support.microsoft.com/en-us/excel/create-and-share-a-dashboard-with-excel-and-microsoft-groups

---


### Dashboard Measures and Denominators

A dashboard measure needs a business definition, numerator, denominator where relevant, date rule and filter scope. Total orders describes the selected portfolio. Backlog is the selected nonterminal work. Overdue is a subset of backlog. On-time closure rate describes Closed rows only: closed on or before their due date divided by Closed rows. Recorded cost sums selected Cost_SGD; it is not a budget variance or inferred savings.

Changing the denominator can make an attractive rate meaningless. If the selected data contains no Closed rows, the on-time rate is N/A because it is undefined; a displayed 0% would falsely suggest failed delivery. A Measures dictionary and independent control sheet make the definitions inspectable. A fixed reporting date gives reproducible comparisons, while TODAY would change the snapshot over time.

**How it works**

- Define source fields and scope.
- Compute count and denominator.
- Handle empty selections explicitly.
- Reconcile against controls.

**Worked example**

- Closed-only rate is different from closed/total completion share.
- A due-today backlog item is not overdue under a strict before-date rule.
- All selected status/chart counts reconcile to total selected work orders.

**Decision guide**

| Use when | Avoid when |
|---|---|
| Measures have agreed definitions and evidence. | A zero denominator is being represented as a measured 0%. |

**Authoritative references**

- https://support.microsoft.com/en-us/excel/create-and-share-a-dashboard-with-excel-and-microsoft-groups

---


### Visual Dashboard Design for Maintenance

A dashboard should make an operational decision easier. KPI cards summarise magnitude; bar charts compare sites, categories or status counts. Labels, units and source/date context define what each visual means. Site backlog and total orders by site answer different questions and must have different names. Use a line chart for a genuine ordered time series, not unordered site names.

Consistent chart scales, short labels, whitespace and limited accents help a manager compare the work queue quickly. Colour alone is insufficient to distinguish statuses. A category count is evidence of frequency, not a causal diagnosis; a busy site is not necessarily performing badly. Choose the visual based on the question and include the limitation that prevents overinterpretation.

**How it works**

- Name the maintenance decision.
- Choose the measure and comparison.
- Use an appropriate labelled chart.
- Check meaning and readability.

**Worked example**

- Status count chart shows the portfolio mix.
- Site backlog chart excludes Closed and Cancelled.
- A category count does not establish the root cause of overdue jobs.

**Decision guide**

| Use when | Avoid when |
|---|---|
| The visual has a clear audience and question. | Decorative charts hide an ambiguous metric. |

**Authoritative references**

- https://support.microsoft.com/en-us/excel/create-and-share-a-dashboard-with-excel-and-microsoft-groups

---


### Lab 8 · Custom Dashboard Skill — Build an Interactive Dashboard with a Custom Skill

Learning outcome: LO3: build and validate an interactive Excel maintenance dashboard.

Goal: Install the water-service-dashboard skill and use it to build an interactive dashboard.

Install the water-service-dashboard skill and use it to build an interactive dashboard.

**What you'll build**

Northstar_Dashboard.xlsx with six KPI tiles, three charts and slicers.   (Tools: Excel Copilot · Microsoft 365 Copilot web · OneDrive (Skills folder only).)

**Prerequisites**

- Microsoft 365 account with Copilot available in Word, Excel, PowerPoint and Outlook. Availability depends on the assigned licence and tenant settings; confirm access with the trainer before class.
- Desktop Excel on Windows or Mac. Download this lab folder and open the files straight from its data folder; save any new file in the same folder. All data is fictional.

**Step-by-step**

1. Upload the skill to OneDrive. In Excel open Copilot and select Settings (...) > Manage plugins & skills > Custom skills. Turn Custom skills on and select Add in OneDrive (or Create OneDrive folder, then Open skills folder). OneDrive opens at your skills folder. Select Create or upload > Folder upload and choose the water-service-dashboard folder in this lab’s data/templates folder.

   ```text
   OneDrive : Documents > Copilot > Microsoft Excel > skills > water-service-dashboard > SKILL.md
   ```

2. Turn the skill on. Back in Excel select Settings (...) > Manage plugins & skills > Custom skills > Refresh, then turn water-service-dashboard on. Close the dialog and type @wat in the Copilot prompt box: water-service-dashboard should appear. If not, wait a minute and select Refresh again.

   ```text
   Check : water-service-dashboard appears when you type @
   ```

3. Plan the dashboard. Open data/templates/Northstar_Dashboard_Starter.xlsx and save it as Northstar_Dashboard.xlsx. Select New chat, choose Plan and send the prompt. Read Copilot’s plan.

   ```text
   EXCEL - PLAN:
   @water-service-dashboard Plan a dashboard for tblWorkOrders with six KPI tiles, three charts (by status, by job category and by site) and slicers. Don’t change anything yet.
   ```

4. Build it. Choose Allow editing, send the prompt and select Done. The tiles should show 120 total, 60 backlog, 50 overdue, 48 closed, on-time 62.5% and cost S$35,827.50.

   ```text
   EXCEL - ALLOW EDITING:
   @water-service-dashboard Build the dashboard you planned, with formulas that read tblWorkOrders. Don’t change the data.
   ```

5. Polish the charts. Send the prompt. Select Done to keep the change, or Undo to reverse it. Each chart title now states a finding.

   ```text
   EXCEL - ALLOW EDITING:
   @chart-design Improve the three dashboard charts with finding-style titles and data labels. Don’t change any values.
   ```

6. Check the numbers. Choose Chat only and send the prompt. Replace any typed-in number it finds with a formula, then save.

   ```text
   EXCEL - CHAT ONLY:
   Check every KPI tile and chart on the Dashboard against tblWorkOrders. List any number that is typed in instead of calculated, and any total that does not match.
   ```


**Test it**

| Check | Expected result |
|---|---|
| Tiles | 120; 60; 50; 48; 62.5%; S$35,827.50. |
| Charts | Status, category and site charts each add up to 120; titles state a finding. |
| Formulas | No typed-in numbers; the source data is unchanged. |

**Troubleshooting**

| If this happens | Fix |
|---|---|
| Copilot cannot see my file | In Excel, save the file and open Copilot again. In Word, PowerPoint or Outlook, upload the file with + > Upload images and files, and upload it again after you change it. |
| A number is different from the lab | Clear any slicers or filters, check the table has no extra rows, then ask again in a new chat. |
| A button or feature is missing | Check you are signed in with your course account and Microsoft 365 is up to date, then tell your trainer. |

**Challenge**

Ask Microsoft 365 Copilot on the web to write your own dashboard SKILL.md and compare it with the supplied one.

**Reflection**

Which evidence proves the output is correct, and which decision still needs a person?

> **Note:** The lab folder labs/lab-08-*/ holds the instruction PDF with sample prompts, a data folder with the lab workbook and any templates (data/Northstar_Work_Orders.xlsx), plus data/templates/water-service-dashboard/SKILL.md (Reviewed interactive dashboard Skill fallback). Northstar Water Services is a fictional water-pipe maintenance and service company. All service hubs, staff and work orders are synthetic. Use the fixed reporting date 2026-09-30; missing facts remain UNKNOWN. Proposals do not change real assignments. Training email drafts are never sent.

---

Concepts for Lab 9: One Filter Scope for Every Visual, Refresh Tests and Static Snapshots.


### One Filter Scope for Every Visual

Interactive means a learner-controlled selection changes the evidence shown. This dashboard has two controls that work together: four dropdowns in B2:B5 and four table slicers. All bypasses one dimension only; selections combine with AND. Every KPI tile and chart summary multiplies the dropdown mask by SUBTOTAL row visibility, so a slicer that hides source rows changes every measure too.

A dashboard can appear interactive while only one chart changes. Test a single-site selection with the dropdown and with the slicer, a combined category/owner selection and an empty selection. Check the scope line and the D3 slicer banner, and compare every chart total with the selected total.

**How it works**

- Define the selector cells.
- Apply the same AND mask everywhere.
- Test each control and edge case.
- Reconcile selected chart and KPI totals.

**Worked example**

- Woodlands Hub in B2 or in the Site slicer gives 24 work orders.
- Status New gives zero Closed and an N/A closure rate.
- D3 warns while any slicer hides source rows.

**Decision guide**

| Use when | Avoid when |
|---|---|
| All output calculations follow the same scope. | A selector only changes a decorative title or one chart. |

**Authoritative references**

- https://support.microsoft.com/en-us/excel/get-started/use-slicers-to-filter-data
- https://support.microsoft.com/en-us/excel/create-and-share-a-dashboard-with-excel-and-microsoft-groups

---


### Refresh Tests and Static Snapshots

A refresh test deliberately introduces known new records and verifies the expected delta. Table references should expand when rows are appended; PivotTables additionally need a refresh and valid source extent. The course adds two rows in a sandbox copy so the live baseline remains 120 rows. A Word/PDF/PowerPoint snapshot freezes evidence and does not automatically update when the Excel dashboard changes.

A correct dashboard today may fail after the next export if formulas reference a fixed cell range. Known delta testing reveals that failure. Preserving a separate baseline prevents a test record from contaminating the management pack. A snapshot should record source, as-at date, filters and version so its claims remain interpretable after the workbook is refreshed.

**How it works**

- Save an isolated sandbox copy.
- Append known unique test rows.
- Recalculate and verify expected deltas.
- Handoff the untouched baseline.

**Worked example**

- Two test rows increase total by2 and recorded cost byS$400.
- Only one new row adds to backlog/overdue; the other adds to on-time Closed.
- The final deck uses the untouched 120-row baseline, not the test copy.

**Decision guide**

| Use when | Avoid when |
|---|---|
| A predictable change can be checked independently. | Test rows are being mixed into the report without disclosure. |

**Authoritative references**

- https://support.microsoft.com/en-us/excel/create-and-share-a-dashboard-with-excel-and-microsoft-groups

---


### Lab 9 · Interactive Filters and Refresh — Test Dashboard Filters and a Data Refresh

Learning outcome: LO3: build and validate an interactive Excel maintenance dashboard.

Goal: Test a finished dashboard: filter it with slicers, check an empty result, then add two rows and watch every number update.

Test a finished dashboard: filter it with slicers, check an empty result, then add two rows and watch every number update.

**What you'll build**

Northstar_Refresh_Test.xlsx with the dashboard updated to 122 work orders.   (Tools: Excel Copilot · Microsoft 365 Copilot web.)

**Prerequisites**

- Microsoft 365 account with Copilot available in Word, Excel, PowerPoint and Outlook. Availability depends on the assigned licence and tenant settings; confirm access with the trainer before class.
- Desktop Excel on Windows or Mac. Download this lab folder and open the files straight from its data folder; save any new file in the same folder. All data is fictional.

**Step-by-step**

1. Open the dashboard. Open data/Northstar_Work_Orders.xlsx in Excel and go to the Dashboard sheet.

   ```text
   Total : 120
   Backlog : 60
   Overdue : 50
   ```

2. Filter one site. Click Woodlands Hub in the Site slicer and check the tiles. Then select the slicer’s Clear Filter button.

   ```text
   Total : 24
   Backlog : 8
   Overdue : 7
   Closed : 16
   On time : 10 of 16
   Cost : S$6,668.50
   ```

3. Try an empty result. Click New in the Status slicer. The on-time rate shows N/A because no New job is closed. Clear the slicer.

   ```text
   Check : on-time rate shows N/A, not 0%
   ```

4. Add two rows. Use File > Save As to save a copy named Northstar_Refresh_Test.xlsx. Copy the two rows on the Refresh_Test_Rows sheet and paste them in the first empty row under the table on Work_Orders. Go back to the Dashboard.

   ```text
   Total : 122
   Closed : 49
   Backlog : 61
   Overdue : 51
   Cost : S$36,227.50
   ```

5. Ask Copilot to check. Open Copilot, choose Chat only and send the prompt. Then save.

   ```text
   EXCEL - CHAT ONLY:
   Check that every KPI tile and chart on the Dashboard includes the two new work orders, WO-2026-0121 and WO-2026-0122. List any number that did not update.
   ```


**Test it**

| Check | Expected result |
|---|---|
| Slicer | Woodlands Hub: 24 total, 8 backlog, 7 overdue, 16 closed, 10 of 16 on time, S$6,668.50. |
| Empty result | Status New: on-time rate N/A. |
| Refresh | 122 total, 49 closed, 61 backlog, 51 overdue, S$36,227.50. |

**Troubleshooting**

| If this happens | Fix |
|---|---|
| Copilot cannot see my file | In Excel, save the file and open Copilot again. In Word, PowerPoint or Outlook, upload the file with + > Upload images and files, and upload it again after you change it. |
| A number is different from the lab | Clear any slicers or filters, check the table has no extra rows, then ask again in a new chat. |
| A button or feature is missing | Check you are signed in with your course account and Microsoft 365 is up to date, then tell your trainer. |

**Challenge**

Repeat the task for one different site and explain how the filter scope changes the result. Keep the original verified output.

**Reflection**

Which evidence proves the output is correct, and which decision still needs a person?

> **Note:** The lab folder labs/lab-09-*/ holds the instruction PDF with sample prompts, a data folder with the lab workbook and any templates (data/Northstar_Work_Orders.xlsx), plus data/templates/water-service-dashboard/SKILL.md (Reviewed dashboard Skill for reruns). Northstar Water Services is a fictional water-pipe maintenance and service company. All service hubs, staff and work orders are synthetic. Use the fixed reporting date 2026-09-30; missing facts remain UNKNOWN. Proposals do not change real assignments. Training email drafts are never sent.

---


### Topic 3 Recap - Mapped to Learning Outcomes

Use this recap to explain what you can now do and identify any lab evidence you still need to repair.

| Learning outcome | Evidence from this topic |
|---|---|
| LO3 | Six KPI tiles and three charts follow four dropdowns and slicers. |
| Verify | Baseline controls and known refresh deltas. |

---


## Topic 4 — Create a Professional Presentation with PowerPoint Copilot

Continue the dashboard into a decision pack

**Key concepts**

- Evidence story — Observation, implication, action and decision.
- Charts — Reviewed values, provenance and snapshot date.
- Refinement — Hierarchy, notes and actual rehearsal feedback.
- Handoff — Reconciled pack and unsent communication.

Concepts for Lab 10: From Dashboard Evidence to a Decision Story, Charts, Templates and Source Provenance.


### From Dashboard Evidence to a Decision Story

A management presentation transforms evidence into a sequence of observations, implications, proposed actions and a decision request. Each slide needs one defensible headline and a register entry linking the claim to its measure, source, reporting date and filter scope. A chart contains data; the headline interprets it. That interpretation must stay within what the data supports.

Copilot can accelerate outlines and drafting, but a persuasive invented conclusion is still wrong. Before generating the deck, use Word to organise an eight-slide brief with a supporting chart and limitation for each claim. This explicit bridge makes the Excel-to-PowerPoint handoff reliable and avoids assuming a workbook can be used by every presentation-generation mode.

**How it works**

- Freeze the verified dashboard snapshot.
- Register each proposed claim.
- Write a reviewed Word brief.
- Generate and reconcile the deck.

**Worked example**

- Backlog by site supports prioritisation, not a proven cause.
- Available-hours evidence supports a capacity discussion, not confirmed allocation.
- The final slide asks management to decide on a proposed plan.

**Decision guide**

| Use when | Avoid when |
|---|---|
| Every headline has a checked measure and clear scope. | The story introduces savings, causes or approvals absent from evidence. |

**Authoritative references**

- https://support.microsoft.com/en-gb/word/copilot/draft-and-add-content-with-copilot-in-word
- https://support.microsoft.com/en-us/powerpoint/copilot/add-a-slide-from-a-file-with-copilot-in-powerpoint
- https://support.microsoft.com/en-us/microsoft-365-copilot/file-formats-supported-by-microsoft-365-copilot

---


### Charts, Templates and Source Provenance

A template supplies slide layouts, typography and colours; it does not supply correct facts. PowerPoint Copilot can draft slides from selected supported files. Reviewed Word briefs are a reliable narrative input for this course. Excel charts may be embedded for editing or pasted as images; both are copies of a reporting state unless a separate supported link is deliberately configured and tested.

Approximate AI-generated charts can contradict source values while looking plausible. Replace them with reviewed charts or verified tables and keep source/date notes. Distinguish all-work-order counts from backlog-only counts. A professional presentation uses consistent units and chart semantics, not just a consistent palette.

**How it works**

- Upload or paste the reviewed brief.
- Apply the existing template.
- Insert verified charts or tables.
- Record source and snapshot scope.

**Worked example**

- An editable embedded chart remains a copy rather than a tested live link.
- An image is labelled as a snapshot at 30 September.
- All eight slides use one reviewed baseline.

**Decision guide**

| Use when | Avoid when |
|---|---|
| The chart object or image can be verified against the register. | A visual is assumed accurate because Copilot produced it. |

**Authoritative references**

- https://support.microsoft.com/en-us/powerpoint/copilot/add-a-slide-from-a-file-with-copilot-in-powerpoint
- https://support.microsoft.com/en-us/microsoft-365-copilot/file-formats-supported-by-microsoft-365-copilot

---


### Lab 10 · Dashboard to presentation — Turn Dashboard Evidence into a Management Story

Learning outcome: LO4: turn verified dashboard evidence into a professional management presentation.

Goal: Turn the dashboard into a Word presentation brief, then into an 8-slide PowerPoint management deck.

Turn the dashboard into a Word presentation brief, then into an 8-slide PowerPoint management deck.

**What you'll build**

Northstar_Presentation_Brief.docx and an 8-slide Northstar_Management_Draft.pptx.   (Tools: Microsoft 365 Copilot · Excel · Word · PowerPoint · Outlook.)

**Prerequisites**

- Microsoft 365 account with Copilot available in Word, Excel, PowerPoint and Outlook. Availability depends on the assigned licence and tenant settings; confirm access with the trainer before class.
- Desktop Excel on Windows or Mac. Download this lab folder and open the files straight from its data folder; save any new file in the same folder. All data is fictional.

**Step-by-step**

1. Write the presentation brief. Open data/templates/Northstar_Presentation_Brief_Template.docx in Word and save it as Northstar_Presentation_Brief.docx. In Copilot select + > Upload images and files and choose Northstar_Work_Orders.xlsx from this lab’s data folder, then send the prompt. Check the brief shows 120 total, 60 backlog, 50 overdue and 6 unassigned, then save.

   ```text
   WORD COPILOT:
   Use the uploaded Northstar_Work_Orders.xlsx to write a brief for an 8-slide management presentation. For each slide give a headline, the number that supports it and a one-line speaker note. Slides: overview, portfolio, site backlog, status and category mix, overdue and on-time, unassigned jobs, proposed actions, decision needed. Use only numbers from the workbook.
   ```

2. Make the deck. Open data/templates/Northstar_Management_Deck_Template.pptx in PowerPoint and save it as Northstar_Management_Draft.pptx. In Copilot select + > Upload images and files and choose Northstar_Presentation_Brief.docx, then send the prompt.

   ```text
   POWERPOINT COPILOT:
   Fill these 8 slides from the uploaded Northstar_Presentation_Brief.docx, one message per slide. Keep the design, use only numbers from the brief and label actions as proposed.
   ```

3. Add a real chart. In Excel open data/Northstar_Work_Orders.xlsx, go to the Dashboard, right-click the site chart and select Copy. In PowerPoint paste it on the site backlog slide and save.

   ```text
   Copy from : Excel Dashboard, site chart
   Paste to : the site backlog slide
   ```

4. Check the deck. Send the prompt in the same PowerPoint chat, fix any wrong number and save.

   ```text
   POWERPOINT COPILOT:
   Check these 8 slides against the uploaded brief. List any number that is wrong and give the correct number.
   ```


**Test it**

| Check | Expected result |
|---|---|
| Brief | 8 slide plans; 120 total, 60 backlog, 50 overdue and 6 unassigned. |
| Deck | 8 slides; numbers match the brief; actions labelled proposed. |
| Chart | The dashboard site chart is on the site backlog slide. |

**Troubleshooting**

| If this happens | Fix |
|---|---|
| Copilot cannot see my file | In Excel, save the file and open Copilot again. In Word, PowerPoint or Outlook, upload the file with + > Upload images and files, and upload it again after you change it. |
| A number is different from the lab | Clear any slicers or filters, check the table has no extra rows, then ask again in a new chat. |
| A button or feature is missing | Check you are signed in with your course account and Microsoft 365 is up to date, then tell your trainer. |

**Challenge**

Repeat the task for one different site and explain how the filter scope changes the result. Keep the original verified output.

**Reflection**

Which evidence proves the output is correct, and which decision still needs a person?

> **Note:** The lab folder labs/lab-10-*/ holds the instruction PDF with sample prompts, a data folder with the lab workbook and any templates (data/Northstar_Work_Orders.xlsx). Northstar Water Services is a fictional water-pipe maintenance and service company. All service hubs, staff and work orders are synthetic. Use the fixed reporting date 2026-09-30; missing facts remain UNKNOWN. Proposals do not change real assignments. Training email drafts are never sent.

---

Concepts for Lab 11: Professional Refinement and Rehearsal, Reviewed Handoff and Artifact Lifecycle.


### Professional Refinement and Rehearsal

Refinement improves the clarity of the existing evidence without changing its meaning. Claim-led titles, short visible text, readable axes, consistent chart styles and concise speaker notes help an audience understand the maintenance decision. Rehearsal tests whether the audience can identify the reporting scope, the key finding and the decision required. It produces observed feedback, not a fabricated checklist completion.

A well-designed deck can still fail when the speaker’s notes contain different numbers or a proposal is spoken as an approved action. Review notes as part of the evidence pack and inspect the exported PDF at presentation size. Exporting can alter layout or font rendering, so the PDF must be opened and checked rather than assumed identical to the source.

**How it works**

- Audit the draft against evidence.
- Apply reviewed design changes.
- Rehearse and record actual feedback.
- Inspect PPTX and exported PDF.

**Worked example**

- One message per slide; chart labels remain readable.
- A 45-second note explains evidence and limitation.
- Partner feedback leads to one recorded revision.

**Decision guide**

| Use when | Avoid when |
|---|---|
| The message and decision can be understood quickly. | Polish hides an unsupported claim or unreadable chart. |

**Authoritative references**

- https://support.microsoft.com/en-us/powerpoint/copilot/copilot-in-powerpoint-skills

---


### Reviewed Handoff and Artifact Lifecycle

The final pack contains an interactive Excel dashboard, a fixed reporting brief, a static PowerPoint/PDF snapshot, the custom skill and a reviewed communication draft. These artifacts have different lifecycles. The dashboard may refresh; the skill defines a method; the presentation records a dated claim set. Link each file accurately and preserve the evidence register so a later reader knows what was reviewed.

Updating one artifact without the others creates inconsistent communication. Reconcile the final pack and explicitly state that actions remain proposed and the email remains a draft. Versioned source and archived superseded artifacts let the team revisit an earlier report without confusing it with the current one. A missing link is UNKNOWN until an actual accessible link is supplied.

**How it works**

- Reconcile final artifacts.
- Record actual filenames and links.
- Review the handoff draft.
- Preserve the dated snapshot and skill.

**Worked example**

- PowerPoint and PDF both show eight slides/pages from the same baseline.
- Outlook does not claim a missing attachment was sent.
- The next update reruns the method with new verified inputs.

**Decision guide**

| Use when | Avoid when |
|---|---|
| Current versions and review evidence are explicit. | A refreshed dashboard is assumed to rewrite an old presentation. |

**Authoritative references**

- https://support.microsoft.com/en-us/microsoft-365-copilot/file-formats-supported-by-microsoft-365-copilot
- https://support.microsoft.com/en-us/powerpoint/copilot/copilot-in-powerpoint-skills

---


### Lab 11 · Professional handoff — Refine and Present the Maintenance Decision Deck

Learning outcome: LO4: turn verified dashboard evidence into a professional management presentation.

Goal: Polish a management deck, rehearse it, save a PDF and draft the handoff email.

Polish a management deck, rehearse it, save a PDF and draft the handoff email.

**What you'll build**

Northstar_Management_Final.pptx and .pdf, and an unsent handoff email draft.   (Tools: Microsoft 365 Copilot · Excel · Word · PowerPoint · Outlook.)

**Prerequisites**

- Microsoft 365 account with Copilot available in Word, Excel, PowerPoint and Outlook. Availability depends on the assigned licence and tenant settings; confirm access with the trainer before class.
- Desktop Excel on Windows or Mac. Download this lab folder and open the files straight from its data folder; save any new file in the same folder. All data is fictional.

**Step-by-step**

1. Review the deck. Open data/Northstar_Management_Draft.pptx in PowerPoint and save it as Northstar_Management_Final.pptx. Open Copilot, send the prompt and read the list.

   ```text
   POWERPOINT COPILOT:
   Review these 8 slides. List crowded slides, unclear headlines, missing labels and any number without a source. Don’t change anything yet.
   ```

2. Fix it. Send the prompt, check that every number is unchanged, then save.

   ```text
   POWERPOINT COPILOT:
   Fix the problems you listed: clear headlines, less text and readable charts. Add a 45-second speaker note to each slide. Keep every number and keep 8 slides.
   ```

3. Rehearse. Select Slide Show and present to a partner in five minutes (or use Rehearse with Coach). Fix one thing your partner found unclear.

   ```text
   Check : one change made after the rehearsal
   ```

4. Save a PDF. Select File > Export > PDF and save Northstar_Management_Final.pdf. Open the PDF.

   ```text
   Check : 8 pages, every chart and number readable
   ```

5. Draft the handoff email. In Outlook start a new email to operations.manager@example.invalid and attach Northstar_Management_Final.pdf and data/Northstar_Work_Orders.xlsx. Select Copilot > Draft with Copilot, paste the prompt and select Generate. Select Keep it, then close the email without sending it.

   ```text
   OUTLOOK COPILOT:
   Write a short handoff email for the attached Northstar management deck (PDF) and dashboard workbook. Give the 30 September 2026 scope, the key findings (120 total, 60 backlog, 50 overdue and 6 unassigned), the proposed actions and the decision needed. Say the PDF is a snapshot and the workbook is interactive. Don’t say anything is approved.
   ```


**Test it**

| Check | Expected result |
|---|---|
| Deck | 8 slides, same numbers, speaker notes added. |
| PDF | 8 readable pages. |
| Email | Two attachments; stays in Drafts; nothing approved. |

**Troubleshooting**

| If this happens | Fix |
|---|---|
| Copilot cannot see my file | In Excel, save the file and open Copilot again. In Word, PowerPoint or Outlook, upload the file with + > Upload images and files, and upload it again after you change it. |
| A number is different from the lab | Clear any slicers or filters, check the table has no extra rows, then ask again in a new chat. |
| A button or feature is missing | Check you are signed in with your course account and Microsoft 365 is up to date, then tell your trainer. |

**Challenge**

Repeat the task for one different site and explain how the filter scope changes the result. Keep the original verified output.

**Reflection**

Which evidence proves the output is correct, and which decision still needs a person?

> **Note:** The lab folder labs/lab-11-*/ holds the instruction PDF with sample prompts, a data folder with the lab workbook and any templates (data/Northstar_Work_Orders.xlsx). Northstar Water Services is a fictional water-pipe maintenance and service company. All service hubs, staff and work orders are synthetic. Use the fixed reporting date 2026-09-30; missing facts remain UNKNOWN. Proposals do not change real assignments. Training email drafts are never sent.

---


### Topic 4 Recap - Mapped to Learning Outcomes

Use this recap to explain what you can now do and identify any lab evidence you still need to repair.

| Learning outcome | Evidence from this topic |
|---|---|
| LO4 | Eight-slide evidence story and reviewed handoff. |
| Verify | PDF, notes, register and actual rehearsal agree. |

---


## Topic 5 — Copilot Agents and Mini Capstone

Build a work-order agent, then apply the whole workflow in groups

**Key concepts**

- Agent Builder — Create a specialist Copilot agent without code.
- Knowledge — OneDrive files the agent searches and cites.
- Instructions & Skills — Role, rules and a reusable work-order Q&A method.
- Mini capstone — Groups turn safe data into a dashboard and decision deck.

Concepts for Lab 12: What Is Agent Builder?.


### What Is Agent Builder?

Agent Builder is the no-code tool in Microsoft Copilot for creating your own specialist agent. An agent is a focused version of Copilot with its own name, instructions, knowledge, skills, capabilities and starter prompts. You open it from Agents & Skills > New agent, describe the agent in plain English or fill in Configure, test it in Try it, then create and share it.

An agent packages a recurring job, here answering work-order questions, so colleagues get consistent, grounded and bounded answers without rewriting prompts. Its answers are only as good as its instructions and knowledge, and it inherits the same permission and licensing rules as Copilot. Skills in agents are a preview that cannot yet be combined with uploaded files.

**How it works**

- Describe the agent’s job.
- Configure instructions and knowledge.
- Add a Skill and starter prompts.
- Test, create and share safely.

**Worked example**

- Knowledge: the handbook and the clean work-order file from OneDrive.
- Skill: work-order-qa sets definitions, citations and UNKNOWN rules.
- Boundary test: the agent refuses to approve a reassignment.

**Decision guide**

| Use when | Avoid when |
|---|---|
| A recurring question set needs consistent, grounded answers. | The agent would need to change records or act without review. |

**Authoritative references**

- https://learn.microsoft.com/en-us/microsoft-365/copilot/extensibility/agent-builder-build-agents
- https://learn.microsoft.com/en-us/microsoft-365/copilot/extensibility/agent-builder-add-knowledge
- https://learn.microsoft.com/en-us/microsoft-365/copilot/extensibility/declarative-agent-skills

---


### Lab 12 · Copilot Agent Builder — Build a Work-Order Agent with Agent Builder

Learning outcome: LO5: build a grounded Copilot agent and apply the full workflow in a group capstone.

Goal: Build a Copilot agent that answers questions about the Northstar work orders, then test its answers and its limits.

Build a Copilot agent that answers questions about the Northstar work orders, then test its answers and its limits.

**What you'll build**

A private Northstar Work Order Assistant agent with two knowledge files.   (Tools: Microsoft Copilot (copilot.cloud.microsoft) · Agent Builder · OneDrive.)

**Prerequisites**

- Microsoft 365 account with Copilot available in Word, Excel, PowerPoint and Outlook. Availability depends on the assigned licence and tenant settings; confirm access with the trainer before class.
- Desktop Excel on Windows or Mac. Download this lab folder and open the files straight from its data folder; save any new file in the same folder. All data is fictional.
- A Microsoft 365 Copilot licence with Agent Builder turned on by your administrator.

**Step-by-step**

1. Put the knowledge files in OneDrive. An agent can only use files stored in Microsoft 365. In OneDrive create a folder named agent-knowledge and upload the two files from this lab’s data/knowledge folder.

   ```text
   OneDrive : agent-knowledge > Northstar_Service_Handbook.docx and Northstar_Work_Orders_Clean.xlsx
   ```

2. Describe the agent. Go to https://copilot.cloud.microsoft and select Agents > New agent. Paste the prompt into the Describe chat and send it.

   ```text
   AGENT BUILDER - DESCRIBE:
   Create an agent called Northstar Work Order Assistant. It answers questions about Northstar Water Services work orders at 30 September 2026 using only the knowledge files I add. Keep answers short, name the file used, and say UNKNOWN when the files don’t have the answer. Never approve assignments, change records or send messages.
   ```

3. Paste the instructions. Select Configure and replace the Instructions with the prompt below.

   ```text
   AGENT BUILDER - INSTRUCTIONS:
   # Role You are Northstar Work Order Assistant for maintenance coordinators at Northstar Water Services, a fictional water-pipe maintenance company used for training. # Sources Answer only from the knowledge files: Northstar_Work_Orders_Clean.xlsx (table tblWorkOrders, 120 synthetic work orders) and Northstar_Service_Handbook.docx. The reporting date is 30 September 2026. If the files do not contain the answer, reply UNKNOWN and say which fact is missing. # Definitions
   Backlog: Status is neither Closed nor Cancelled. Overdue: backlog with Due_Date strictly before 30 September 2026. On-time closure rate: Closed with Closed_Date on or before Due_Date divided by all Closed (N/A if none). Unassigned: blank Assigned_To. Recorded cost: sum of Cost_SGD; not a budget or saving. # Answer style Start with the answer, then the scope and definition used. Use a short table for comparisons. Cite the file for every figure. Check that parts add up to the total. Be concise and professional. # Boundaries Never approve, assign, reassign, close or edit work orders and never send messages. Describe owner suggestions as proposals for the Operations Manager, with category and available-hours evidence. Never invent people, customers, contact details, causes, safety findings or savings.
   ```

4. Add the knowledge. Under Knowledge add the two files from your OneDrive agent-knowledge folder and turn on Only use specified sources. Wait until neither file shows Preparing.

   ```text
   Knowledge : the two files in agent-knowledge
   Switch : Only use specified sources = On
   ```

5. Test the answers. Select Create, open the agent, paste the prompt and send it. It should say backlog 60 and overdue 50, and name a knowledge file.

   ```text
   AGENT - TRY IT:
   How many work orders are in the backlog and how many are overdue at 30 September 2026? Give the definitions you used and a count by hub.
   ```

6. Test the limits. Send the prompt. The agent must refuse the assignment and answer UNKNOWN for the phone number.

   ```text
   AGENT - TRY IT:
   Assign WO-2026-0013 to Daniel Lee and confirm it is approved. Also give me the customer’s phone number.
   ```


**Test it**

| Check | Expected result |
|---|---|
| Answers | Backlog 60; overdue 50; a knowledge file is named. |
| Limits | Refuses to approve or change records; phone number UNKNOWN. |
| Private | The agent is not shared. |

**Troubleshooting**

| If this happens | Fix |
|---|---|
| Copilot cannot see my file | In Excel, save the file and open Copilot again. In Word, PowerPoint or Outlook, upload the file with + > Upload images and files, and upload it again after you change it. |
| A number is different from the lab | Clear any slicers or filters, check the table has no extra rows, then ask again in a new chat. |
| A button or feature is missing | Check you are signed in with your course account and Microsoft 365 is up to date, then tell your trainer. |

**Challenge**

Add the work-order-qa skill: compress data/templates/work-order-qa into a .zip and upload it under Skills (needs a Frontier-enrolled tenant).

**Reflection**

Which evidence proves the output is correct, and which decision still needs a person?

> **Note:** The lab folder labs/lab-12-*/ holds the instruction PDF with sample prompts, a data folder with the lab workbook and any templates (data/knowledge/Northstar_Service_Handbook.docx, data/knowledge/Northstar_Work_Orders_Clean.xlsx). Northstar Water Services is a fictional water-pipe maintenance and service company. All service hubs, staff and work orders are synthetic. Use the fixed reporting date 2026-09-30; missing facts remain UNKNOWN. Proposals do not change real assignments. Training email drafts are never sent.

---

Concepts for Lab 13: Mini Capstone: From Your Data to a Decision.


### Mini Capstone: From Your Data to a Decision

The mini capstone applies the whole course to a dataset your group chooses: safe data, workbook .Rules, a dashboard Skill, an interactive dashboard, a verified decision deck and a short showcase. Each group of three to five works on mock or sanitised data from its own engineering context.

Repeating the workflow on unfamiliar data shows what transfers: definitions written as rules, reusable skills, independent checks and a decision-focused story. It also tests data control: sanitising or generating data before any of it reaches Copilot.

**How it works**

- Choose safe data and roles.
- Write .Rules and build with a Skill.
- Verify KPIs and slicers.
- Build the deck and showcase.

**Worked example**

- A 150-row synthetic lift-maintenance table replaces real records.
- Six KPI tiles reconcile to independent COUNTIFS.
- A five-slide deck ends with the decision requested.

**Decision guide**

| Use when | Avoid when |
|---|---|
| You can explain every number from your own data. | The dataset contains personal, customer or confidential information. |

**Authoritative references**

- https://support.microsoft.com/en-us/excel/create-and-share-a-dashboard-with-excel-and-microsoft-groups
- https://support.microsoft.com/en-us/excel/copilot/copilot-in-excel-rules
- https://support.microsoft.com/en-us/excel/copilot/copilot-in-excel-skills

---


### Lab 13 · Mini Capstone — Mini Capstone: Group Dashboard and Decision Deck

Learning outcome: LO5: build a grounded Copilot agent and apply the full workflow in a group capstone.

Goal: In groups, build a dashboard and a 5-slide decision deck from your own fictional dataset, then present it in three minutes.

In groups, build a dashboard and a 5-slide decision deck from your own fictional dataset, then present it in three minutes.

**What you'll build**

Per group: a dataset, a .Rules sheet, an interactive dashboard, a 5-slide deck and a three-minute showcase.   (Tools: Excel Copilot · PowerPoint Copilot · Microsoft 365 Copilot web.)

**Prerequisites**

- Microsoft 365 account with Copilot available in Word, Excel, PowerPoint and Outlook. Availability depends on the assigned licence and tenant settings; confirm access with the trainer before class.

**Step-by-step**

1. (5 min) Make a dataset. Form groups of 3-5. Go to https://copilot.cloud.microsoft, paste the prompt (change the domain to your own) and send it.

   ```text
   MICROSOFT 365 COPILOT WEB:
   Create a fictional dataset for an engineering team in [your domain, for example lift maintenance]. Return 150 rows as a table with columns Record_ID, Site, Category, Priority, Status, Owner, Opened_Date, Due_Date, Closed_Date, Hours and Cost_SGD. Use 2026 dates and no real people, companies or places.
   ```

2. (3 min) Put it in Excel. Paste the table into a new workbook, press Ctrl+T and name the table tblData. Add a sheet named Control with your reporting date in B2. Save it as Group_Dashboard.xlsx.

   ```text
   Table : tblData
   Control : reporting date in B2
   File : Group_Dashboard.xlsx
   ```

3. (4 min) Add rules. Open Copilot, choose Allow editing, send the prompt and select Done.

   ```text
   EXCEL - ALLOW EDITING:
   Add a visible sheet named exactly .Rules. In column A, one rule per cell, write rules for this workbook: keep tblData unchanged; use the reporting date in Control!B2; six KPI tiles in row 4; charts below; slicers on the right; navy, blue and teal colours; chart titles that state a finding.
   ```

4. (10 min) Build the dashboard. Install the interactive-dashboard skill from this lab’s data/templates folder: in Copilot select Settings (...) > Manage plugins & skills > Custom skills > Add in OneDrive, upload the folder, then Refresh and turn it on. Send the prompt and select Done.

   ```text
   EXCEL - ALLOW EDITING:
   @interactive-dashboard Build a one-page dashboard for tblData that follows the .Rules: six KPI tiles, three charts and slicers that filter every tile and chart.
   ```

5. (7 min) Make the deck. Open data/templates/Northstar_Management_Deck_Template.pptx (or your own template) in PowerPoint. Open Copilot, paste the prompt, type your dashboard numbers after it and send it.

   ```text
   POWERPOINT COPILOT:
   Using the dashboard numbers below, create a five-slide decision deck: 1 scope and date, 2-3 one finding per slide, 4 proposed actions, 5 the decision needed. No invented causes or savings.
   ```

6. (12 min) Present. Each group has three minutes: the question, the dashboard (click one slicer), the decision slide and one thing Copilot got wrong that you caught.

   ```text
   Time : 3 minutes per group
   ```


**Test it**

| Check | Expected result |
|---|---|
| Safe data | Fictional data only. |
| Dashboard | Tiles and charts follow the slicers. |
| Deck | Numbers match the dashboard; actions labelled proposed. |
| Showcase | Three minutes, one live slicer click. |

**Troubleshooting**

| If this happens | Fix |
|---|---|
| Copilot cannot see my file | In Excel, save the file and open Copilot again. In Word, PowerPoint or Outlook, upload the file with + > Upload images and files, and upload it again after you change it. |
| A number is different from the lab | Clear any slicers or filters, check the table has no extra rows, then ask again in a new chat. |
| A button or feature is missing | Check you are signed in with your course account and Microsoft 365 is up to date, then tell your trainer. |

**Challenge**

Turn your group’s .Rules and dashboard Skill into a reusable pair your team can apply to next month’s data.

**Reflection**

Which evidence proves the output is correct, and which decision still needs a person?

> **Note:** The lab folder labs/lab-13-*/ holds the instruction PDF with sample prompts, a data folder with the lab workbook and any templates (Your own mock or sanitised dataset). Northstar Water Services is a fictional water-pipe maintenance and service company. All service hubs, staff and work orders are synthetic. Use the fixed reporting date 2026-09-30; missing facts remain UNKNOWN. Proposals do not change real assignments. Training email drafts are never sent.

---


### Topic 5 Recap - Mapped to Learning Outcomes

Use this recap to explain what you can now do and identify any lab evidence you still need to repair.

| Learning outcome | Evidence from this topic |
|---|---|
| LO5 | A grounded work-order agent and a group dashboard and decision deck. |
| Verify | Agent answers match Control; capstone figures reconcile to the group data. |

---


## Closing: 5 Principles of AI Security

AI security is the set of habits and controls that keep data, decisions and systems safe when people work with AI assistants and agents. Five principles apply to every Copilot task in this course: data control, permission control, human in the loop, traceability, and using a well-tested model rather than the newest one for important work. Copilot only surfaces data a user can already access and does not use prompts to train its foundation models, but people can still overshare, give an agent too much access, accept an unchecked draft or lose track of what was used. The principles turn those risks into checks you can perform before work leaves your hands.

**Data control**

Share only what the task needs; use synthetic or sanitised data.

**Permission control**

Least privilege for files, agents, skills and sharing.

**Human in the loop**

Plan, review and approve before edits, emails or decisions.

**Traceability**

Log prompts, sources, versions and checks for every output.

**Well-tested models**

Prefer proven, approved models over the newest release.

**Put the principles into practice**

- Share only the data the task needs.
- Limit access for people, agents and skills.
- Review and approve before anything takes effect.
- Log sources, prompts, versions and checks.
- Use synthetic or sanitised data in training and demos.
- An agent gets Can chat access, not Can edit, unless needed.
- A Copilot email stays a draft until a person reviews it.

---


## Next Steps

- First pass: complete every lab yourself, following the steps in each lab file.
- Second pass: redo the labs from memory until the workflow is automatic.
- Apply the techniques to a real process or project in your own organisation.
- Review each lab's detailed steps in this guide and re-run the labs on your own.


## Glossary

- **Agent** — A specialist Copilot with its own instructions, knowledge and skills.
- **Agent Builder** — The Microsoft Copilot tool to describe, configure, test and share an agent.
- **Built-in skill** — A ready-made Copilot skill such as @chart-design, turned on in Manage plugins & skills.
- **Slicer** — A clickable filter connected to a table; here it filters every dashboard tile and chart.
- **Personalisation** — Account-level Copilot preferences; not embedded in a workbook.
- **.Rules** — Visible workbook sheet with column-A instructions for Copilot.
- **Pareto** — Descending contribution counts and cumulative share; not proof of cause.
- **Grounding** — Supplying accessible evidence for the current request.
- **Backlog** — Selected work with Status neither Closed nor Cancelled.
- **Overdue** — Backlog due strictly before the fixed reporting date.
- **Skill** — Reusable instructions in a matching folder and SKILL.md file.
- **Snapshot** — A dated, scoped copy of verified evidence.
- **Structured reference** — A formula reference to a named Excel table or its columns.
- **Denominator** — The population used to calculate a rate.
- **Proposed assignment** — A suggested owner awaiting a real manager decision.
