---
name: slr-prisma
metadata:
  author: Chuah Kee Man
description: "Guide users through writing a systematic literature review (SLR) following the PRISMA 2020 framework. Use this skill whenever the user mentions 'systematic review', 'systematic literature review', 'SLR', 'PRISMA', 'PRISMA 2020', 'PRISMA flow diagram', 'PRISMA checklist', or asks for help writing, structuring, or auditing a literature review that follows reporting guidelines. Also trigger when the user asks about inclusion/exclusion criteria for a review, search strategies for databases like Scopus/WoS/PubMed, study selection processes, risk of bias assessment, or narrative synthesis for a review paper. This skill covers the full PRISMA 2020 checklist (27 items), produces a Word document manuscript, and generates a PRISMA flow diagram. It does NOT cover meta-analysis or statistical pooling."
---

# Systematic Literature Review — PRISMA 2020

This skill walks a user through writing a systematic literature review (SLR) that follows the PRISMA 2020 reporting guideline. It produces a structured Word document (.docx) and a PRISMA flow diagram, working section-by-section with the user.

## Before you begin

Read these reference files as needed:
- `references/prisma-2020-checklist.md` — The full 27-item PRISMA 2020 checklist. Consult this when drafting each section to make sure nothing is missed.
- `references/flow-diagram.md` — PRISMA flow diagram templates and guidance. Consult this when building the flow diagram.

Also read the **docx skill** (`/mnt/skills/public/docx/SKILL.md`) before generating the final Word document, as it contains critical rules for docx-js.

If the user has a **writing-style skill**, apply it to all drafted prose.

---

## Phase 1: Interview

Before any drafting, gather the information needed to write the review. There are two paths into the interview, and the user should be offered both up front.

### Path A: Upload existing documents

The user may already have a proposal, protocol, draft manuscript, PROSPERO registration, data extraction sheet, or search log. At the start of the interview, ask whether they have any documents to share. Common uploads include:

- Research proposal or protocol (often contains RQs, eligibility criteria, databases, and methods)
- PROSPERO registration form
- Draft or partial manuscript
- Search strategy export or search log
- Data extraction spreadsheet (e.g. from Excel, Google Sheets, or Rayyan/Covidence export)
- List of included/excluded studies
- Completed PRISMA checklist from a previous attempt

If the user uploads a document, read it using the appropriate skill (docx skill for .docx, file-reading skill for other formats, pdf-reading skill for PDFs, or xlsx skill for spreadsheets). Extract as much of the essential information (listed below) as possible from the document. Then present a summary of what was extracted and ask the user to confirm, correct, or fill in the gaps.

This saves the user from re-typing information they have already written. Many postgrad students will have a proposal or partial draft — encouraging them to upload it makes the process much faster.

If the user uploads multiple documents, read them all and cross-reference the information. Flag any contradictions (e.g. different inclusion criteria in the proposal vs. the draft).

### Path B: Conversational interview

If the user has no documents to share, or after extracting what is available from uploaded documents, gather the remaining information conversationally. Ask questions in a natural flow, not as a wall of text. Adapt to what the user already provides — skip questions they have already answered.

### Essential information to collect

**About the review itself:**
- Working title
- Research question(s) or objective(s)
- Type of review (e.g. intervention effectiveness, diagnostic accuracy, qualitative, scoping turned systematic, mixed methods)
- Whether this is a new review or an update of a previous one
- Registration status (e.g. PROSPERO number, or not registered)
- Protocol status (published, unpublished, not prepared)

**About the search:**
- Databases searched (e.g. Scopus, Web of Science, PubMed, ERIC, IEEE Xplore, ProQuest)
- Other sources (websites, grey literature, citation searching, hand-searching, expert consultation)
- Date range and date of last search
- Search terms and Boolean strategy (or enough detail to reconstruct one)
- Any filters or limits applied (language, date, document type)

**About eligibility:**
- Inclusion criteria (population, intervention/exposure, comparator, outcome, study design — or the relevant framework like PICo, PICO, SPIDER, etc.)
- Exclusion criteria
- How studies were grouped for synthesis

**About screening and selection:**
- Number of reviewers at each stage
- Whether reviewers worked independently
- How disagreements were resolved
- Any automation tools used (e.g. Rayyan, ASReview, Covidence)

**About data extraction:**
- What data items were extracted (outcomes, variables, study characteristics)
- Data extraction tool or form used
- Number of reviewers, independence, and conflict resolution

