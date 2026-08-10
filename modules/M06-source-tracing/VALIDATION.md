# M06 Internal Validation Record

**Date:** 2026-08-10  
**Module:** M06 — Search Strategy, Source Tracing & Provenance Chains  
**Status after check:** `CONTENT-COMPLETE DRAFT`  
**Independent human pilot:** NOT YET COMPLETED

---

## 1. Structural completeness

Confirmed present in repository:

- [x] module entrypoint / README;
- [x] 9 substantive lesson chapters;
- [x] 12-case casebook;
- [x] staged guided exercise task;
- [x] phase-1 dataset;
- [x] phase-2 dataset;
- [x] guided instructor solution;
- [x] 20-question knowledge check;
- [x] answer key;
- [x] reference sheet;
- [x] common-errors/remediation guide;
- [x] sources/freshness dossier;
- [x] instructor guide;
- [x] independent assessment link to L03.

---

## 2. Learning-path check

The authored path now implements:

```text
concept
→ role separation
→ propagation models
→ search strategy
→ platform/archive/media specifics
→ circularity
→ confidence/limitations
→ micro-cases
→ guided practice
→ knowledge check
→ independent lab
```

This satisfies the intended progression from explanation to supported practice to independent performance.

---

## 3. Methodology consistency check

Checked against project standard:

- [x] observation / inference / conclusion separated;
- [x] earliest-known ≠ creator rule consistent throughout;
- [x] provenance graph edges require basis;
- [x] common-upstream alternatives taught;
- [x] publication count ≠ independent origin count;
- [x] media provenance separated from claim provenance;
- [x] hash interpretation bounded;
- [x] deletion not treated as motive evidence;
- [x] edit states version-preserved;
- [x] archive capture ≠ publication time;
- [x] confidence assigned per claim;
- [x] `unknown / insufficient` treated as valid outcome.

---

## 4. Self-audit issue found and fixed

### Issue

Initial guided-exercise phase 2 used one generic `time` field for an archived web object. This risked teaching exactly the mistake M06 warns against: conflating publication time with archive capture time.

### Fix

Datasets now separate:

- `publication_time`;
- `archive_capture_time`;
- `time_basis`.

For record E:

- page claims publication at 07:51;
- archive capture proves that state existed by 08:02.

Instructor solution explicitly requires students to keep those evidence claims separate.

### Result

PASS after correction.

---

## 5. Current external-source validation

Checked 2026-08-10:

### Telegram primary documentation

- FAQ;
- API message object;
- TDLib forward-info / copy-related behaviour;
- Bot API message fields.

Teaching implication confirmed:

- explicit forward metadata can be provenance evidence;
- absence of forward reference cannot prove independent creation;
- edit/deletion behaviour must be treated as version/availability evidence, not motive evidence.

### Internet Archive primary documentation

Teaching implication confirmed:

- archive capture time is not publication time;
- archive coverage is incomplete;
- missing capture is not proof of non-existence;
- Save Page Now is scoped and may not preserve all dynamic context.

---

## 6. Known gaps before pilot-ready

- [ ] independent human learner run;
- [ ] measured time per lesson/exercise;
- [ ] terminology comprehension test with Ukrainian-speaking learners;
- [ ] check whether mixed Ukrainian/English professional terminology creates unnecessary friction;
- [ ] observe whether 9 chapters should be regrouped into shorter learning units;
- [ ] test knowledge-check difficulty and distractors;
- [ ] test L03 rubric inter-reviewer agreement;
- [ ] validate optional live-demo tools immediately before cohort.

---

## 7. Known design decision

M06 intentionally does **not** depend on live Telegram scraping/search or one specific OSINT service for assessment.

Live tools may be demonstrated, but core competency is evaluated on controlled synthetic material so platform outages, access differences or commercial-tool changes do not invalidate assessment.

---

## 8. Readiness statement

M06 is no longer a skeleton. It is an authored, internally self-consistent **content-complete draft** suitable for an independent human usability/learning pilot.

It must not be labelled `PILOT-READY` or `VALIDATED` until that independent run is completed and the resulting fixes are applied.