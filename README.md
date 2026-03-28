# Claude Skill for Systematic Literature Review - PRISMA (slr-prisma)

A Claude skill that walks you through writing a systematic literature review following the PRISMA 2020 framework.

It covers the full 27-item PRISMA 2020 checklist, produces a Word document manuscript section by section, and generates a PRISMA flow diagram. It does not cover meta-analysis or statistical pooling.

## What it does

The skill runs in five phases.

**Phase 1 — Interview.** Gathers your review topic, research questions, databases, eligibility criteria, screening process, quality appraisal tool, synthesis approach, and flow diagram numbers. You can upload existing documents (proposals, protocols, PROSPERO registrations, search logs, data extraction sheets) and the skill will extract what it can, then only ask about whatever is missing.

**Phase 2 — Section-by-section drafting.** Works through the manuscript in order (Title, Abstract, Introduction, Methods, Results, Discussion, Other Information), mapping every section to its PRISMA 2020 checklist items. It pauses after each section for your feedback before moving on. Tone adjusts depending on whether you are a first-time reviewer or an experienced researcher.

**Phase 3 — PRISMA flow diagram.** Selects the correct template (new or updated review, databases only or other sources), confirms the numbers, and builds the diagram as a table inside the Word document.

**Phase 4 — Word document.** Compiles the full manuscript as a .docx with A4 formatting, heading styles, and the flow diagram embedded in the Results section.

**Phase 5 — Checklist audit (optional).** Maps each of the 27 PRISMA items to where it appears in the manuscript, flagging anything missing or incomplete.

It also handles partial requests — just the Methods section, just a flow diagram, just a search strategy, or auditing an existing manuscript against the checklist.

## Installation

Download the `slr-prisma.skill` file from [Releases](../../releases) and install it in Claude (Customise>Skills)
Alternatively, copy the `SKILL.md` and `references/` folder into your Claude skills directory.

## How to Start Using

Enable this skills in Claude. Then whenever you prompt "Peform a literature review on TOPIC" it will begin reading the skill file to assist you. Respond to the questions given to you clearly. This will help enhance accuracy of your review. Happy Trying!

## File structure

```
slr-prisma/
├── SKILL.md                              # Main skill instructions
├── references/
│   ├── prisma-2020-checklist.md          # Full 27-item PRISMA 2020 checklist
│   └── flow-diagram.md                   # Flow diagram templates and guidance
├── LICENSE
└── README.md
```

## PRISMA 2020

This skill is based on the [PRISMA 2020 statement](https://www.prisma-statement.org/prisma-2020) (Page et al., 2021). The checklist and flow diagram templates are distributed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).

> Page MJ, McKenzie JE, Bossuyt PM, Boutron I, Hoffmann TC, Mulrow CD, et al. The PRISMA 2020 statement: an updated guideline for reporting systematic reviews. BMJ 2021;372:n71. doi: 10.1136/bmj.n71

## Licence

The PRISMA 2020 checklist and flow diagram content is licensed under CC BY 4.0 (see above). The skill itself is licensed under the [MIT Licence](LICENSE).