**About quality appraisal:**
- Risk of bias tool used (e.g. RoB 2, ROBINS-I, Newcastle-Ottawa Scale, CASP, JBI, MMAT)
- Number of reviewers and independence

**About synthesis:**
- Synthesis approach (narrative synthesis, thematic synthesis, framework synthesis, vote counting, harvest plots, etc.)
- How results will be presented (tables, figures, summary of findings)

**About the numbers (for the flow diagram):**
- Records identified per database/source
- Duplicates removed
- Records screened and excluded
- Full-text reports retrieved and not retrieved
- Full-text reports assessed and excluded (with reasons)
- Final number of included studies

If the user does not have all the numbers yet (common for students mid-process), note which are missing and use placeholder values (n = ?) in the flow diagram. The user can fill these in later.

### How to run the interview

Start by asking the user whether they have any existing documents to share (proposal, protocol, draft, search log, data extraction sheet, etc.). If they do, read the documents first and extract what you can before asking follow-up questions. This avoids making the user repeat themselves.

If no documents are provided, or after processing uploads, work through the remaining gaps conversationally. Start with the big picture (title, RQ, databases) and work through the rest in 2–3 rounds of questions, grouping related items together. Use the ask_user_input tool where options are bounded (e.g. risk of bias tool choice, synthesis approach). Use open questions for things like research questions and search terms.

Once you have enough to begin, confirm the plan with the user before drafting.

---

## Phase 2: Section-by-section drafting

Work through the manuscript one section at a time. After drafting each section, present it to the user and wait for feedback or approval before moving on.

### Section order and PRISMA mapping

Draft sections in this order. The PRISMA item numbers in brackets show which checklist items each section addresses.

1. **Title** [Item 1]
2. **Abstract** [Item 2]
3. **Introduction**
   - Rationale [Item 3]
   - Objectives [Item 4]
4. **Methods**
   - Eligibility criteria [Item 5]
   - Information sources [Item 6]
   - Search strategy [Item 7]
   - Selection process [Item 8]
   - Data collection process [Item 9]
   - Data items [Items 10a, 10b]
   - Study risk of bias assessment [Item 11]
   - Effect measures [Item 12] (if applicable; skip for purely qualitative reviews)
   - Synthesis methods [Items 13a–13f]
   - Reporting bias assessment [Item 14]
   - Certainty assessment [Item 15]
5. **Results**
   - Study selection and PRISMA flow diagram [Items 16a, 16b]
   - Study characteristics [Item 17]
   - Risk of bias in studies [Item 18]
   - Results of individual studies [Item 19]
   - Results of syntheses [Items 20a–20d]
   - Reporting biases [Item 21]
   - Certainty of evidence [Item 22]
6. **Discussion**
   - Interpretation [Item 23a]
   - Limitations of evidence [Item 23b]
   - Limitations of review process [Item 23c]
   - Implications [Item 23d]
7. **Other information**
   - Registration and protocol [Items 24a–24c]
   - Support [Item 25]
   - Competing interests [Item 26]
   - Data availability [Item 27]

### Drafting guidance

**For postgraduate students (first-time reviewers):**
- Explain what each section needs to achieve before drafting it
- Flag common mistakes (e.g. writing eligibility criteria as a vague narrative instead of explicit include/exclude lists)
- Offer brief rationale for why PRISMA requires certain details (transparency and reproducibility)

**For experienced researchers:**
- Skip the explanations and draft directly
- Focus on completeness and precision

**Tone calibration:**
- If the user seems unsure or asks basic questions, lean towards the student-friendly approach
- If they provide detailed methodological input unprompted, treat them as experienced
- When in doubt, briefly explain and offer to skip explanations ("I can walk you through what this section needs, or just draft it directly — your call")

### Section-specific notes

**Title [Item 1]:** The title must identify the report as a systematic review. Common format: "A systematic review of [topic]" or "[Topic]: A systematic review".

**Abstract [Item 2]:** Use the PRISMA 2020 for Abstracts structure. For journals requiring structured abstracts, include: Background, Objectives, Data Sources, Study Eligibility Criteria, Participants and Interventions, Appraisal and Synthesis Methods, Results, Limitations, Conclusions, Registration. Draft this last (after the full manuscript), even though it appears first in the document.

**Search strategy [Item 7]:** Present the full Boolean search string for at least the primary database. If the user provides keywords but not a Boolean string, help them construct one. Common format: (Term1 OR Synonym1 OR Synonym2) AND (Term2 OR Synonym3) AND (Term3 OR Synonym4).

