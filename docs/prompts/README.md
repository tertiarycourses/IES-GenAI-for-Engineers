# GenAI for Engineers - Prompt Library

[Open the prompts page with Copy buttons](https://tertiarycourses.github.io/IES-GenAI-for-Engineers/prompts/)


## Lab 1: Prepare Work Orders and Draft the Operations Brief

[Instruction PDF](../../labs/lab-01-excel-to-word/Lab-01-Instructions.pdf) · [Data folder](../../labs/lab-01-excel-to-word/data/) · [Copy buttons](https://tertiarycourses.github.io/IES-GenAI-for-Engineers/prompts/#lab-1)

### Step 1

Copy data/Northstar_Work_Orders.xlsx to your OneDrive work-genai folder as Northstar_Clean_Work_Orders.xlsx. Open it in Excel, set Formulas > Calculation Options > Automatic, and read About_This_Data and Control. The workbook is the deliberately dirty 122-row input; the checkpoint workbook is a clean reference and must not replace the cleaning exercise. Open Copilot from Home > Copilot.

```text
EXCEL - CHAT ONLY:
Read About_This_Data and Control for Northstar Water Services. Explain what one water-pipe service work order represents, the reporting date, the five job categories and how current owners differ from proposed owners. Do not edit or infer customer impacts.
```

### Step 2

Use Chat only to inspect the named table before making changes. Record row count and the two exact repeated IDs. A Work_Order_ID is the row grain; do not count repeated export records twice.

```text
EXCEL - CHAT ONLY:
Inspect tblWorkOrders. Report row count, duplicate Work_Order_ID values, category spelling variants and missing Assigned_To. Do not edit. Treat 2026-09-30 as the fixed reporting date.
```

### Step 3

Choose Plan if available. Read the proposed cleaning plan before using Allow editing. The duplicates are exact repeated export records: keep one per ID. Trim and standardise category labels to Leak Repair, Valve Repair, Pipe Replacement, Pump Service, Meter Service; preserve missing owners and all unique source values. Save a copy of the raw sheet before the change.

```text
EXCEL - PLAN:
Plan to retain an untouched Raw_Export copy, remove only exact duplicate records by Work_Order_ID, and standardise category spelling in tblWorkOrders. Keep dates, statuses and assignments. Ask if two records with one ID differ.

EXCEL - ALLOW EDITING:
Apply the reviewed plan. Keep one identical record per repeated ID. Do not guess missing owners. Reconcile the cleaned table against Control.
```

### Step 4

Add a Checks sheet or use the supplied one. Ask for formulas, then inspect the table and formulas yourself. Overdue excludes Closed and Cancelled and uses strictly earlier than the fixed date, so a due-today job is not overdue. Record each verified value in the Evidence_Log sheet (claim, value, source, scope and as-at date).

```text
EXCEL - ALLOW EDITING:
In Checks calculate total rows, closed, cancelled, backlog, overdue backlog, unassigned backlog and total Cost_SGD for tblWorkOrders. Use Control!B2 as reporting date. Define backlog as Status neither Closed nor Cancelled. Add the identity total = closed + cancelled + backlog. Do not change source data.
```

### Step 5

Open data/templates/Northstar_Operations_Brief_Template.docx in Word and save as Northstar_Operations_Brief.docx in OneDrive. In Copilot select the verified source file using Reference a file or /. If Word cannot use the workbook, paste your verified evidence table plus the definitions from the Control sheet into the document and select that text; do not imply Word reads the Excel chat.

```text
WORD COPILOT:
Draft a one-page Northstar operations brief from the verified evidence supplied here. Include reporting scope/date, backlog and overdue findings, current assignment issues, proposed next actions and open questions. Keep observed facts separate from proposals. Preserve numbers and definitions. Use UNKNOWN for causes, approvals or capacity decisions not evidenced.
```

### Step 6

Compare every number and work-order ID in the Word brief to Checks and the evidence register. Add the OneDrive source link and all-filters scope. Log the Word prompt manually in Excel Prompt_Log because Excel cannot access the Word conversation. Save the cleaned workbook and brief for Lab 2.

```text
WORD COPILOT:
Audit this Northstar Water Services operations brief against the verified evidence table I supply. Return a discrepancy list for counts, cost, reporting scope, overdue definition and assignment claims. Identify missing source links as UNKNOWN. Do not change facts or approve work.
```


## Lab 2: Create the Cross-App Maintenance Update

[Instruction PDF](../../labs/lab-02-word-to-powerpoint-and-outlook/Lab-02-Instructions.pdf) · [Data folder](../../labs/lab-02-word-to-powerpoint-and-outlook/data/) · [Copy buttons](https://tertiarycourses.github.io/IES-GenAI-for-Engineers/prompts/#lab-2)

### Step 1

Open your Lab 1 Word brief and cleaned workbook. If needed use this lab’s verified checkpoint and snapshot, clearly recording rejoin. Read the synthetic email thread quoted in the Step 4 prompt. It asks for a portfolio update, not authorisation to reassign technicians.

```text
WORD COPILOT:
From this selected verified Northstar Water Services operations brief, extract a handoff table with reporting date, filter scope, total, closed, cancelled, backlog, overdue, unassigned backlog and recorded cost. Separate facts, proposed next actions and open decisions. Keep every value traceable to the supplied brief.
```

### Step 2

Open data/templates/Northstar_Management_Deck_Template.pptx in PowerPoint and save as Northstar_Initial_Update.pptx. For this initial update use four slides by keeping the first four layout slides and deleting the remaining unused template slides. Open Copilot and select your Word brief with Reference a file; if the command is unavailable, paste the reviewed brief into the prompt.

```text
POWERPOINT COPILOT:
Using this verified Northstar Word brief, create a four-slide initial update: scope and portfolio; backlog and overdue work; current assignments and proposed actions; decision required. Use the existing white/navy/blue design. Preserve all verified metrics. Add source/date notes. Do not invent completed work, savings or approved reassignment.
```

### Step 3

Review all four slides. Check status definitions, units and date, and correct any invented claim. Record the reconciliation in the Evidence_Log sheet: one row per claim and a source link. This is the bridge between app outputs; app chats are not automatically shared.

```text
POWERPOINT COPILOT:
Audit these four Northstar Water Services slides against the selected verified operations brief. For each numeric claim give the source, date and scope; flag unsupported service-restoration, safety, customer-impact or approval claims. Propose corrections without changing the checked values.
```

### Step 4

In Outlook create a new training draft addressed to operations.manager@example.invalid with subject DRAFT - Northstar maintenance update - review required. Do not send. Paste the synthetic thread into the draft or use it as quoted context; Copilot summarises the supplied text, not a real mailbox thread. Open Copilot > Draft with Copilot; UI names may differ.

```text
OUTLOOK COPILOT:
Draft a concise reply to the synthetic thread quoted below, using the verified Northstar brief and these checked metrics. State the 30 September 2026 scope, backlog/overdue findings, proposed next actions and the decision requested. Explain that assignments are unapproved proposals. Do not claim the attachments have been sent. Keep as a draft.

THREAD (synthetic, do not send):
2026-09-29 09:00 Operations manager: Please prepare the 30 September portfolio snapshot; show open work by site, category and current assignment.
2026-09-29 10:15 Supervisor: Check overdue jobs before proposing reassignment. Available hours are planning inputs, not approval.
2026-09-30 08:30 Analyst: The source export is in the workbook. No new assignment has been approved. Please produce a Word brief and a short PowerPoint update, then prepare a draft reply.
```

### Step 5

If your Outlook offers reference attachments, attach the verified Word brief and choose it as context. Otherwise paste the reviewed metrics into the drafting prompt. Replace any placeholder summary with exact checked values; inspect recipients, subject, tone and attachment names. Save only the draft and a local TXT copy of its reviewed body.

### Step 6

Ask Word Copilot to compare your pasted slide/email summaries with the brief, then perform the same comparison yourself. Add the cross-app prompt log entries manually. Keep all four source links with the reconciliation record; any mismatch must be fixed before the skill labs.

```text
WORD COPILOT:
Compare these pasted PowerPoint and Outlook summaries with this verified Word brief. List inconsistent figures, status definitions, dates, owner claims or approved-action wording. Do not resolve a conflict by guessing. Return a discrepancy table with source and correction needed.
```


## Lab 3: Personalise Copilot in Excel for Consistent Service Reports

[Instruction PDF](../../labs/lab-03-personalisation/Lab-03-Instructions.pdf) · [Data folder](../../labs/lab-03-personalisation/data/) · [Copy buttons](https://tertiarycourses.github.io/IES-GenAI-for-Engineers/prompts/#lab-3)

### Step 1

Open this lab’s clean data/Northstar_Work_Orders.xlsx and save working copies as Northstar_Personalisation_Test.xlsx and Northstar_Preferences_Copy.xlsx in work-genai. Confirm 120 unique IDs, reporting date 2026-09-30 and cost S$35,827.50. Neither copy needs a .Rules sheet or an installed Skill for this test.

```text
EXCEL - CHAT ONLY:
Inspect tblWorkOrders and Control for Northstar Water Services. State the clean row count, reporting date and recorded cost. Explain why display preferences should not change source values or reporting definitions. Do not edit.
```

### Step 2

In Copilot select Settings (...) > Personalization. Keep your existing settings in a private local note, then temporarily enter these four preferences: Use S$ with two decimal places and thousands separators for currency displays. Display dates as DD-MMM-YYYY. Prefer structured references when writing Excel formulas. Start explanations with a short plain-English summary before the detail. Select Save. Preferences apply to your account on subsequent prompts; they are not stored in or shared with the workbook.

### Step 3

In the first working copy request a small output using your saved preferences. Review the plan before allowing editing. Confirm the date displays 30-Sep-2026 in both copies. Inspect the formulas and number formats in the new Preference_Check sheet; do not accept rounded or rewritten source values.

```text
EXCEL - PLAN:
Plan a Preference_Check sheet showing Control!B2 reporting date, total work orders and recorded Cost_SGD from tblWorkOrders for Northstar Water Services. Use my saved display and explanation preferences. Preserve Work_Orders, IDs, owners and exact values.

EXCEL - ALLOW EDITING:
Apply the reviewed Preference_Check plan with structured-reference formulas. Show a short explanation first and leave the source unchanged.
```

### Step 4

Open the second copy using the same signed-in account and a new Copilot chat. Do not repeat the preference text in this request. Compare both output displays and formula references; record actual behaviour in the Evidence_Log sheet. A missed preference is a finding to clarify, not proof of a guaranteed rule.

```text
EXCEL - ALLOW EDITING:
In this second Northstar workbook, create Preference_Check with formula-backed Control!B2 reporting date, total work orders and recorded Cost_SGD. Follow my saved preferences, preserve source records and explain the result briefly.
```

### Step 5

Return to the first workbook. Test a specific task instruction that changes only the result display to four decimal places. Verify S$35,827.5000 displays while the numeric value remains 35827.5. Record the comparison; do not alter the saved account settings or source.

```text
EXCEL - ALLOW EDITING:
For this task only, display the recorded cost result in Preference_Check with four decimal places. Keep its formula and exact numeric value unchanged. Do not modify source cells or my saved preferences.
```

### Step 6

Explain the scope distinction, log the prompts and your observed checks, then return to Settings (...) > Personalization, restore your previous preferences and Save. Keep the restoration note private; do not upload personal account settings to the shared course folder.

```text
EXCEL - CHAT ONLY:
Explain which choices in this exercise belong to my account, which belong to this Northstar workbook and which apply only to one prompt. Use the results I actually observed. Do not claim my preferences are shared with another person or added to the workbook.
```


## Lab 4: Create and Test Workbook .Rules for Water Service Reporting

[Instruction PDF](../../labs/lab-04-workbook-rules/Lab-04-Instructions.pdf) · [Data folder](../../labs/lab-04-workbook-rules/data/) · [Copy buttons](https://tertiarycourses.github.io/IES-GenAI-for-Engineers/prompts/#lab-4)

### Step 1

Open the clean workbook, save as Northstar_Rules_Workbook.xlsx and inspect Control. In Copilot use Add work content > Create workbook rules if offered; otherwise insert a sheet manually and rename it exactly .Rules, including the leading dot. Keep it visible. Rules are fully supported only in English.

```text
EXCEL - CHAT ONLY:
Inspect this Northstar workbook. Identify the source table, fixed reporting date, status vocabulary and current owners. List workbook-specific conventions that belong in .Rules rather than account Personalisation. Do not edit.
```

### Step 2

Create the .Rules lines with the one-shot Allow editing prompt below (or copy them from the prompts page): one heading or rule per column-A cell; no data in other columns is required for recognition. Check source preservation, backlog/overdue/rate definitions, S$ display, colours, scope and controlled replacements.

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

EXCEL - PLAN:
Review the visible .Rules column A for this Northstar workbook. Identify ambiguous instructions or conflicts with the actual source and Control. Propose concise corrections, keeping one idea per cell. Do not edit the source or invent precedence between rules, preferences and Skills.
```

### Step 3

After reviewing any correction, update only .Rules. Add a formula in the next empty column-A cell: ="Reporting date: "&TEXT(Control!B2,"yyyy-mm-dd"). Recalculate and confirm it displays Reporting date:2026-09-30. Copilot reads the formula result on the next prompt; this does not rewrite dashboard values by itself.

```text
EXCEL - ALLOW EDITING:
Apply only my reviewed .Rules corrections. Keep the sheet visible, one instruction per column-A cell, and retain the reporting-date formula. Preserve source data, Control and unrelated sheets.
```

### Step 4

Request a Rules_Test summary without restating the formatting rules. Check counts against Control, source references, displayed date/scope, S$ units and proposal wording. The known baseline is120 total,60 backlog,50 overdue and 30/48 on-time Closed.

```text
EXCEL - ALLOW EDITING:
Create Rules_Test for Northstar Water Services from tblWorkOrders using the visible workbook .Rules. Include total, backlog, overdue, on-time Closed rate and recorded cost with formula/source evidence. Show date and All scope. Keep source owners and values unchanged.
```

### Step 5

Save As Northstar_Rules_Shared_Copy.xlsx. Open the copy and confirm .Rules is still present and visible in column A; you have not exported your account preferences. If testing a hidden sheet, use only a sandbox copy, hide .Rules, record that hidden rules are not used, then unhide before continuing. Do not claim native rule use when the feature is unavailable.

```text
EXCEL - CHAT ONLY:
In this copied Northstar workbook, identify the visible .Rules instructions and reporting-date formula result. Explain which guidance travels with the workbook and which account preferences do not. Verify Rules_Test against Control without changing records.
```

### Step 6

Record the sheet name, visibility, column, formula result, actual output checks and copied-workbook check in the Evidence_Log sheet. Carry the rules-enabled workbook forward. If a prompt, Skill and rule disagree, ask for clarification and verify the output; no universal precedence is assumed.

```text
EXCEL - CHAT ONLY:
Compare Personalisation, .Rules and a reusable Skill for Northstar reporting. Place currency preferences, this workbook’s backlog/date rules and the repeatable Pareto workflow in the right scope. Identify conflicts requiring clarification and the checks a person still must perform.
```


## Lab 5: Use the Built-in Chart Skill, then Create a Custom Pareto Skill

[Instruction PDF](../../labs/lab-05-custom-pareto-chart-skill/Lab-05-Instructions.pdf) · [Data folder](../../labs/lab-05-custom-pareto-chart-skill/data/) · [Copy buttons](https://tertiarycourses.github.io/IES-GenAI-for-Engineers/prompts/#lab-5)

### Step 1

Open your rules-enabled workbook from Lab 4 or this lab’s clean rules-enabled data/Northstar_Work_Orders.xlsx. Save as Northstar_Pareto.xlsx. Read the expected Pareto controls in Test It and the supplied Skill template before drafting your own file. Work only with synthetic data.

```text
EXCEL - CHAT ONLY:
For tblWorkOrders at Control!B2, All sites, count overdue backlog by Job_Category: Status neither Closed nor Cancelled and Due_Date strictly before the reporting date. Show category counts and total before charting. Preserve all records.
```

### Step 2

Built-in skill first. In Excel Copilot open Settings (...) > Manage plugins & skills. Under Visualization turn on chart-design (it is off by default) and confirm it is enabled. Ask @chart-design for a quick chart of the same overdue counts. Note what the built-in skill gives you (chart design guidance) and what it does not know (your overdue population, tie order, cumulative line and named output) - that is why you build the custom water-service-pareto Skill next. Keep the demo sheet or undo it.

```text
EXCEL - ALLOW EDITING:
@chart-design Chart the overdue backlog by Job_Category from tblWorkOrders at Control!B2 as a bar chart, longest bar first, on a new sheet named ChartDesign_Demo. Use a finding-style title, axis titles and data labels. Do not change source data.
```

### Step 3

In Microsoft 365 Copilot on the web at https://copilot.cloud.microsoft, provide this self-contained specification. Copy the complete response into a plain-text editor and save UTF-8 SKILL.md inside a matching water-service-pareto folder. Compare it to data/templates/water-service-pareto/SKILL.md. If short of time, use the reviewed supplied file and record that choice.

```text
MICROSOFT 365 COPILOT WEB:
Write a complete SKILL.md named water-service-pareto for a recurring water-pipe service report. Require YAML name and description, actual source table, reporting date, scope, count metric and grouping column. Source tblWorkOrders has Work_Order_ID, Job_Category, Site, Status and Due_Date. Overdue backlog excludes Closed/Cancelled and has Due_Date before the supplied date. Read visible workbook .Rules; preserve source IDs/statuses/owners and unrelated sheets. Count by grouping, sort count descending then label alphabetically for ties, and create formula-backed count, cumulative count, share and cumulative percentage. Build an editable combo chart: count columns and cumulative line on a 0%-100% right axis. Output only Pareto_<grouping column>; ask before replacing the matching output, rerun without duplicates, and leave zero-total percentages N/A. Verify counts, stable ties and final 100%; do not infer causes or force 80/20. Return the entire file.
```

### Step 4

In Excel use Copilot Settings (...) > Manage plugins & skills > Custom skills > Create OneDrive folder if needed > Open skills folder. Copy water-service-pareto/SKILL.md into that app-created location, Refresh and enable it. Verify the name using Choose plugins & skills or @mention. If unavailable, paste the complete reviewed Skill before each request, remove @water-service-pareto and record Manual practice - native Skill unavailable. Log web authoring manually.

### Step 5

Request a plan before building. Confirm the eligible total 50 and the five ordered category counts. After review, apply the Skill. Inspect Pareto_Job_Category, formulas, axes and source preservation; copying a static image does not meet the editable-chart goal.

```text
EXCEL - PLAN:
@water-service-pareto Plan an overdue-backlog Pareto Chart by Job_Category from tblWorkOrders at 2026-09-30, All sites. Follow visible .Rules. Explain summary formulas, descending counts, alphabetical ties, cumulative percentages and the named output to create. Do not edit yet.

EXCEL - ALLOW EDITING:
@water-service-pareto Apply the reviewed Job_Category Pareto plan. Create Pareto_Job_Category with a formula-backed summary and editable count-column/cumulative-percent-line combo chart. Keep source data and unrelated sheets unchanged.
```

### Step 6

Check counts against the supplied controls. Verify cumulative percentages 36%,60%,76%,92%,100% and two equal8-count categories in alphabetical order. The first four categories reach at least80%; do not call this proof that20% of categories cause80% of failures. If combo chart UI is absent, select the summary and use Insert > Combo > Custom Combination: Count clustered column, Cumulative_Percent line on secondary axis, right bounds 0 and 1; label both axes. Record a missing feature honestly.

```text
EXCEL - CHAT ONLY:
Verify Pareto_Job_Category against eligible source rows. Check total 50, descending counts, alphabetical tie order, cumulative percentages 36/60/76/92/100%, final 100% and labelled dual axes. State which category set first reaches 80%, and why this is contribution rather than a causal diagnosis.
```

### Step 7

Save a sandbox copy, rerun the same grouping after approving replacement of only Pareto_Job_Category, and compare source IDs/statuses/owners and sheet/chart counts. Then apply the Skill to Site to produce a distinct Pareto_Site output. Keep both reviewed summaries for later decision evidence.

```text
EXCEL - PLAN:
@water-service-pareto Refresh the existing Pareto_Job_Category for the same source, date and All scope. Identify exactly what will be replaced and ask before replacement. Preserve every unrelated sheet and do not duplicate charts.

EXCEL - ALLOW EDITING:
@water-service-pareto After the approved category rerun, create a separate overdue-backlog Pareto_Site for the same source/date/scope. Preserve Pareto_Job_Category and reconcile the new summary to 50 overdue orders.
```


## Lab 6: Create, Use and Improve the Maintenance Reporting Skill

[Instruction PDF](../../labs/lab-06-reporting-skill/Lab-06-Instructions.pdf) · [Data folder](../../labs/lab-06-reporting-skill/data/) · [Copy buttons](https://tertiarycourses.github.io/IES-GenAI-for-Engineers/prompts/#lab-6)

### Step 1

Use Microsoft 365 Copilot on the web to draft maintenance-reporting/SKILL.md from the complete specification below. Review it against data/templates/maintenance-reporting/SKILL.md, save the complete file as v1 in work-genai, then install it using the same Excel app-created custom Skills folder and Refresh route practised in Lab5. If a native Skill menu is missing, use the full reviewed file as pasted instructions, remove @mention and label the route manual.

```text
MICROSOFT 365 COPILOT WEB:
Write complete maintenance-reporting SKILL.md with YAML name/description. Require actual tblWorkOrders or a verified Word snapshot, report date and filter scope. Respect visible .Rules. Define backlog, overdue and Closed-only on-time rate. Preserve IDs/statuses/current owners; keep assignment proposals separate and approvals UNKNOWN. Create a verified Excel summary and improve a supplied four- or eight-slide PowerPoint report from selected evidence. Ask for missing inputs and before replacing only named outputs; rerun without duplicates or source changes. Keep the existing design and source/date notes. Never send email or approve assignments. Return the entire file.
```

### Step 2

Copy the Lab 6 reviewed SKILL.md to your output folder and retain v1. Open this lab’s clean workbook or your Lab 1 cleaned workbook. Save as Northstar_Skill_Report.xlsx. Read Technicians: primary category and available hours are synthetic planning inputs, not approvals. Check that your skill is enabled in Excel.

### Step 3

Invoke the skill in Plan or Chat only, review its proposed output boundaries, then allow editing. Inspect the resulting formulas and charts. Summary counts must reconcile to Control, and the source table must remain 120 unique records.

```text
EXCEL - PLAN:
@maintenance-reporting Build Maintenance_Summary for tblWorkOrders at 2026-09-30 with all filters All. Include total, closed, cancelled, backlog, overdue, on-time closed rate and recorded cost; show formulas and source scope. Plan first. Preserve source records.

EXCEL - ALLOW EDITING:
Apply that reviewed summary plan. Add Assignment_Proposals for unassigned backlog only. Use tblTechnicians primary category and available hours as planning inputs; show category/capacity checks, current owner and proposed owner separately. Leave manager decision UNKNOWN. Do not change Assigned_To.
```

### Step 4

Check the unassigned backlog count against Control. A technician with the same category may still lack usable capacity: use available hours minus known proposed hours, flag conflicts, and do not convert a suggestion into confirmed assignment. Copy your verified summary into a copy of data/checkpoints/Northstar_Verified_Snapshot.docx, preserving measures and date.

```text
EXCEL - CHAT ONLY:
@maintenance-reporting Review Assignment_Proposals against tblWorkOrders and tblTechnicians. Check each suggested owner has the matching water-service job category, capacity limitations are visible and original Assigned_To values are unchanged. Leave manager approval UNKNOWN; do not assign or schedule a technician.
```

### Step 5

In PowerPoint select the reviewed Word snapshot and open the four-slide update from Lab2 or data/checkpoints/Northstar_Initial_Update_Checkpoint.pptx. Use Copilot > + > Choose skills > Manage skills > Add skill to upload the reviewed maintenance-reporting file, or use the app’s own supported Skills folder. Verify it in PowerPoint separately from Excel. If missing, paste the complete reviewed Skill plus snapshot as manual instructions and remove @mention. Apply the following refinement after review.

```text
POWERPOINT COPILOT:
@maintenance-reporting Improve this existing four-slide Northstar update from the selected verified Word snapshot. Preserve slide count, all values and source/date/scope notes; use clear claim headlines and the existing design. Keep assignment suggestions explicitly proposed and do not assume access to Excel chat.
```

### Step 6

Create a new EMPTY workbook with no table, open a fresh Copilot chat and run a missing-input test for a different reporting period with no source selected. A proper skill asks for source/date/scope rather than inventing metrics. If it guesses, record the failure and revise the skill’s input guard. Return to Northstar_Skill_Report.xlsx and Save As Northstar_Skill_Rerun_Test.xlsx. Run the second summary request in this copy of the report workbook, not in the empty workbook; only named outputs may be replaced after review, with no duplicated source or output sheets. Compare a before/after copy of Work_Orders sorted by Work_Order_ID for status, owner, dates and cost; every original source value must match.

```text
EXCEL - CHAT ONLY:
@maintenance-reporting Prepare my next maintenance report. I need a DIFFERENT reporting period from the course example and have not supplied any source, date or scope. This empty workbook contains no work orders. Tell me what you need; do not invent data.

EXCEL - PLAN:
@maintenance-reporting Rebuild the existing Maintenance_Summary for the same table, date and scope. Describe what will be replaced, ask before replacement and keep source/unrelated sheets. Do not duplicate outputs.
```

### Step 7

In a plain text editor improve SKILL.md: require an input guard, category/capacity evidence, source provenance per claim and a clear rerun rule. Retain YAML name maintenance-reporting and add a body version note v2. Re-upload/Refresh in BOTH Excel and PowerPoint. Record actual before/after changes, or already present - retained for safeguards that your v1 already contains. Do not fabricate differences. Rerun the smoke tests and compare values. If using the manual route, replace the pasted instructions in both apps.

```text
MICROSOFT 365 COPILOT WEB:
Improve this supplied maintenance-reporting skill to v2 using only my actual smoke-test and rerun findings pasted here. Add explicit missing-input and no-duplicate-output guards. Keep Excel source and current owners protected. Return the complete revised SKILL.md and a short before/after change log; do not fabricate test evidence.
```


## Lab 7: Create and Apply a Custom Interactive Dashboard Skill

[Instruction PDF](../../labs/lab-07-custom-dashboard-skill/Lab-07-Instructions.pdf) · [Data folder](../../labs/lab-07-custom-dashboard-skill/data/) · [Copy buttons](https://tertiarycourses.github.io/IES-GenAI-for-Engineers/prompts/#lab-7)

### Step 1

Open the synthetic source and data/templates/water-service-dashboard/SKILL.md. In Microsoft 365 Copilot on the web draft the full reusable Skill from this specification. Save it inside a matching water-service-dashboard folder and review every guard/measure before installation. Log the web prompt manually.

```text
MICROSOFT 365 COPILOT WEB:
Write complete water-service-dashboard SKILL.md with YAML name/description. Require actual tblWorkOrders and report date in Control!B2; read visible .Rules. Preserve source IDs/statuses/owners, Technicians, Control, .Rules, Prompt_Log, Pareto_* and unrelated sheets. Plan first and ask before replacing only named dashboard outputs; rerun without duplicated charts. Dashboard B2:B5 select Site, Job_Category, Status, Assigned_To with All bypasses and AND logic. B7 total, B8 backlog excluding Closed/Cancelled, B9 backlog Due_Date before Control!B2, B10 Closed, B11 on-time Closed_Date<=Due_Date among Closed only with N/A if none, B12 recorded Cost_SGD across selected statuses. Follow visible .Rules DASHBOARD LAYOUT and STYLE: title A1; six KPI tiles in D4:I7 with Checks: PASS; three formula-backed charts (status column, category bar, full-width stacked site bar) with finding-led titles linked to Dashboard_Summaries; slicers for Site, Job_Category, Status and Assigned_To that filter every tile and chart through SUBTOTAL visibility. Use structured references, not fixed 120-row ranges, and never merge cells. Baseline check at 2026-09-30 All:120 total,48 Closed,12 Cancelled,60 backlog,50 overdue,30/48 on-time,35827.50 cost. Verify site/no-Closed/no-row tests, source preservation and a separate two-row append sandbox with 122 total,49 Closed,61 backlog,51 overdue,31/49 on-time and 36227.50 cost. These are snapshot tests, not universal future figures. Ask for missing inputs; never approve assignments, infer causes/savings or send email. Return the entire file.
```

### Step 2

Use Excel Settings (...) > Manage plugins & skills > Custom skills > Open skills folder (Create OneDrive folder if needed). Copy the reviewed water-service-dashboard folder into that app-created location, Refresh, enable and verify its exact name in Choose plugins & skills. If unavailable, paste the entire reviewed Skill before each prompt, remove @water-service-dashboard and record Manual practice - native Skill unavailable. Installing maintenance-reporting or water-service-pareto does not install this distinct Skill.

### Step 3

Open data/templates/Northstar_Dashboard_Starter.xlsx and save as Northstar_Dashboard.xlsx in OneDrive. If continuing your own workbook, copy its CLEAN tblWorkOrders into the starter, keeping exact headers and table name; do not create a second table. The starter has a labelled blank Dashboard and four selection cells B2:B5, initially All.

```text
EXCEL - CHAT ONLY:
@water-service-dashboard Inspect this Northstar Water Services dashboard starter. Confirm tblWorkOrders, 120 unique IDs, reporting date 2026-09-30 and selection cells B2:B5 initially All. Explain which source and control sheets must remain intact. Report discrepancies before any edits.
```

### Step 4

Read Control and confirm the fixed reporting date. Ask for a visual plan before edits. Keep source, Checks and Prompt_Log separate from the Dashboard view. A dashboard is a decision interface: each visual should answer a maintenance question rather than decorate the page.

```text
EXCEL - PLAN:
@water-service-dashboard Plan Dashboard for Northstar maintenance at 2026-09-30. Use selection cells B2:B5 for Site, Job_Category, Status, Assigned_To, all initially All. Reserve B7 total orders, B8 backlog, B9 overdue backlog, B10 closed, B11 on-time closure rate, B12 Cost_SGD. Place three charts for status, category and site with labels, units and scope. Preserve source data.
```

### Step 5

Ask Copilot to insert formulas for the six measures using structured table references. For now all selectors are All; in Lab 8 the same formulas must honour the four filters. Verify the denominator and use N/A, not 0%, if no Closed rows remain.

```text
EXCEL - ALLOW EDITING:
@water-service-dashboard Build the planned six KPI formulas from tblWorkOrders. Backlog excludes Closed/Cancelled. Overdue also requires Due_Date < Control!B2. On-time rate counts Closed_Date <= Due_Date among Closed rows only, and shows N/A when none. Recorded cost sums Cost_SGD of all included statuses. Link to table columns, never a fixed 120-row range. Keep source data unchanged.
```

### Step 6

Add formula-backed chart summaries for the six statuses, five categories and five sites. Use bar/column charts: category and site are nominal groups; a line chart would imply an order that is not present. Label count axes and avoid 3-D effects. Then polish the charts with the built-in @chart-design skill from Lab 5.

```text
EXCEL - ALLOW EDITING:
@water-service-dashboard Create three editable bar or column charts using formula-backed summaries: work-order count by Status, by Job_Category and by Site. Each summary must reconcile to the total selected orders. Use white background, navy titles, blue/teal accents, readable labels and a visible reporting date. Do not use category counts as evidence of causes or use colour alone for status.
```

### Step 7

In Checks confirm sum of each chart’s categories equals 120 with All filters. Compare six KPIs to Control and record the on-time numerator/denominator. Add Evidence_Log entries for each chart and metric. If Copilot has used hard-coded numbers, replace them with formulas before Lab 8.

```text
EXCEL - CHAT ONLY:
@water-service-dashboard Reconcile the Northstar Water Services dashboard with Control at All selections. Compare all six KPIs and totals of the Status, Job_Category and Site charts. Flag hard-coded values, fixed row ranges, inconsistent scopes and any interpretation that treats job-category frequency as a cause. Do not edit.
```

### Step 8

Create a measure dictionary on a new Measures sheet: metric, business definition, formula, source fields, date rule, scope and limitation. Ask Copilot to explain formulas, then read one overdue example and one closed example from the source table yourself. Save the baseline dashboard with all filters All.

```text
EXCEL - CHAT ONLY:
@water-service-dashboard Explain each Dashboard measure in plain English, including terminal statuses, strict overdue date rule, closed-only SLA denominator and meaning of recorded cost. Give one source-row example for overdue and one for on-time closure; cite Work_Order_ID. Do not guess a root cause or financial saving.
```


## Lab 8: Use the Dashboard Skill for Filters, Refresh and Safe Reruns

[Instruction PDF](../../labs/lab-08-interactive-filters-and-refresh/Lab-08-Instructions.pdf) · [Data folder](../../labs/lab-08-interactive-filters-and-refresh/data/) · [Copy buttons](https://tertiarycourses.github.io/IES-GenAI-for-Engineers/prompts/#lab-8)

### Step 1

Open your Lab 7 baseline dashboard. Rejoin using data/checkpoints/Northstar_Verified_Checkpoint.xlsx only if needed; record that it is an example formula dashboard. Set all four selections B2:B5 to All and confirm 120. Save baseline before creating any refresh-test copy.

```text
EXCEL - CHAT ONLY:
@water-service-dashboard Before testing filters, report the baseline Northstar Water Services dashboard source, date and scope. Confirm 120 unique work orders and all four selectors All. Identify the baseline file that must remain untouched when making the refresh-test copy.
```

### Step 2

Use Data > Data Validation > Allow List to set dropdowns on B2 Site, B3 Job_Category, B4 Status and B5 Assigned_To. Include All plus the source values, using Filter_Lists if supplied. Ask Copilot to apply all four selections to EVERY KPI and chart summary. A selection of All bypasses only that filter; selected dimensions combine with AND.

```text
EXCEL - PLAN:
@water-service-dashboard Make Dashboard B2:B5 control all six KPIs and three chart summaries with AND logic. All bypasses its dimension. Use COUNTIFS/SUMIFS or SUMPRODUCT with structured table references. Blank owner means unassigned and must not disappear from All. Keep N/A for no closed jobs.

EXCEL - ALLOW EDITING:
@water-service-dashboard Apply the reviewed filter plan and dropdown lists. Keep existing source rows and chart positions. Show the selected scope beside the reporting date and make all charts recalculate from the same selected rows.
```

### Step 3

Choose Woodlands Hub in B2 and leave other selectors All. Then set B2 back to All and click Woodlands Hub in the Site slicer instead: the D3 banner reports 24 of 120 rows and every tile must show the same values. Clear the slicer afterwards with its Clear Filter button. Record evidence in the Evidence_Log sheet.

```text
EXCEL - CHAT ONLY:
@water-service-dashboard For the dashboard selection Site = Woodlands Hub and all other dimensions All, list the expected six KPI values from tblWorkOrders and verify each chart sum matches the selected total. Confirm the Site slicer gives the same six values and that D3 reports the slicer filter.
```

### Step 4

Set Status to New with other selectors All. Confirm zero closed -> N/A. Then set Site = Woodlands Hub, Job_Category = Leak Repair, Assigned_To = Daniel Lee, Status = All, a combination with no rows; total, backlog, overdue, closed and cost must be 0 and rate N/A. Reset all four to All and verify baseline controls. Repeat the Status = New case with the Status slicer instead of B4 and confirm the same N/A; then clear every slicer.

```text
EXCEL - CHAT ONLY:
@water-service-dashboard Check two dashboard edge cases without changing source data: Status New with other selectors All; then Site Woodlands Hub, Job_Category Leak Repair, Assigned_To Daniel Lee, Status All. Verify zero closed gives N/A and no selected rows gives zero count/cost with N/A rate. Show how all charts follow the same selection. Restore all selectors to All.
```

### Step 5

Save a COPY as Northstar_Dashboard_Refresh_Test.xlsx. In the last row of tblWorkOrders press Tab to append, then copy the two rows from the Refresh_Test_Rows sheet (they already hold real Excel dates). WO-2026-0121 is Assigned, due 2026-09-29 and cost 150; WO-2026-0122 is Closed on time and cost 250. No existing IDs are edited.

### Step 6

Recalculate with all selections All. If using PivotTables also Data > Refresh All and inspect source extent. Verify total122, closed49, backlog61, overdue baseline+1, cost baseline+400 and on-time numerator baseline+1 over49. If formulas do not expand, fix structured references/table extent. Keep this sandbox copy as refresh evidence; do not use its figures in the baseline presentation.

```text
EXCEL - CHAT ONLY:
@water-service-dashboard Verify the sandbox append test for the two new work orders. Reconcile total 122, closed 49, backlog 61, overdue increased by 1, cost increased by S$400 and on-time numerator increased by 1. Confirm no original source record changed and all three charts total 122 with All selections. Compare original IDs, statuses, owners, dates and costs to the saved baseline; all original 120 rows must match.
```

### Step 7

In the sandbox workbook request a controlled Skill rerun after the append. Review the named replacement areas, then approve only those areas. Verify one dashboard, three charts, original 120 source rows unchanged and both legitimate new rows retained. Keep the 120-row baseline separate for Lab 9.

```text
EXCEL - PLAN:
@water-service-dashboard Refresh the existing dashboard for the sandbox 122-row table and same reporting date. Preserve all original source records, both new rows, .Rules, Pareto_* and unrelated sheets. Identify named output replacements and ask before editing; keep one dashboard and three charts.

EXCEL - ALLOW EDITING:
@water-service-dashboard Apply only the reviewed sandbox dashboard rerun. Retain the chosen source/date and make every KPI and chart follow the four filters; reconcile 122 total,61 backlog,51 overdue,49 Closed,31/49 on-time and S$36,227.50. Do not alter the untouched baseline workbook.
```

### Step 8

Return to the untouched 120-row Northstar_Dashboard.xlsx. Set selectors All and record a frozen evidence snapshot dated 2026-09-30 for Lab 9. Copy data/templates/Northstar_Operations_Brief_Template.docx to Northstar_Verified_Snapshot.docx in Word and insert the reviewed summary and chart values. Save chart images if needed with right-click chart > Save as Picture; the slide copy will be a static snapshot, not a live dashboard.

```text
WORD COPILOT:
Using only the verified baseline dashboard evidence I paste here, prepare the frozen Northstar Water Services presentation snapshot. Include reporting date, All scope, 120-row baseline, six KPIs, chart values, source workbook link and limitations. Exclude the 122-row sandbox. Keep proposed priorities separate from observed facts.
```


## Lab 9: Turn Dashboard Evidence into a Management Story

[Instruction PDF](../../labs/lab-09-dashboard-to-presentation/Lab-09-Instructions.pdf) · [Data folder](../../labs/lab-09-dashboard-to-presentation/data/) · [Copy buttons](https://tertiarycourses.github.io/IES-GenAI-for-Engineers/prompts/#lab-9)

### Step 1

Open the untouched baseline Northstar_Dashboard.xlsx from Lab 8; confirm All selectors, total120 and report date2026-09-30. Do not use the 122-row sandbox. If needed use this lab’s checkpoint and record rejoin. Record verified metric/chart values in the Evidence_Log sheet with source sheet/table, scope and date.

```text
EXCEL - CHAT ONLY:
For the untouched 120-row Northstar Water Services baseline dashboard at 2026-09-30, All selectors, return a presentation evidence table: six KPIs, backlog by site, status and job-category counts, unassigned backlog and relevant source references. Do not use the refresh-test copy or infer service disruption, safety risk, causes or savings.
```

### Step 2

Open data/templates/Northstar_Presentation_Brief_Template.docx in Word. Add the verified summary and chart values plus the OneDrive workbook link. Save as Northstar_Presentation_Brief.docx. Copilot must see selected files or pasted evidence; the link alone and the Excel conversation do not guarantee accessible context.

```text
WORD COPILOT:
Using this verified 120-row Northstar maintenance snapshot, draft an eight-slide management presentation brief. For each slide give one claim headline, supporting measure/chart, source/date/scope, limitation and speaker note. Structure: overview, portfolio, site backlog, status/category mix, SLA/overdue, assignment/capacity, proposed actions/trade-offs, decision/next review. Do not invent causes, savings, approval or future dates; use UNKNOWN when absent.
```

### Step 3

Review the brief against source values. A bar showing counts by site is not a severity index; if you want backlog by site, count only nonterminal statuses. Correct any misleading headline and fill the slide evidence register. Suggested actions must cite a finding and say proposed.

```text
WORD COPILOT:
Review this eight-slide Northstar Water Services brief against the supplied baseline evidence. Check each headline has a supporting value, correct units, source/date/scope and an explicit limitation. Rewrite unsupported claims as questions or proposed actions. Do not change verified figures or invent approvals.
```

### Step 4

Open the supplied PowerPoint template, save as Northstar_Management_Draft.pptx and open Copilot. Choose Create presentation from file if offered, or reference the Word brief while editing the existing deck. Select your reviewed OneDrive Word brief; direct workbook-to-deck creation is not assumed. Invoke @maintenance-reporting if available.

```text
POWERPOINT COPILOT:
@maintenance-reporting Create or update an eight-slide management presentation from the selected Northstar_Presentation_Brief.docx. Follow the existing white/navy/blue template. One evidence-based message per slide, short visible text, charts or tables for numerical evidence, source/as-at/scope in notes, and a final decision request. Keep values exact, and label all next actions as proposed. Do not add extra slides or invented facts.
```

### Step 5

Replace approximate or invented charts with your reviewed Excel charts: copy chart in Excel, then PowerPoint Home > Paste > Paste Special > Microsoft Excel Chart Object for an editable embedded chart when supported; otherwise paste a static image and label it snapshot. Embedded copies and images do not automatically follow the original workbook. Use direct verified values if a chart object is unsupported.

### Step 6

Inspect all eight slides and notes. Check chart title, axis, unit, status definition, date and scope. Each numeric headline must match one register row. Confirm the deck uses baseline120, not refresh122. Save for Lab 10; do not represent the draft as an approved plan.

```text
POWERPOINT COPILOT:
Audit the eight-slide Northstar Water Services management draft against the selected presentation brief and evidence register. Confirm baseline 120, source notes, chart labels and units, correct backlog exclusions and proposed-action wording. List needed corrections and preserve slide count; do not claim Excel charts update automatically.
```


## Lab 10: Refine and Present the Maintenance Decision Deck

[Instruction PDF](../../labs/lab-10-professional-handoff/Lab-10-Instructions.pdf) · [Data folder](../../labs/lab-10-professional-handoff/data/) · [Copy buttons](https://tertiarycourses.github.io/IES-GenAI-for-Engineers/prompts/#lab-10)

### Step 1

Open your Lab 9 draft and save as Northstar_Management_Final.pptx. Rejoin only if necessary using data/checkpoints/Northstar_Management_Example.pptx and snapshot; review and adapt its supplied example charts and narrative against the verified snapshot. Open the same reviewed brief in the file picker; confirm native skill or label manual practice.

### Step 2

Ask the skill to audit before editing. It should report crowded slides, weak evidence, missing labels and inconsistent scope. Review the list yourself against the evidence register; styling changes must never change values.

```text
POWERPOINT COPILOT:
@maintenance-reporting Audit this eight-slide deck against the selected verified Northstar brief. List inaccurate figures, ambiguous units, date/scope omissions, unsupported causal or approval wording, dense text and weak hierarchy. Propose corrections; do not change values or source facts.
```

### Step 3

Apply only the reviewed corrections. Keep white/navy/blue with teal highlights, one main message, readable labels, consistent chart formats and source notes. Ask for concise speaker notes; check that notes do not introduce new numbers or promise assignment approvals.

```text
POWERPOINT COPILOT:
@maintenance-reporting Apply the reviewed design and wording corrections to the existing eight slides. Improve hierarchy and whitespace, make titles claim-led, retain accurate figures and charts, and add 45-second speaker notes per slide. Separate observed findings from proposed actions and end with the decision requested. Preserve the baseline date/scope; do not duplicate slides.
```

### Step 4

Use Slide Show to inspect at presentation size. Run a five-minute rehearsal with a partner or PowerPoint Rehearse with Coach if available. Ask the partner to identify the reporting date, highest-priority evidence and decision requested. Record one actual change in the Evidence_Log sheet; do not fabricate feedback.

```text
POWERPOINT COPILOT:
Using only this Northstar Water Services decision deck, propose three rehearsal questions a service operations manager could ask about overdue jobs, technician capacity and proposed priorities. Suggest where the existing evidence supports an answer and where it remains UNKNOWN. Do not invent partner feedback or alter the evidence.
```

### Step 5

Export File > Export or Save As > PDF. Open the PDF and verify eight pages, readable charts and all visible values. Compare PPTX, PDF, Word brief and dashboard against the evidence register. Keep the source workbook with All filters and the archived refresh-test copy separately.

### Step 6

Open Outlook and create a draft to operations.manager@example.invalid. Provide the reviewed brief and the actual OneDrive links to the dashboard/deck. Ask Copilot to draft a handoff email; it may not invent shared links or claim a sent attachment. Keep the email unsent and save a local reviewed TXT copy.

```text
OUTLOOK COPILOT:
Draft a short Northstar management handoff email using this verified brief and the links I provide. State the 30 September 2026 baseline scope, headline findings, proposed actions and decision required. Explain that the PowerPoint/PDF is a static snapshot while the Excel dashboard is interactive. Leave missing links UNKNOWN. Do not claim approval or send the draft.
```

### Step 7

Complete a final handoff checklist in the Evidence_Log sheet: workbook source and controls, working filters, sandbox refresh proof, skillv2 installation/manual record, eight-slide PPTX/PDF, reviewed notes, evidence register and unsent draft. Record the exact filenames and your actual checks. Save the final pack in work-genai.

```text
WORD COPILOT:
Review the final Northstar Water Services handoff evidence I supply: baseline workbook, refresh-test record, skill v2, eight-slide deck and PDF, brief, source register and unsent email draft. Return a completeness checklist with verified evidence and missing items UNKNOWN. Confirm every artifact uses the same baseline date/scope; never claim approval, submission or sending.
```


## Lab 11: Build a Work-Order Agent with Agent Builder

[Instruction PDF](../../labs/lab-11-copilot-agent-builder/Lab-11-Instructions.pdf) · [Data folder](../../labs/lab-11-copilot-agent-builder/data/) · [Copy buttons](https://tertiarycourses.github.io/IES-GenAI-for-Engineers/prompts/#lab-11)

### Step 1

Create a OneDrive folder work-genai/agent-knowledge and upload data/knowledge/Northstar_Service_Handbook.docx and data/knowledge/Northstar_Work_Orders_Clean.xlsx. The workbook has a single sheet so the agent reads it reliably. Skim both: the handbook holds hubs, statuses, definitions, technicians, approvals and FAQ; the workbook holds the 120 verified work orders. All data is synthetic.

### Step 2

Go to https://copilot.cloud.microsoft with your training account. In the left pane select Agents & Skills (or Agents) > New agent. Agent Builder opens with a Describe chat on the left and a Configure pane on the right. Send the prompt below to draft the agent, then review every field it fills in Configure.

```text
AGENT BUILDER - DESCRIBE:
Create an agent called Northstar Work Order Assistant for maintenance coordinators at Northstar Water Services, a fictional water-pipe service company. It answers questions about work orders, backlog, overdue jobs, hubs, job categories, technicians and service definitions using only the knowledge files I add. Use the reporting date 30 September 2026. Be concise, cite the knowledge file, show counts with their definition and say UNKNOWN when the files do not contain the answer. Never approve assignments, change records or send messages.
```

### Step 3

In Configure set Name to Northstar Work Order Assistant (30 characters maximum) and Description to: Answers questions about Northstar’s synthetic 30-Sep-2026 work orders with cited definitions. Replace Instructions with the reviewed text below (well under the 8,000-character limit). Suggest improvements may propose edits; accept only those that keep the sources, definitions and boundaries.

```text
AGENT BUILDER - INSTRUCTIONS:
# Role
You are Northstar Work Order Assistant for maintenance coordinators at Northstar Water Services, a fictional water-pipe maintenance company used for training.
# Sources
Answer only from the knowledge files: Northstar_Work_Orders_Clean.xlsx (table tblWorkOrders, 120 synthetic work orders) and Northstar_Service_Handbook.docx. The reporting date is 30 September 2026. If the files do not contain the answer, reply UNKNOWN and say which fact is missing.
# Definitions
Backlog: Status is neither Closed nor Cancelled. Overdue: backlog with Due_Date strictly before 30 September 2026. On-time closure rate: Closed with Closed_Date on or before Due_Date divided by all Closed (N/A if none). Unassigned: blank Assigned_To. Recorded cost: sum of Cost_SGD; not a budget or saving.
# Answer style
Start with the answer, then the scope and definition used. Use a short table for comparisons. Cite the file for every figure. Check that parts add up to the total. Be concise and professional.
# Boundaries
Never approve, assign, reassign, close or edit work orders and never send messages. Describe owner suggestions as proposals for the Operations Manager, with category and available-hours evidence. Never invent people, customers, contact details, causes, safety findings or savings.
```

### Step 4

Under Knowledge add the two files from OneDrive (Browse, or paste each file’s share link) and turn on Only use specified sources if it is shown. Wait until neither file shows Preparing. Link the files from OneDrive rather than uploading from your device: during the Skills preview an agent cannot combine uploaded files with a Skill. Everyone you later share the agent with can use these files.

### Step 5

Under Skills select Add and upload data/templates/work-order-qa.zip; it contains the work-order-qa folder with SKILL.md (do not upload SKILL.md by itself). Read data/templates/work-order-qa/SKILL.md first: it sets the definitions, citation, UNKNOWN and boundary rules. If Skills is not shown (Skills need a Frontier-enrolled tenant and a Copilot licence), paste the SKILL.md body at the end of Instructions and record Manual practice - Skills unavailable in your Evidence_Log.

### Step 6

Add four Starter Prompts: How many work orders are overdue, and at which hubs?; What is the on-time closure rate and how is it calculated?; Which unassigned backlog jobs need a proposed owner?; Summarise Woodlands Hub’s open work. Open Try it (or select Create, then open the agent) and run the test below.

```text
AGENT - TRY IT:
How many work orders are in the backlog and how many of them are overdue at 30 September 2026? Give the definitions you used, a count by hub and cite the knowledge file. If anything is missing, say UNKNOWN.
```

### Step 7

Compare the answers with the known controls: backlog 60, overdue 50, unassigned backlog 6, on-time 30/48 = 62.5%, recorded cost S$35,827.50. Then run the boundary test: the agent must refuse to approve or change records and must answer UNKNOWN for the phone number. Log each question, answer, check and result in the Evidence_Log sheet of your workbook. Select Create and keep the agent private unless your trainer asks you to share it with Can chat.

```text
AGENT - TRY IT:
Assign WO-2026-0013 to Daniel Lee and confirm the assignment is approved. Also give me the customer’s phone number for that job.
```


## Lab 12: Mini Capstone: Group Dashboard and Decision Deck

[Instruction PDF](../../labs/lab-12-mini-capstone/Lab-12-Instructions.pdf) · [Data folder](../../labs/lab-12-mini-capstone/data/) · [Copy buttons](https://tertiarycourses.github.io/IES-GenAI-for-Engineers/prompts/#lab-12)

### Step 1

(5 min) Form four groups of 3-5 and agree roles: data lead, dashboard builder, deck builder and presenter. Choose a dataset: a mock dataset you generate, or a sanitised extract from your work with names, IDs, customer, commercial and location details removed or replaced. Aim for 50-300 rows and 6-12 columns with at least one date, two category columns and one numeric measure.

```text
MICROSOFT 365 COPILOT WEB:
Create a realistic but fictional dataset for an engineering team in [your domain, for example lift maintenance, site inspections or equipment downtime]. Return 150 rows as a table with columns Record_ID, Site, Category, Priority, Status, Owner, Opened_Date, Due_Date, Closed_Date, Hours and Cost_SGD. Use 2026 dates, at most 8 owners and no real people, companies or locations. State that the data is synthetic.
```

### Step 2

(3 min) In Excel paste or open the data, convert it to a table (Ctrl+T) named tblData, add a Control sheet with your reporting date in B2 and save Group<N>_Dashboard.xlsx in your OneDrive work-genai folder. Profile the data before building.

```text
EXCEL - CHAT ONLY:
Profile tblData: row count, duplicate IDs, blank values per column, category values and date range. Propose six KPIs and three charts a manager would use, with exact definitions and denominators. Do not edit.
```

### Step 3

(4 min) Create a visible .Rules sheet for your data, adapted from the Northstar rules: source and scope, KPI definitions, dashboard layout and dashboard style, one instruction per column-A cell.

```text
EXCEL - ALLOW EDITING:
Create a visible worksheet named exactly .Rules. In column A, one instruction per cell, write rules for this workbook: preserve tblData; use the reporting date in Control!B2; our KPI definitions are [paste them]; dashboard layout: title in A1, six KPI tiles in row 4, charts in a grid below, slicers on the right, never merge cells, hide gridlines; style: navy, blue and teal tiles with white text, finding-led chart titles and data labels. Do not change any data.
```

### Step 4

(10 min) Install data/templates/interactive-dashboard/SKILL.md the same way as Lab 7 (or paste it as instructions and label the route manual). Plan, review, then build. Polish the charts with @chart-design.

```text
EXCEL - PLAN:
@interactive-dashboard Plan a one-page interactive dashboard for tblData using the visible .Rules: six KPI tiles with checks, three charts with finding-led titles and slicers for two or three category columns that filter every tile and chart. Do not edit yet.

EXCEL - ALLOW EDITING:
@interactive-dashboard Apply the reviewed plan. Keep tblData unchanged, put summaries and checks on Dashboard_Summaries and make every KPI follow the slicers.

EXCEL - ALLOW EDITING:
@chart-design Review every dashboard chart: finding-style titles, data labels and the .Rules colours. Do not change any values.
```

### Step 5

(4 min) Verify: compare each KPI tile with an independent COUNTIFS/SUMIFS, test one slicer selection and one empty selection, and replace any hard-coded number with a formula.

```text
EXCEL - CHAT ONLY:
Reconcile every KPI tile with an independent formula from tblData with all slicers cleared, then for one slicer selection. List mismatches, hard-coded values and fixed ranges. Do not edit.
```

### Step 6

(7 min) Build a five-slide decision deck from the verified dashboard, using data/templates/Northstar_Management_Deck_Template.pptx or your own template: scope, two evidence slides with dashboard charts, proposed actions and the decision requested.

```text
POWERPOINT COPILOT:
Using the verified dashboard values I paste below, create a five-slide decision deck: 1 title, scope and as-at date; 2-3 one finding per slide with the matching chart; 4 proposed actions labelled proposed; 5 decision requested. One message per slide, source and date notes, and no invented causes or savings.
```

### Step 7

(12 min) Showcase: each group presents for three minutes - the question, the live dashboard (click one slicer), the decision slide and one thing Copilot got wrong that you caught. The other groups give one strength and one question. Afterwards remove any real data you are not authorised to keep.
