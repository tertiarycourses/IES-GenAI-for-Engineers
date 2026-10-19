# GenAI for Engineers - Prompt Library

[Open the prompts page with Copy buttons](https://tertiarycourses.github.io/IES-GenAI-for-Engineers/prompts/)


## Lab 1: Prepare Work Orders and Draft the Operations Brief

[Instruction PDF](../../labs/lab-01-excel-to-word/Lab-01-Instructions.pdf) · [Data folder](../../labs/lab-01-excel-to-word/data/) · [Copy buttons](https://tertiarycourses.github.io/IES-GenAI-for-Engineers/prompts/#lab-1)

### Step 1

Look at the data. Open data/Northstar_Work_Orders.xlsx in Excel and open Copilot from the Copilot button on the Home tab. Choose Chat only (answers, no changes) and send the prompt. Copilot should find 122 rows, 2 repeated IDs (WO-2026-0005 and WO-2026-0020) and 2 job categories spelt differently.

```text
EXCEL - CHAT ONLY:
Describe this work-order table for me. How many rows are there? Are there any repeated Work_Order_IDs, or Job_Category names spelt in different ways? Don’t change anything.
```

### Step 2

Clean the table. Switch to Allow editing and send the prompt. Select Done to keep the change, or Undo to reverse it. The table should now have 120 rows and 5 job categories.

```text
EXCEL - ALLOW EDITING:
Copy the table to a new sheet named Raw_Export. Then remove the repeated rows, keeping one row for each Work_Order_ID, and fix the Job_Category spelling. Leave empty Assigned_To cells empty.
```

### Step 3

Add check formulas. Send the prompt and select Done. You should see 120 total, 48 closed, 12 cancelled, 60 backlog, 50 overdue, 6 unassigned, cost S$35,827.50. Save the workbook (Ctrl+S / Cmd+S).

```text
EXCEL - ALLOW EDITING:
In the Checks sheet, add formulas that count the total work orders, closed, cancelled, backlog (not Closed or Cancelled), overdue backlog (due before the date in Control!B2) and unassigned backlog, and add up Cost_SGD.
```

### Step 4

Write the brief in Word. Open data/templates/Northstar_Operations_Brief_Template.docx in Word and save it as Northstar_Operations_Brief.docx. In Copilot select + > Upload images and files and choose Northstar_Work_Orders.xlsx from this lab’s data folder, then send the prompt.

```text
WORD COPILOT:
Write a one-page operations brief in this document from the uploaded Northstar_Work_Orders.xlsx. Include the reporting date, the key numbers from the Checks sheet, the backlog and overdue findings, the unassigned jobs, proposed next actions and open questions. Use only numbers from the workbook, and write UNKNOWN for anything it does not show.
```

### Step 5

Check the brief. Send the prompt in the same chat and fix any number it lists. Save the brief.

```text
WORD COPILOT:
Check every number in this brief against the uploaded workbook. List any number that is different, with the correct value.
```


## Lab 2: Create the Cross-App Maintenance Update

[Instruction PDF](../../labs/lab-02-word-to-powerpoint-and-outlook/Lab-02-Instructions.pdf) · [Data folder](../../labs/lab-02-word-to-powerpoint-and-outlook/data/) · [Copy buttons](https://tertiarycourses.github.io/IES-GenAI-for-Engineers/prompts/#lab-2)

### Step 1

Read the brief. Open data/Northstar_Operations_Brief.docx in Word, open Copilot and send the prompt. You don’t need to select any text. The table should show 120 total, 60 backlog, 50 overdue and 6 unassigned.

```text
WORD COPILOT:
Make a short table of the key numbers in this document: date, total, closed, cancelled, backlog, overdue, unassigned backlog and cost. Show it here in the chat and don’t change the document.
```

### Step 2

Make the slides. Open data/templates/Northstar_Management_Deck_Template.pptx in PowerPoint and save it as Northstar_Initial_Update.pptx. In Copilot select + > Upload images and files and choose Northstar_Operations_Brief.docx from this lab’s data folder, then send the prompt.

```text
POWERPOINT COPILOT:
Fill these 4 slides from the uploaded Northstar_Operations_Brief.docx: 1 scope and totals, 2 backlog and overdue work, 3 unassigned jobs and proposed actions, 4 the decision needed. Keep the design and use only numbers from the brief.
```

### Step 3

Check the slides. Send the prompt in the same chat, fix any wrong number on the slides and save.

```text
POWERPOINT COPILOT:
Check these 4 slides against the uploaded brief. List any number that is wrong and give the correct number.
```

### Step 4

Draft the email. In Outlook start a new email to operations.manager@example.invalid. Select Copilot > Draft with Copilot, paste the prompt and select Generate. Select Keep it, then close the email without sending it: it stays in your Drafts folder.

```text
OUTLOOK COPILOT:
Write a short reply to the email below. Use these numbers for 30 September 2026: 120 total, 48 closed, 12 cancelled, 60 backlog, 50 overdue, 6 unassigned, cost S$35,827.50. Say what we found, what we propose next and what decision we need. Say that any new assignment is only a proposal, not approved.
EMAIL (fictional):
2026-09-29 09:00 Operations manager: Please prepare the 30 September portfolio snapshot; show open work by site, category and current assignment.
2026-09-29 10:15 Supervisor: Check overdue jobs before proposing reassignment. Available hours are planning inputs, not approval.
2026-09-30 08:30 Analyst: The source export is in the workbook. No new assignment has been approved. Please produce a Word brief and a short PowerPoint update, then prepare a draft reply.
```

### Step 5

Compare all three. The brief, the slides and the email must show the same numbers. Fix anything that is different.

```text
Total : 120
Backlog : 60
Overdue : 50
Unassigned : 6
Cost : S$35,827.50
```


## Lab 3: Personalise Copilot in Excel for Consistent Service Reports

[Instruction PDF](../../labs/lab-03-personalisation/Lab-03-Instructions.pdf) · [Data folder](../../labs/lab-03-personalisation/data/) · [Copy buttons](https://tertiarycourses.github.io/IES-GenAI-for-Engineers/prompts/#lab-3)

### Step 1

Save four preferences. Open data/Northstar_Work_Orders.xlsx in Excel. In Copilot select Settings (...) > Personalization. Write down your current settings so you can put them back later, then add the four preferences below and select Save.

```text
Money : show S$ with two decimals
Dates : show as DD-MMM-YYYY
Formulas : use structured references
Answers : start with a one-line summary
```

### Step 2

See them work. Select New chat, choose Allow editing and send the prompt. Select Done to keep the change, or Undo to reverse it. The date shows as 30-Sep-2026 and the cost as S$35,827.50, although the prompt did not ask for these formats.

```text
EXCEL - ALLOW EDITING:
Add a sheet named Preference_Check that shows the reporting date from Control!B2, the number of work orders and the total Cost_SGD, using formulas.
```

### Step 3

Change a preference once. Send the prompt and select Done. The cost now shows S$35,827.5000: a prompt can override a preference for one task.

```text
EXCEL - ALLOW EDITING:
Just for this task, show the total cost on Preference_Check with four decimal places. Keep the same formula.
```

### Step 4

Ask what applies where. Choose Chat only and send the prompt.

```text
EXCEL - CHAT ONLY:
In this exercise, which settings belong to my account, which belong to this workbook, and which applied to one prompt only? Answer in three short points.
```

### Step 5

Put your settings back. Select Settings (...) > Personalization, restore the settings you wrote down and select Save.

```text
Excel : Copilot > Settings (...) > Personalization
Check : your original settings are back
```


## Lab 4: Create and Test Workbook .Rules for Water Service Reporting

[Instruction PDF](../../labs/lab-04-workbook-rules/Lab-04-Instructions.pdf) · [Data folder](../../labs/lab-04-workbook-rules/data/) · [Copy buttons](https://tertiarycourses.github.io/IES-GenAI-for-Engineers/prompts/#lab-4)

### Step 1

Add the rules sheet. Open data/Northstar_Work_Orders.xlsx in Excel. In Copilot choose Allow editing, send the prompt and select Done. A sheet named .Rules appears as the last tab, with one rule in each cell of column A.

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

### Step 2

Add a date rule yourself. On the .Rules sheet click the first empty cell in column A, type the formula below and press Enter. It shows Reporting date: 2026-09-30.

```text
="Reporting date: "&TEXT(Control!B2,"yyyy-mm-dd")
```

### Step 3

Test the rules. Select New chat, choose Allow editing and send the prompt, then select Done. The prompt does not mention formats, but Rules_Test follows the rules: 120 total, 60 backlog, 50 overdue, on-time 30/48 = 62.5%, cost S$35,827.50.

```text
EXCEL - ALLOW EDITING:
Add a sheet named Rules_Test with the total work orders, backlog, overdue backlog, on-time closure rate and total cost from tblWorkOrders, using formulas.
```

### Step 4

Check the rules travel with the file. Save, then use File > Save As to save a copy named Northstar_Rules_Copy.xlsx. In the copy choose Chat only and send the prompt: Copilot lists the same rules.

```text
EXCEL - CHAT ONLY:
What rules does this workbook give you? List them briefly.
```


## Lab 5: Find the Vital Few Failure Modes with a Pareto Skill

[Instruction PDF](../../labs/lab-05-custom-pareto-chart-skill/Lab-05-Instructions.pdf) · [Data folder](../../labs/lab-05-custom-pareto-chart-skill/data/) · [Copy buttons](https://tertiarycourses.github.io/IES-GenAI-for-Engineers/prompts/#lab-5)

### Step 1

Turn on the built-in chart skill. Open data/Northstar_Work_Orders.xlsx in Excel. In Copilot select Settings (...) > Manage plugins & skills and turn on chart-design under Visualization.

```text
Excel : Copilot > Settings (...) > Manage plugins & skills
Turn on : chart-design (under Visualization)
```

### Step 2

Use it. Choose Allow editing and send the prompt. Select Done to keep the change, or Undo to reverse it. The bars run from highest to lowest, starting with Corrosion.

```text
EXCEL - ALLOW EDITING:
@chart-design Make a bar chart of the number of work orders for each Failure_Mode on a new sheet named ChartDesign_Demo, sorted from highest to lowest.
```

### Step 3

Upload the skill to OneDrive. In Excel open Copilot and select Settings (...) > Manage plugins & skills > Custom skills. Turn Custom skills on and select Add in OneDrive (or Create OneDrive folder, then Open skills folder). OneDrive opens at your skills folder. Select Create or upload > Folder upload and choose the water-service-pareto folder in this lab’s data/templates folder.

```text
OneDrive : Documents > Copilot > Microsoft Excel > skills > water-service-pareto > SKILL.md
```

### Step 4

Turn the skill on. Back in Excel select Settings (...) > Manage plugins & skills > Custom skills > Refresh, then turn water-service-pareto on. Close the dialog and type @wat in the Copilot prompt box: water-service-pareto should appear. If not, wait a minute and select Refresh again.

```text
Check : water-service-pareto appears when you type @
```

### Step 5

Find the vital few. Select New chat, choose Allow editing, send the prompt and select Done. You should see Corrosion 42, Joint seal leak 30, Valve seat wear 22, Pump bearing wear 10, Pressure surge 8, Meter fault 4, Blockage 2, Third-party damage 2. The top 3 failure modes cause 78% of all work orders.

```text
EXCEL - ALLOW EDITING:
@water-service-pareto Make a Pareto chart of Failure_Mode for all work orders in tblWorkOrders.
```

### Step 6

Look at the overdue jobs. Send the prompt and select Done. Among the 50 overdue jobs the order changes: Joint seal leak 14, Corrosion 13, Valve seat wear 8, Pump bearing wear 7, Pressure surge 3, Blockage 2, Meter fault 2, Third-party damage 1. A Pareto shows where to look first; confirm the root cause on site.

```text
EXCEL - ALLOW EDITING:
@water-service-pareto Now make the same Pareto chart for the overdue work orders only.
```


## Lab 6: Build a Maintenance Report with Two Skills

[Instruction PDF](../../labs/lab-06-reporting-skill/Lab-06-Instructions.pdf) · [Data folder](../../labs/lab-06-reporting-skill/data/) · [Copy buttons](https://tertiarycourses.github.io/IES-GenAI-for-Engineers/prompts/#lab-6)

### Step 1

Upload the skill to OneDrive. In Excel open Copilot and select Settings (...) > Manage plugins & skills > Custom skills. Turn Custom skills on and select Add in OneDrive (or Create OneDrive folder, then Open skills folder). OneDrive opens at your skills folder. Select Create or upload > Folder upload and choose the water-service-pareto and maintenance-reporting folders in this lab’s data/templates folder.

```text
OneDrive : Documents > Copilot > Microsoft Excel > skills > water-service-pareto > SKILL.md
OneDrive : Documents > Copilot > Microsoft Excel > skills > maintenance-reporting > SKILL.md
```

### Step 2

Turn the skills on. Back in Excel select Settings (...) > Manage plugins & skills > Custom skills > Refresh, then turn water-service-pareto and maintenance-reporting on. Close the dialog and type @ in the Copilot prompt box: water-service-pareto and maintenance-reporting should appear. If not, wait a minute and select Refresh again.

```text
Check : water-service-pareto appears when you type @
Check : maintenance-reporting appears when you type @
```

### Step 3

Build the summary. Open data/Northstar_Work_Orders.xlsx, select New chat, choose Allow editing and send the prompt. Select Done to keep the change, or Undo to reverse it. You should see 120 total, 48 closed, 12 cancelled, 60 backlog, 50 overdue, on-time 30/48 = 62.5% and cost S$35,827.50.

```text
EXCEL - ALLOW EDITING:
@maintenance-reporting Build a Maintenance_Summary sheet for 30 September 2026 with the total, closed, cancelled, backlog, overdue, on-time closure rate and cost.
```

### Step 4

Add the failure-mode Pareto. Send the prompt and select Done. The chart is sorted from highest to lowest: Corrosion 42, Joint seal leak 30, Valve seat wear 22, Pump bearing wear 10, Pressure surge 8, Meter fault 4, Blockage 2, Third-party damage 2.

```text
EXCEL - ALLOW EDITING:
@water-service-pareto Make a Pareto chart of Failure_Mode for all work orders and place it on the Maintenance_Summary sheet, to the right of the numbers.
```

### Step 5

Suggest owners. Send the prompt and select Done. Assignment_Proposals lists 6 jobs, each marked as a proposal, and Assigned_To on Work_Orders is unchanged. Save the workbook.

```text
EXCEL - ALLOW EDITING:
@maintenance-reporting Add an Assignment_Proposals sheet for the backlog jobs with no owner. Suggest an owner from tblTechnicians with the same job category and free hours, and mark each one as a proposal. Don’t change Assigned_To.
```

### Step 6

Use the skill in PowerPoint. Open data/Northstar_Initial_Update.pptx. In Copilot select + > Choose skills > Manage skills > Add skill and upload data/templates/maintenance-reporting/SKILL.md, then send the prompt. Every number must stay the same.

```text
POWERPOINT COPILOT:
@maintenance-reporting Improve these 4 slides with clearer headlines and less text. Keep every number and keep 4 slides.
```


## Lab 7: Create a PowerPoint Design Skill: From Plain to Professional

[Instruction PDF](../../labs/lab-07-powerpoint-design-skill/Lab-07-Instructions.pdf) · [Data folder](../../labs/lab-07-powerpoint-design-skill/data/) · [Copy buttons](https://tertiarycourses.github.io/IES-GenAI-for-Engineers/prompts/#lab-7)

### Step 1

Look at the plain deck. Open data/Northstar_Plain_Update.pptx in PowerPoint and save it as Northstar_Professional_Update.pptx. The numbers are right, but the slides are plain: black text, no header, no branding.

```text
Slides : 6
Look : plain black text, no colours, no header, no footer
```

### Step 2

Write the skill. Go to https://copilot.cloud.microsoft, start a new chat, paste the prompt and send it. Read the reply: it starts with --- and the name northstar-deck-design. Copy the whole reply.

```text
MICROSOFT 365 COPILOT WEB:
Write a complete SKILL.md for a Copilot in PowerPoint skill named northstar-deck-design. Start with --- front matter: name: northstar-deck-design and description: Use when I ask to make a presentation look professional or apply the Northstar brand. Then write numbered steps: 1) Keep every slide, number and fact; change only the design. 2) Fonts: Segoe UI Semibold for titles, Segoe UI for body text. 3) Colours: navy #1F4E79, blue #2E75B6, teal #2A9D8F, light grey #F2F4F7 cards, white background. 4) Slide 1: navy background, large white title, teal subtitle. 5) Every other slide: a navy header bar with a white title and a thin teal line under it. 6) Turn key numbers into KPI cards with a big bold number and a short label. 7) At most 4 short bullets per slide, with plenty of white space. 8) A footer on every slide except slide 1: Northstar Water Services | 30 September 2026, and the slide number. 9) Check every slide and list anything you could not fix. Return only the SKILL.md text, starting with ---, without code fences.
```

### Step 3

Add the skill to PowerPoint. In PowerPoint open Copilot and select + > Choose skills > Manage skills > Add skill. Paste the reply into the form and select Add. Short of time? Open data/templates/northstar-deck-design/SKILL.md in Notepad or TextEdit, copy all of it and paste that instead.

```text
Check : northstar-deck-design appears when you type @nor
```

### Step 4

Transform the deck. Send the prompt and watch every slide change: a navy title slide, a header bar on each slide, KPI cards for the numbers and a footer.

```text
POWERPOINT COPILOT:
@northstar-deck-design Redesign this whole deck in the Northstar style. Keep every slide and every number.
```

### Step 5

Check the result. Send the prompt and fix anything it lists. The numbers must not change: 120 total, 60 backlog, 50 overdue and 6 unassigned, cost S$35,827.50. Save the deck.

```text
POWERPOINT COPILOT:
@northstar-deck-design Check every slide against the skill. List any slide missing the header bar, footer, Northstar fonts or colours, and fix it. Do not change any number.
```


## Lab 8: Build an Interactive Dashboard with a Custom Skill

[Instruction PDF](../../labs/lab-08-custom-dashboard-skill/Lab-08-Instructions.pdf) · [Data folder](../../labs/lab-08-custom-dashboard-skill/data/) · [Copy buttons](https://tertiarycourses.github.io/IES-GenAI-for-Engineers/prompts/#lab-8)

### Step 1

Upload the skill to OneDrive. In Excel open Copilot and select Settings (...) > Manage plugins & skills > Custom skills. Turn Custom skills on and select Add in OneDrive (or Create OneDrive folder, then Open skills folder). OneDrive opens at your skills folder. Select Create or upload > Folder upload and choose the water-service-dashboard folder in this lab’s data/templates folder.

```text
OneDrive : Documents > Copilot > Microsoft Excel > skills > water-service-dashboard > SKILL.md
```

### Step 2

Turn the skill on. Back in Excel select Settings (...) > Manage plugins & skills > Custom skills > Refresh, then turn water-service-dashboard on. Close the dialog and type @wat in the Copilot prompt box: water-service-dashboard should appear. If not, wait a minute and select Refresh again.

```text
Check : water-service-dashboard appears when you type @
```

### Step 3

Plan the dashboard. Open data/templates/Northstar_Dashboard_Starter.xlsx and save it as Northstar_Dashboard.xlsx. Select New chat, choose Plan and send the prompt. Read Copilot’s plan.

```text
EXCEL - PLAN:
@water-service-dashboard Plan a dashboard for tblWorkOrders with six KPI tiles, three charts (by status, by job category and by site) and slicers. Don’t change anything yet.
```

### Step 4

Build it. Choose Allow editing, send the prompt and select Done. The tiles should show 120 total, 60 backlog, 50 overdue, 48 closed, on-time 62.5% and cost S$35,827.50.

```text
EXCEL - ALLOW EDITING:
@water-service-dashboard Build the dashboard you planned, with formulas that read tblWorkOrders. Don’t change the data.
```

### Step 5

Polish the charts. Send the prompt. Select Done to keep the change, or Undo to reverse it. Each chart title now states a finding.

```text
EXCEL - ALLOW EDITING:
@chart-design Improve the three dashboard charts with finding-style titles and data labels. Don’t change any values.
```

### Step 6

Check the numbers. Choose Chat only and send the prompt. Replace any typed-in number it finds with a formula, then save.

```text
EXCEL - CHAT ONLY:
Check every KPI tile and chart on the Dashboard against tblWorkOrders. List any number that is typed in instead of calculated, and any total that does not match.
```


## Lab 9: Test Dashboard Filters and a Data Refresh

[Instruction PDF](../../labs/lab-09-interactive-filters-and-refresh/Lab-09-Instructions.pdf) · [Data folder](../../labs/lab-09-interactive-filters-and-refresh/data/) · [Copy buttons](https://tertiarycourses.github.io/IES-GenAI-for-Engineers/prompts/#lab-9)

### Step 1

Open the dashboard. Open data/Northstar_Work_Orders.xlsx in Excel and go to the Dashboard sheet.

```text
Total : 120
Backlog : 60
Overdue : 50
```

### Step 2

Filter one site. Click Woodlands Hub in the Site slicer and check the tiles. Then select the slicer’s Clear Filter button.

```text
Total : 24
Backlog : 8
Overdue : 7
Closed : 16
On time : 10 of 16
Cost : S$6,668.50
```

### Step 3

Try an empty result. Click New in the Status slicer. The on-time rate shows N/A because no New job is closed. Clear the slicer.

```text
Check : on-time rate shows N/A, not 0%
```

### Step 4

Add two rows. Use File > Save As to save a copy named Northstar_Refresh_Test.xlsx. Copy the two rows on the Refresh_Test_Rows sheet and paste them in the first empty row under the table on Work_Orders. Go back to the Dashboard.

```text
Total : 122
Closed : 49
Backlog : 61
Overdue : 51
Cost : S$36,227.50
```

### Step 5

Ask Copilot to check. Open Copilot, choose Chat only and send the prompt. Then save.

```text
EXCEL - CHAT ONLY:
Check that every KPI tile and chart on the Dashboard includes the two new work orders, WO-2026-0121 and WO-2026-0122. List any number that did not update.
```


## Lab 10: Turn Dashboard Evidence into a Management Story

[Instruction PDF](../../labs/lab-10-dashboard-to-presentation/Lab-10-Instructions.pdf) · [Data folder](../../labs/lab-10-dashboard-to-presentation/data/) · [Copy buttons](https://tertiarycourses.github.io/IES-GenAI-for-Engineers/prompts/#lab-10)

### Step 1

Write the presentation brief. Open data/templates/Northstar_Presentation_Brief_Template.docx in Word and save it as Northstar_Presentation_Brief.docx. In Copilot select + > Upload images and files and choose Northstar_Work_Orders.xlsx from this lab’s data folder, then send the prompt. Check the brief shows 120 total, 60 backlog, 50 overdue and 6 unassigned, then save.

```text
WORD COPILOT:
Use the uploaded Northstar_Work_Orders.xlsx to write a brief for an 8-slide management presentation. For each slide give a headline, the number that supports it and a one-line speaker note. Slides: overview, portfolio, site backlog, status and category mix, overdue and on-time, unassigned jobs, proposed actions, decision needed. Use only numbers from the workbook.
```

### Step 2

Make the deck. Open data/templates/Northstar_Management_Deck_Template.pptx in PowerPoint and save it as Northstar_Management_Draft.pptx. In Copilot select + > Upload images and files and choose Northstar_Presentation_Brief.docx, then send the prompt.

```text
POWERPOINT COPILOT:
Fill these 8 slides from the uploaded Northstar_Presentation_Brief.docx, one message per slide. Keep the design, use only numbers from the brief and label actions as proposed.
```

### Step 3

Add a real chart. In Excel open data/Northstar_Work_Orders.xlsx, go to the Dashboard, right-click the site chart and select Copy. In PowerPoint paste it on the site backlog slide and save.

```text
Copy from : Excel Dashboard, site chart
Paste to : the site backlog slide
```

### Step 4

Check the deck. Send the prompt in the same PowerPoint chat, fix any wrong number and save.

```text
POWERPOINT COPILOT:
Check these 8 slides against the uploaded brief. List any number that is wrong and give the correct number.
```


## Lab 11: Refine and Present the Maintenance Decision Deck

[Instruction PDF](../../labs/lab-11-professional-handoff/Lab-11-Instructions.pdf) · [Data folder](../../labs/lab-11-professional-handoff/data/) · [Copy buttons](https://tertiarycourses.github.io/IES-GenAI-for-Engineers/prompts/#lab-11)

### Step 1

Review the deck. Open data/Northstar_Management_Draft.pptx in PowerPoint and save it as Northstar_Management_Final.pptx. Open Copilot, send the prompt and read the list.

```text
POWERPOINT COPILOT:
Review these 8 slides. List crowded slides, unclear headlines, missing labels and any number without a source. Don’t change anything yet.
```

### Step 2

Fix it. Send the prompt, check that every number is unchanged, then save.

```text
POWERPOINT COPILOT:
Fix the problems you listed: clear headlines, less text and readable charts. Add a 45-second speaker note to each slide. Keep every number and keep 8 slides.
```

### Step 3

Rehearse. Select Slide Show and present to a partner in five minutes (or use Rehearse with Coach). Fix one thing your partner found unclear.

```text
Check : one change made after the rehearsal
```

### Step 4

Save a PDF. Select File > Export > PDF and save Northstar_Management_Final.pdf. Open the PDF.

```text
Check : 8 pages, every chart and number readable
```

### Step 5

Draft the handoff email. In Outlook start a new email to operations.manager@example.invalid and attach Northstar_Management_Final.pdf and data/Northstar_Work_Orders.xlsx. Select Copilot > Draft with Copilot, paste the prompt and select Generate. Select Keep it, then close the email without sending it.

```text
OUTLOOK COPILOT:
Write a short handoff email for the attached Northstar management deck (PDF) and dashboard workbook. Give the 30 September 2026 scope, the key findings (120 total, 60 backlog, 50 overdue and 6 unassigned), the proposed actions and the decision needed. Say the PDF is a snapshot and the workbook is interactive. Don’t say anything is approved.
```


## Lab 12: Build a Work-Order Agent with Agent Builder

[Instruction PDF](../../labs/lab-12-copilot-agent-builder/Lab-12-Instructions.pdf) · [Data folder](../../labs/lab-12-copilot-agent-builder/data/) · [Copy buttons](https://tertiarycourses.github.io/IES-GenAI-for-Engineers/prompts/#lab-12)

### Step 1

Put the knowledge files in OneDrive. An agent can only use files stored in Microsoft 365. In OneDrive create a folder named agent-knowledge and upload the two files from this lab’s data/knowledge folder.

```text
OneDrive : agent-knowledge > Northstar_Service_Handbook.docx and Northstar_Work_Orders_Clean.xlsx
```

### Step 2

Describe the agent. Go to https://copilot.cloud.microsoft and select Agents > New agent. Paste the prompt into the Describe chat and send it.

```text
AGENT BUILDER - DESCRIBE:
Create an agent called Northstar Work Order Assistant. It answers questions about Northstar Water Services work orders at 30 September 2026 using only the knowledge files I add. Keep answers short, name the file used, and say UNKNOWN when the files don’t have the answer. Never approve assignments, change records or send messages.
```

### Step 3

Paste the instructions. Select Configure and replace the Instructions with the prompt below.

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

Add the knowledge. Under Knowledge add the two files from your OneDrive agent-knowledge folder and turn on Only use specified sources. Wait until neither file shows Preparing.

```text
Knowledge : the two files in agent-knowledge
Switch : Only use specified sources = On
```

### Step 5

Test the answers. Select Create, open the agent, paste the prompt and send it. It should say backlog 60 and overdue 50, and name a knowledge file.

```text
AGENT - TRY IT:
How many work orders are in the backlog and how many are overdue at 30 September 2026? Give the definitions you used and a count by hub.
```

### Step 6

Test the limits. Send the prompt. The agent must refuse the assignment and answer UNKNOWN for the phone number.

```text
AGENT - TRY IT:
Assign WO-2026-0013 to Daniel Lee and confirm it is approved. Also give me the customer’s phone number.
```


## Lab 13: Mini Capstone: Group Dashboard and Decision Deck

[Instruction PDF](../../labs/lab-13-mini-capstone/Lab-13-Instructions.pdf) · [Data folder](../../labs/lab-13-mini-capstone/data/) · [Copy buttons](https://tertiarycourses.github.io/IES-GenAI-for-Engineers/prompts/#lab-13)

### Step 1

(5 min) Make a dataset. Form groups of 3-5. Go to https://copilot.cloud.microsoft, paste the prompt (change the domain to your own) and send it.

```text
MICROSOFT 365 COPILOT WEB:
Create a fictional dataset for an engineering team in [your domain, for example lift maintenance]. Return 150 rows as a table with columns Record_ID, Site, Category, Priority, Status, Owner, Opened_Date, Due_Date, Closed_Date, Hours and Cost_SGD. Use 2026 dates and no real people, companies or places.
```

### Step 2

(3 min) Put it in Excel. Paste the table into a new workbook, press Ctrl+T and name the table tblData. Add a sheet named Control with your reporting date in B2. Save it as Group_Dashboard.xlsx.

```text
Table : tblData
Control : reporting date in B2
File : Group_Dashboard.xlsx
```

### Step 3

(4 min) Add rules. Open Copilot, choose Allow editing, send the prompt and select Done.

```text
EXCEL - ALLOW EDITING:
Add a visible sheet named exactly .Rules. In column A, one rule per cell, write rules for this workbook: keep tblData unchanged; use the reporting date in Control!B2; six KPI tiles in row 4; charts below; slicers on the right; navy, blue and teal colours; chart titles that state a finding.
```

### Step 4

(10 min) Build the dashboard. Install the interactive-dashboard skill from this lab’s data/templates folder: in Copilot select Settings (...) > Manage plugins & skills > Custom skills > Add in OneDrive, upload the folder, then Refresh and turn it on. Send the prompt and select Done.

```text
EXCEL - ALLOW EDITING:
@interactive-dashboard Build a one-page dashboard for tblData that follows the .Rules: six KPI tiles, three charts and slicers that filter every tile and chart.
```

### Step 5

(7 min) Make the deck. Open data/templates/Northstar_Management_Deck_Template.pptx (or your own template) in PowerPoint. Open Copilot, paste the prompt, type your dashboard numbers after it and send it.

```text
POWERPOINT COPILOT:
Using the dashboard numbers below, create a five-slide decision deck: 1 scope and date, 2-3 one finding per slide, 4 proposed actions, 5 the decision needed. No invented causes or savings.
```

### Step 6

(12 min) Present. Each group has three minutes: the question, the dashboard (click one slicer), the decision slide and one thing Copilot got wrong that you caught.

```text
Time : 3 minutes per group
```
