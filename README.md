# GenAI for Engineers

**IES Academy · v2.4 · 19 October 2026**

![GenAI for Engineers slide cover](screenshot.png)

One day with 7.5 instructional hours. Twelve connected labs use the same fictional Northstar Water Services maintenance and service scenario across Excel, Word, PowerPoint, Outlook and Microsoft Copilot, ending with a work-order agent built in Agent Builder and a group mini capstone.

**[Open the copy-ready prompts page →](https://tertiarycourses.github.io/IES-GenAI-for-Engineers/prompts/)** · to download everything, use **Code → Download ZIP** on GitHub.

## Course materials

- [Trainer slides](courseware/GenAI%20for%20Engineers-v2.4.pptx)
- [Slides PDF](courseware/GenAI%20for%20Engineers-v2.4.pdf)
- [Learner Guide Word](courseware/LG-GenAI%20for%20Engineers.docx) · [PDF](courseware/LG-GenAI%20for%20Engineers.pdf) · [Markdown](LG-GenAI%20for%20Engineers.md)
- [Lesson Plan Word](courseware/LP-GenAI%20for%20Engineers.docx) · [PDF](courseware/LP-GenAI%20for%20Engineers.pdf)
- [Copy-ready prompts, step by step (public page)](https://tertiarycourses.github.io/IES-GenAI-for-Engineers/prompts/) · [source](docs/prompts/index.html)
- [Lab folders](labs/)

On the prompts page pick a lab, follow each step and click **Copy** on the prompt under it. Every lab instruction PDF links to its own section of that page (for example `…/prompts/#lab-8`). Every lab is self-contained: its folder holds the instruction PDF and a `data/` folder with every file that lab needs, so you can start any lab without finishing the one before. Open the files straight from the lab's `data/` folder and save new files in the same folder; there is no extra working folder and nothing to copy. Steps are short, with one prompt each and the exact numbers you should see. All Excel work runs in desktop Excel on local files, with no OneDrive upload. OneDrive is used only for the Excel custom Skills folder and the Lab 11 agent knowledge files. In Lab 11 you compress the supplied `work-order-qa` Skill folder into a .zip yourself before uploading it to Agent Builder.

| Lab | Topic | Lab | Topic |
|---|---|---|---|
| 1 · Excel to Word | 1 | 7 · Custom Dashboard Skill | 3 |
| 2 · Word to PowerPoint and Outlook | 1 | 8 · Interactive Filters and Refresh | 3 |
| 3 · Personalisation | 2 | 9 · Dashboard to Presentation | 4 |
| 4 · Workbook .Rules | 2 | 10 · Professional Handoff | 4 |
| 5 · Built-in chart skill + custom Pareto Skill | 2 | 11 · Copilot Agent Builder | 5 |
| 6 · Reporting Skill | 2 | 12 · Mini Capstone (groups) | 5 |

## Topics

1. Fundamentals of Microsoft 365 Copilot — Labs 1–2.
2. Personalisation, .Rules and Skills for Excel — Labs 3–6.
3. Interactive Dashboards with Custom Skills — Labs 7–8.
4. Create a Professional Presentation with PowerPoint Copilot — Labs 9–10.
5. Copilot Agents and Mini Capstone — Lab 11 (Agent Builder) and Lab 12 (group capstone).

The course closes with the **5 Principles of AI Security**: data control, permission control, human in the loop, traceability, and well-tested models.

All work orders, service hubs and staff are synthetic. Use the fixed reporting date 30 September 2026. Verify every result, retain UNKNOWN for missing evidence, keep proposed assignments separate from current assignments, and leave training email drafts unsent. Capstone groups use only mock or sanitised data.

## Rebuilding

Every artifact is generated from one source in [`.agents/skills/non-wsq-courseware-build/build/`](.agents/skills/non-wsq-courseware-build/build/) (`course_data.py`, the lab modules, `ies_updates.py` and `simple_labs.py`, which holds the short lab steps). Run `bash build_courseware.sh` there to regenerate the deck, Lesson Plan, Learner Guide, lab folders and prompt page together. Superseded materials are kept in [`archive/`](archive/): v2.3 in `archive/20261019-v2.3-superseded/`, v2.2 in `archive/20261018-v2.2-superseded/` and the original package in `archive/20261014-before-c27-replacement/`.
