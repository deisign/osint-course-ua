# M06 — Search Strategy, Source Tracing & Provenance Chains

**Статус:** `CONTENT-COMPLETE DRAFT`  
**Phase:** Search & Verification  
**Competencies:** C04, C05; supports C13  
**Primary lab:** `labs/L03-telegram-source-tracing/`  
**Standard:** `standards/osint-investigation-standard-v0.1.md`  
**Platform-specific content checked:** 2026-08-10

---

## 1. Навіщо цей модуль

Модуль навчає відповідати не на питання:

> «Де я це побачив?»

а на питання:

> «Яке найраніше доступне джерело конкретного material/claim я можу встановити, як він поширювався, які relationships observed, які inferred, і що залишається unknown?»

Source tracing — це не гонка за найстарішим timestamp. Це **reconstruction provenance chain** із чіткими межами доказової сили.

Після модуля студент має стати повільнішим у категоричних attribution claims, але швидшим у структурованому описі uncertainty.

---

## 2. Learning outcomes

Після модуля студент здатний:

1. відрізняти creator, uploader, publisher, republisher і source-for-later-publisher;
2. уточнювати `source of what?` для publication, media, caption і claim;
3. будувати відтворювану search strategy;
4. знаходити earliest known available source без перетворення його на creator;
5. розрізняти explicit provenance і inferred copying;
6. будувати provenance graph із `observed / inferred / unknown` edges;
7. виявляти circular reporting і рахувати independent origins;
8. розділяти media lineage та claim lineage;
9. працювати з edits/deletions/archive captures як versioned observations;
10. коректно трактувати hash, watermark, crop/transcode та інші media clues;
11. переглядати стару модель при появі нового earlier evidence;
12. формулювати bounded conclusion з confidence, alternatives і limitations.

Target level: C04 → L3; C05 reinforcement.

---

# 3. Student path

## Core lessons

1. [`01-why-provenance-matters.md`](01-why-provenance-matters.md) — знахідка vs походження; publication/media/claim objects.
2. [`02-source-roles.md`](02-source-roles.md) — creator/uploader/publisher/republisher roles.
3. [`03-propagation-models.md`](03-propagation-models.md) — observed/inferred/unknown edges, common upstream.
4. [`04-search-strategy.md`](04-search-strategy.md) — fingerprints, search ladder, search log, stop conditions.
5. [`05-telegram-specifics.md`](05-telegram-specifics.md) — Telegram forward/copy/edit/delete provenance signals and gaps.
6. [`06-web-and-archives.md`](06-web-and-archives.md) — archive captures, mirrors, web version history.
7. [`07-media-provenance.md`](07-media-provenance.md) — byte identity, derived copies, media vs claim timelines.
8. [`08-circular-reporting.md`](08-circular-reporting.md) — publication count vs independent evidence origins.
9. [`09-confidence-and-limitations.md`](09-confidence-and-limitations.md) — bounded conclusions and calibrated confidence.

## Examples

[`examples/casebook.md`](examples/casebook.md) — 12 synthetic micro-cases.

For every mini-case use four questions:

1. What is **observed**?
2. What is **inferred**?
3. What remains **unknown**?
4. What **overclaim** must be avoided?

## Guided practice

[`guided-exercise/task.md`](guided-exercise/task.md)

Two-phase exercise. Student first builds a plausible provenance graph, then receives an earlier archive record and must revise the model rather than defend the original hypothesis.

Instructor solution:

`guided-exercise/solution.md`

## Knowledge check

- [`knowledge-check/questions.md`](knowledge-check/questions.md)
- `knowledge-check/answer-key.md` — instructor-only before completion.

20 questions test concepts independently of tool proficiency.

## Field aids

- [`reference-sheet.md`](reference-sheet.md) — concise operational checklist;
- [`common-errors.md`](common-errors.md) — 20 common failure modes + remediation.

## Independent assessment

`labs/L03-telegram-source-tracing/`

Student independently reconstructs a synthetic Telegram provenance chain including:

- earlier publication;
- manual copy;
- explicit forwards;
- material edit;
- deletion event;
- derived media;
- web mirror.

---

# 4. Core reasoning model

```text
received claim/media
→ define object: publication / media / claim
→ inventory fingerprints
→ search current + earlier states
→ preserve relevant objects
→ build timeline
→ classify propagation edges
→ separate media and claim provenance
→ collapse circular sources
→ test common-upstream alternatives
→ revise model when new evidence appears
→ state earliest-known + confidence + limitations
```

---

# 5. The five identities students must not collapse

For one item, different entities may be:

- **Creator** — produced primary content;
- **Uploader** — uploaded a specific copy;
- **Publisher** — presented material to an audience and added context;
- **Source for later publisher** — actual upstream relationship for a downstream publication;
- **Earliest known available publisher** — earliest publication established within the current research scope.

These roles may coincide, but coincidence must be supported rather than assumed.

---

# 6. Critical professional rules

1. Earliest timestamp ≠ creator.
2. Same SHA-256 ≠ direct transmission.
3. Different hash ≠ unrelated media.
4. Same wording ≠ observed copy relationship.
5. No forward marker ≠ independent origin.
6. Deleted ≠ deceptive/guilty.
7. Archive capture time ≠ publication time.
8. Five publications ≠ five independent confirmations.
9. Watermark ≠ authorship.
10. `Verified` must name the specific verified claim.
11. New evidence must be allowed to lower confidence in old conclusions.
12. `Unknown / insufficient` is a valid professional result.

---

# 7. Assessment philosophy

Technical complexity does not compensate for overclaiming.

A student who uses CSV/Markdown and correctly preserves uncertainty should score higher than a student who builds sophisticated graphs/scripts but calls an earliest uploader the creator.

Critical failures include systematic collapse of:

- uploader → creator;
- chronology → direction;
- repetition → corroboration;
- deletion → motive;
- search scope → universal absence.

---

# 8. Sources and freshness

See [`sources.md`](sources.md).

Current primary platform/service documentation checked on 2026-08-10:

- Telegram official FAQ/API/TDLib;
- Internet Archive / Wayback Machine official Help Center.

Practitioner donor:

- Bellingcat social-media verification guidance.

Stable abstractions must remain teachable even if a particular search/archive UI changes.

---

# 9. Instructor material

[`instructor-guide.md`](instructor-guide.md)

Includes:

- recommended learning sequence;
- provisional timing;
- pre/post diagnostic;
- guided exercise facilitation;
- L03 debrief;
- critical misconceptions;
- grading philosophy;
- safety rules;
- platform freshness check;
- pilot protocol.

---

# 10. Status

M06 is now **content-complete as a first authored draft**, not merely a curriculum skeleton.

Completed:

- [x] 9 substantive lesson chapters;
- [x] 12-case micro-casebook;
- [x] staged guided exercise + solution;
- [x] 20-question knowledge check + answer key;
- [x] reference sheet;
- [x] common-errors/remediation guide;
- [x] source dossier/freshness policy;
- [x] instructor guide;
- [x] independent synthetic lab L03;
- [x] current primary Telegram/Wayback documentation checked.

Still required before `PILOT-READY`:

- [ ] independent human run without oral hints;
- [ ] measured completion time;
- [ ] wording/usability fixes from tester;
- [ ] final reviewer grading pass;
- [ ] optional current live-demo tool set validated.

This module is the **golden-module candidate** for defining the quality bar of the rest of the course.