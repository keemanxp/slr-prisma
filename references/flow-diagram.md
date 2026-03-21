# PRISMA 2020 Flow Diagram Reference

The PRISMA flow diagram maps the flow of information through a systematic review: records identified, screened, assessed for eligibility, included, and excluded (with reasons).

There are four official templates. Choose based on two questions:
1. Is this a **new** or **updated** review?
2. Did the search include **databases/registers only**, or also **other sources** (websites, citation searching, grey literature, organisations)?

---

## Template Selection

| Review type | Sources | Template |
|-------------|---------|----------|
| New | Databases and registers only | Template A |
| New | Databases, registers, and other sources | Template B |
| Updated | Databases and registers only | Template C |
| Updated | Databases, registers, and other sources | Template D |

Most student and first-time SLRs use **Template A** or **Template B**.

---

## Template A: New review, databases and registers only

```
IDENTIFICATION
  Records identified from databases (n = ?)
  Records identified from registers (n = ?)
  Records removed before screening:
    Duplicate records (n = ?)
    Records marked as ineligible by automation tools (n = ?)
    Records removed for other reasons (n = ?)

SCREENING
  Records screened (n = ?)
  Records excluded (n = ?)
  Reports sought for retrieval (n = ?)
  Reports not retrieved (n = ?)
  Reports assessed for eligibility (n = ?)
  Reports excluded, with reasons:
    Reason 1 (n = ?)
    Reason 2 (n = ?)
    Reason 3 (n = ?)
    etc.

INCLUDED
  Studies included in review (n = ?)
  Reports of included studies (n = ?)
```

## Template B: New review, databases, registers, and other sources

Same as Template A, but adds a parallel column:

```
IDENTIFICATION (Other methods)
  Records identified from:
    Websites (n = ?)
    Organisations (n = ?)
    Citation searching (n = ?)
    etc.
  Reports sought for retrieval (n = ?)
  Reports not retrieved (n = ?)
  Reports assessed for eligibility (n = ?)
  Reports excluded, with reasons:
    Reason 1 (n = ?)
    Reason 2 (n = ?)
    etc.
```

Both streams merge at "Studies included in review".

## Template C & D: Updated reviews

Same structure as A and B respectively, but add a third stream at the top:

```
IDENTIFICATION (Previous studies)
  Studies included in previous version of review (n = ?)
  Reports of studies included in previous version of review (n = ?)
```

These feed into screening alongside the new search results.

---

## Generating the Flow Diagram in a Word Document

When producing the PRISMA flow diagram inside a .docx file, build it as a structured table using docx-js. The diagram should use:

- A table-based layout with merged cells to represent the flow
- Clear box borders for each stage
- Arrow indicators between stages (use → or ↓ text within cells, or downward-pointing text)
- Shaded header rows for each phase (Identification, Screening, Included)
- Placeholder values (n = ?) that the user fills in with their actual numbers

The flow diagram should be placed in the Results section of the manuscript, alongside the narrative description of the selection process (PRISMA item 16a).

---

## Notes

- The "n" values represent counts of records, reports, or studies at each stage. Records ≠ reports ≠ studies (one study may have multiple reports, one report may describe multiple studies).
- "Records" = a title or abstract (or both) of a report indexed in a database or register.
- "Reports" = a document (journal article, preprint, conference abstract, book chapter, etc.) supplying information about a study.
- "Studies" = an investigation (e.g. a clinical trial, observational study) that may be reported in one or more reports.

Source: Page MJ et al. (2021). Licensed under CC BY 4.0.
