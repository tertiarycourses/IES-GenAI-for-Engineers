# IES GenAI for Engineers — alignment matrix

The supplied Lesson Plan controls the sequence, time boxes, outcomes and named activities.

| Module | Time | PPT | Learning outcomes | Named activities |
|---|---|---:|---|---|
| 1 · Copilot ecosystem | 09:00–10:00 | 5–25 | LO2, LO3 | 1.1 Access; 1.2 AI versus Engineer |
| 2 · Prompting | 10:00–11:15 | 26–55 | LO2, LO3 | 2.1 Specification; 2.2 Report; 2.3 Risk/method |
| 3 · Methodologies | 11:30–13:00 | 56–94 | LO1, LO2, LO3 | 3.1 FMEA; 3.2 DMAIC with SPC/Cp-Cpk; 3.3 Specification pack |
| 4 · Agents | 14:00–15:15 | 95–124 | LO4, LO5 | 4.1 FMEA Agent; 4.2 Report Writer; 4.3 Minutes chain; 4.4 Researcher/Analyst |
| 5 · SharePoint | 15:30–16:15 | 125–143 | LO6 | 5.1 Knowledge agent; 5.2 Grounded chain |
| 6 · Security | 16:15–16:45 | 144–156 | LO7 | 6.1 Seven-step review; 6.2 Toolkit |
| Close | 16:45–17:00 | 157–162 | LO1–LO7 | Outcome check and action |
| Reference | after class | 163–186 | reference | Framework, method, prompt and security aids |

## Concept-to-application sequence

| Concept | Explain first | Copilot application | Independent evidence |
|---|---|---|---|
| FMEA | Function, failure mode, effect, cause, control, S/O/D, RPN and severity gate | Excel table and FMEA Agent | FM01 RPN = 140; FM04 Severity = 9 |
| DMAIC | Define, Measure, Analyse, Improve, Control; Pareto, fishbone and 5-Whys | Excel analysis and report draft | Baseline 9.0%; pilot 3.5%; no causal claim |
| SPC | Time-ordered chart, common/special cause, control/specification limits, Cp/Cpk | Excel formulas, flags and chart | T10 = 59.4 L/h versus fixed LCL |
| Prompt engineering | Benefits, RISE, E-MAP, constraints, personas, debate and iteration | Word, Excel, PowerPoint and agent prompts | Source, formula/citation, unknowns and acceptance test |

Each PPT slide carries an LO tag, a LIVE or REFERENCE route tag, and a technical-anchor classification in `build/slides.json`. All 16 activity folders use the same Frame → Plan → Generate → Inspect → Verify → Correct → Commit workflow.
