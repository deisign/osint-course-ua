# The Art of Data Journalism — DataJournalismTutorials

**Author:** Matt Waite  
**Repository:** `The-Art-of-Data-Journalism/DataJournalismTutorials`  
**Checked:** 2026-08-12  
**Audit status:** `PARTIAL-REVIEWED`  
**License:** GPL-3.0

## Why this donor matters

This repository is primarily a **learning-design donor** rather than an OSINT methodology donor. Its strongest contribution is the way technical practice is taught: interactive `learnr` lessons, progressive exercises, immediate checks with `gradethis`, repetition until basic actions become routine, real datasets, and localisation of the same lesson to data close to the student.

Reviewed: project README/curriculum, `DESCRIPTION`, `LICENSE`, and selected tutorials: Data Smells, Janitor, Cleaning Text, Joining, Census/API.

## Key decisions

| Component | Decision | Target in our course |
|---|---|---|
| Data Smells | `ADOPT + EXPAND` | M14 Data Hygiene + analytical discipline |
| Preserve original data; clean into derived fields | `ADOPT` | M14 + transformation logging |
| Text cleaning / clustering | `ADAPT + EXPAND` | L08 Dirty Entities |
| Progressive repetition | `ADOPT` | golden-module learning design |
| Automated formative checks | `REBUILD` | future course shell / micro-practice |
| Localised datasets | `ADAPT + EXPAND` | parametrised regional/synthetic labs |
| Joins | `ADAPT` | datasets, network/data modules |
| APIs through convenient wrappers | `ADAPT` | M16 Automation, then expose request/provenance details |
| R/tidyverse as mandatory core | `REJECT` | optional data specialization only |
| ggplot/Datawrapper-heavy tail | `SELECTIVE` | reporting layer |

## 1. Data Smells

The strongest concept for us. A dataset should be treated as potentially misleading until basic checks are complete: missing data, gaps, wrong data types, outliers, internal inconsistency, disagreement across datasets, wrongly derived values, spatial problems, and inconsistent text.

For our course this becomes a **Data Intake Gate**:

`acquire → preserve raw → profile/smell-check → document weaknesses → clean/normalise → validate → analyse`

No `raw → analysis` jump.

## 2. Preserve the original

The cleaning-text lesson explicitly avoids overwriting the source value and creates a new cleaned field. This maps directly to our evidence-first model:

`raw/reference value → documented transformation → working/derived value`

For M14:

- original value remains intact;
- normalized value is separate;
- transformation rule is logged;
- fuzzy/clustering suggestion is not an automatic merge;
- ambiguous merge decisions require review.

## 3. Cleaning as a logic problem

Waite teaches cleaning as solving the specific inconsistency that prevents answering a research question, not as learning a particular cleaning application.

This reinforces our tool-independent approach: OpenRefine, R, Python or spreadsheet tools are implementations; the competency is identifying and controlling normalization, duplicates, transliteration, fuzzy matches, false merge and false split.

## 4. Progressive micro-practice

The lessons repeatedly use the pattern:

`explain → small exercise → immediate check → repeat → add one complication`

Our golden-module standard should add a denser micro-practice layer before guided and independent labs.

Suggested path:

1. demonstration;
2. hinted micro-exercise;
3. unhinted micro-exercise;
4. guided case;
5. independent lab;
6. capstone transfer.

## 5. Automated formative feedback

`learnr + gradethis` is valuable as a pattern, not as required technology. We should eventually auto-check structural conditions such as:

- schema/required fields;
- unique IDs;
- row counts where meaningful;
- parsed dates;
- raw field preserved;
- cleaned field created;
- chronology consistency;
- hash format;
- allowed status values.

Automated checks must not judge open-ended attribution or analytical conclusions.

## 6. Localised real data

The repository uses a configurable state value so the same lesson runs on locally relevant datasets. For us the transferable idea is **case parametrisation**: one competency and rubric, several regional or synthetic datasets.

This is especially useful for L08 Dirty Entities and later data-heavy labs.

## 7. Curriculum impact

### Strengthen M14

M14 should include:

- raw vs derived data;
- schema inspection;
- data smells;
- completeness and data types;
- duplicates;
- normalization;
- fuzzy matching;
- false merge / false split;
- transliteration;
- cross-dataset consistency;
- transformation log;
- external aggregate validation;
- reproducible cleaning.

### Build L08 Dirty Entities as staged practice

- Phase 1: obvious casing/spacing/date issues;
- Phase 2: spelling/transliteration variants;
- Phase 3: fuzzy suggestions with both correct and dangerous merges;
- Phase 4: cross-dataset join revealing a false merge.

Core rule:

> **automation proposes; investigator decides and documents.**

## 8. Relationship to other donors

Bradshaw helps answer **how to think like an investigator**. Berkeley helps answer **how to collect, preserve, verify and document open-source material professionally**. Waite adds a third layer: **how to design practice so the student actually acquires the technical habit instead of merely understanding the lecture**.

## Remaining review

Before `REVIEWED`:

- fundamentals/dates tutorials;
- spreadsheets;
- deeper join failure modes;
- selected visualization lessons for evidence communication;
- Datawrapper;
- localisation implementation;
- dataset/source documentation;
- update/freshness mechanics.

**Overall value:** very high for pedagogy; high for data hygiene/automation; selective for direct content reuse.