**PRISMA flow diagram [Item 16a]:** Read `references/flow-diagram.md` to select the correct template. Build the flow diagram as a table in the Word document (see "Generating the Word Document" below).

**Study characteristics [Item 17]:** Typically presented as a table (author, year, country, study design, population, intervention/exposure, outcome, key findings). If the user provides a data extraction spreadsheet or list of included studies, use it to populate this table.

**Synthesis [Items 13a–f, 20a–d]:** Since this skill covers narrative synthesis only (not meta-analysis), guide the user through describing how studies were grouped, compared, and synthesised narratively. If the user mentions wanting to do meta-analysis, let them know this skill focuses on the narrative review and suggest they consult meta-analysis-specific guidance separately.

---

## Phase 3: PRISMA flow diagram

After drafting the Results section (specifically Item 16a), generate the PRISMA flow diagram.

1. Read `references/flow-diagram.md` to determine which template applies.
2. Confirm the numbers with the user (or use placeholders).
3. Build the flow diagram as a table within the Word document.

The flow diagram table should have:
- Three phases as shaded header rows: **Identification**, **Screening**, **Included**
- Boxes for each step, with record/report/study counts
- Exclusion reasons listed where applicable
- If Template B or D (other sources), use a two-column layout to show parallel streams

---

## Phase 4: Generate the Word document

Once all sections are drafted and approved, compile the full manuscript into a .docx file.

### Document structure

Read the **docx skill** before generating the document. Key points:
- Use `npm install -g docx` and docx-js to create the file
- Use A4 page size (11906 × 16838 DXA) since the user is in a Malaysian academic context
- Set 1-inch margins (1440 DXA on all sides)
- Use Times New Roman or Arial, 12pt body text, with standard academic formatting
- Include a Table of Contents
- Use Heading1 for main sections (Introduction, Methods, Results, Discussion), Heading2 for subsections
- Number sections if the user or their institution requires it
- Place the PRISMA flow diagram in the Results section as a formatted table
- Include the study characteristics table and any other tables in the appropriate sections
- Add page numbers in the footer

### After generating

1. Validate the document: `python scripts/office/validate.py doc.docx`
2. Copy to `/mnt/user-data/outputs/` and present to the user
3. Offer to generate a separate filled PRISMA checklist document if the user wants one (a table mapping each item number to the page/section where it is reported)

---

## Phase 5: PRISMA checklist audit (optional)

If the user asks for a checklist audit, or after the manuscript is complete, offer to produce a filled PRISMA 2020 checklist. This is a table with three columns:

| Item # | Checklist item | Reported on page/section |

Read `references/prisma-2020-checklist.md` and map each of the 27 items to where it appears in the manuscript. Flag any items that are missing or incomplete so the user can address them.

This can be produced as a separate Word document or appended to the manuscript.

---

## Handling partial requests

Not every user will want the full pipeline. Common partial requests and how to handle them:

- **"Help me write my Methods section"** — Run a targeted interview for Methods-related info only, then draft the Methods subsections with PRISMA items 5–15.
- **"Create a PRISMA flow diagram"** — Ask for the numbers, select the right template, and generate the diagram in a Word doc.
- **"Check my SLR against PRISMA"** — Ask the user to upload their manuscript (or paste the text), read it using the appropriate file-reading skill, then audit it against the 27-item checklist and report which items are missing or incomplete.
- **"Help me build a search strategy"** — Interview about topic, databases, and terms, then construct Boolean search strings.
- **"I just need the Results section"** — Gather the relevant data (included studies, synthesis findings, flow diagram numbers) and draft Results with items 16–22.

Always anchor partial work to the relevant PRISMA items so the user knows which parts of the checklist they are addressing.

---

## Important reminders

- PRISMA is a **reporting** guideline, not a **conduct** guideline. It tells you what to report, not how to do the review. If the user needs methodological guidance (e.g. how to actually screen studies), help them, but be clear about the distinction.
- The 2020 version supersedes the original 2009 PRISMA statement. If the user references the old version, gently steer them to PRISMA 2020.
- PRISMA 2020 is primarily designed for reviews of interventions. For other types (scoping reviews, diagnostic test accuracy, network meta-analysis, etc.), there are PRISMA extensions. If the user's review type clearly falls under an extension, mention it and offer to adapt the guidance. But for most SLRs in social science, education, and health, the main PRISMA 2020 checklist is appropriate.
- Not every item applies to every review. Qualitative or mixed-methods reviews may skip or adapt items like Effect Measures (12) or statistical synthesis (13d, 20b). Help the user identify which items are relevant and which can be marked "Not applicable".
