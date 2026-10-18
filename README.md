# GenAI for Engineers

**IES Academy · v2.3 · 18 October 2026**

![GenAI for Engineers slide cover](screenshot.png)

One day with 7.5 instructional hours. Twelve connected labs use the same fictional Northstar Water Services maintenance and service scenario across Excel, Word, PowerPoint, Outlook and Microsoft Copilot, ending with a work-order agent built in Agent Builder and a group mini capstone.

**[Open the copy-ready prompts page →](https://tertiarycourses.github.io/IES-GenAI-for-Engineers/prompts/)** · to download everything, use **Code → Download ZIP** on GitHub.

## Course materials

- [Trainer slides](courseware/GenAI%20for%20Engineers-v2.3.pptx)
- [Slides PDF](courseware/GenAI%20for%20Engineers-v2.3.pdf)
- [Learner Guide Word](courseware/LG-GenAI%20for%20Engineers.docx) · [PDF](courseware/LG-GenAI%20for%20Engineers.pdf) · [Markdown](LG-GenAI%20for%20Engineers.md)
- [Lesson Plan Word](courseware/LP-GenAI%20for%20Engineers.docx) · [PDF](courseware/LP-GenAI%20for%20Engineers.pdf)
- [Copy-ready prompts, step by step (public page)](https://tertiarycourses.github.io/IES-GenAI-for-Engineers/prompts/) · [source](docs/prompts/index.html)
- [Lab folders](labs/)

On the prompts page pick a lab, follow each step and click **Copy** on the prompt under it. Every lab instruction PDF links to its own section of that page (for example `…/prompts/#lab-8`). Each lab folder holds only its instruction PDF and a `data/` folder with the lab workbook, the templates that lab uses and a rejoin checkpoint.

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

All work orders, service hubs and staff are synthetic. Use the fixed reporting date 30 September 2026. Verify every result, retain UNKNOWN for missing evidence, keep proposed assignments separate from current assignments, and leave training email drafts unsent. Capstone groups use only mock or sanitised data.

## Rebuilding

Every artifact is generated from one source in [`.agents/skills/non-wsq-courseware-build/build/`](.agents/skills/non-wsq-courseware-build/build/) (`course_data.py`, the lab modules and `ies_updates.py`). Run `bash build_courseware.sh` there to regenerate the deck, Lesson Plan, Learner Guide, lab folders and prompt page together. Superseded materials are kept in [`archive/`](archive/): v2.2 in `archive/20261018-v2.2-superseded/` and the original package in `archive/20261014-before-c27-replacement/`.
