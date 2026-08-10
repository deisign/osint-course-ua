# M06 Instructor Guide — Source Tracing & Provenance Chains

**Module status:** content-complete draft candidate  
**Primary assessment:** L03 Telegram Source Tracing  
**Prerequisites:** M01–M05 concepts, especially claim/evidence distinction and preservation basics.

---

# 1. What this module is really teaching

The visible topic is source tracing.

The deeper professional habit is:

> **do not collapse observation, inference and conclusion into one mental step.**

A student can know reverse search, Telegram, archives and hashes and still fail this module if they routinely turn:

- earliest → original;
- uploader → creator;
- repetition → corroboration;
- deletion → motive;
- similarity → transmission;
- search failure → non-existence.

Therefore grade reasoning discipline above tool fluency.

---

# 2. Suggested learning sequence

## Block A — Concepts

1. `01-why-provenance-matters.md`
2. `02-source-roles.md`
3. E01–E04 from casebook

Goal: separate object/role claims.

## Block B — Propagation

4. `03-propagation-models.md`
5. `08-circular-reporting.md`
6. E03, E10, E12

Goal: distinguish edges and origin counts.

## Block C — Discovery

7. `04-search-strategy.md`
8. `06-web-and-archives.md`
9. `07-media-provenance.md`
10. relevant casebook examples

Goal: trace earlier states without overstating completeness.

## Block D — Platform

11. `05-telegram-specifics.md`

Goal: understand current Telegram provenance signals and gaps.

## Block E — Calibration

12. `09-confidence-and-limitations.md`
13. knowledge check

Goal: bounded conclusions.

## Block F — Practice

14. guided exercise phase 1
15. freeze result
16. guided exercise phase 2
17. discussion
18. independent L03

---

# 3. Timing — provisional

Do not treat these as final until a human pilot.

| Activity | Target |
|---|---:|
| Concept reading/discussion | 60–90 min |
| Casebook discussion | 45–60 min |
| Search/archive/media lessons | 60–90 min |
| Telegram-specific lesson | 30–45 min |
| Guided exercise | 45–60 min |
| Knowledge check | 25–35 min |
| L03 independent lab | 75–120 min |
| Debrief | 30–45 min |

Expected total: roughly 6–8 hours including independent work.

This is a hypothesis pending pilot measurement.

---

# 4. Pre-module diagnostic

Before teaching, give these three questions without explanation:

### Q1

A posted a video 5 minutes before B. Who is original source?

### Q2

Five media outlets repeat one Telegram claim. How many sources confirm it?

### Q3

A post was deleted after criticism. What does that prove?

Record exact answers.

The same questions can be repeated after module completion to test conceptual change.

---

# 5. Do not rescue the student too early

In the guided exercise, students should be allowed to make the plausible initial inference `A→B`.

Do not immediately correct it.

The educational value comes when phase 2 introduces E and forces revision.

The key observation is not whether phase-1 hypothesis was wrong. It is whether student can:

- preserve original reasoning;
- revise confidence;
- abandon an attractive model;
- leave gaps unresolved.

---

# 6. Questions instructor should ask

Instead of saying «wrong», use:

- «What exactly does this timestamp establish?»
- «What evidence establishes direction?»
- «Could both have a common upstream?»
- «Are you proving creator or uploader?»
- «Does this outlet add new evidence?»
- «What would change your confidence?»
- «What do you still not know?»
- «How would another researcher reproduce this edge?»

These questions model peer review.

---

# 7. Critical misconceptions

The following require explicit correction before passing the module:

1. earliest timestamp = creator;
2. uploader = creator;
3. same hash = direct transmission;
4. no forward marker = independent source;
5. publication count = independent corroboration;
6. archive capture = publication time;
7. deleted = guilty/deceptive;
8. current edited state = full historical state;
9. search failure = absolute absence;
10. `verified` without a defined claim.

---

# 8. Grading philosophy

A technically sophisticated submission should fail if it overclaims.

A simpler submission can pass strongly if it:

- preserves provenance;
- labels uncertainty;
- separates observed/inferred;
- revises hypotheses;
- states bounded conclusion;
- is reproducible.

### Example

Student A uses scripts, graph software and perceptual hashing but calls earliest uploader the creator.

Student B uses CSV/Markdown, leaves creator unknown and documents all edges correctly.

**Student B should score higher.**

---

# 9. L03 grading priorities

Use lab rubric, but pay special attention to:

## Critical

- earliest-known vs creator separation;
- edit/deletion history;
- explicit vs inferred edges;
- media transformation relationship;
- bounded conclusion.

## Secondary

- visual polish of graph;
- tool choice;
- automation sophistication.

Tool complexity is not a learning outcome of M06.

---

# 10. How to debrief L03

Do not start by showing the instructor solution.

Recommended order:

1. Ask 2–3 students for earliest known source.
2. Ask «who is creator?» separately.
3. Put all proposed edges on board.
4. Ask each edge author for basis.
5. Reclassify collectively observed/inferred/unknown.
6. Count publications vs independent origins.
7. Review edit/deletion effect.
8. Only then reveal/compare instructor solution.

The disagreement itself is useful teaching data.

---

# 11. Live-tool demonstrations

Controlled assessment should not depend on live tools.

Optional live demonstration may use current:

- search engines;
- reverse visual search;
- Wayback Machine;
- public Telegram interfaces/API-derived observations where lawful and appropriate.

Before delivery:

- recheck tool availability;
- use non-sensitive demonstration target;
- have screenshots/recorded backup;
- never make module completion dependent on one commercial service.

---

# 12. Safety and ethics

M06 can be taught entirely on synthetic/public benign material.

Do not use beginner exercises that require:

- contacting subjects;
- joining hostile/private groups;
- impersonation;
- doxxing;
- downloading suspicious executables;
- probing systems;
- identifying a private person from weak clues.

Those activities are not needed to teach provenance.

---

# 13. Platform freshness check

Before every cohort, review `sources.md` and specifically verify:

- Telegram forward/copy model;
- edit/delete fields and user-visible signals;
- Wayback save/search limitations;
- any optional live search tools.

Update the `checked` date in platform-specific lessons.

If behaviour is uncertain, teach the stable abstraction and mark platform detail as uncertain.

---

# 14. Independent human pilot protocol

The first tester should receive:

- module README/navigation;
- lessons;
- casebook;
- guided exercise;
- reference sheet;
- L03.

They should **not** receive:

- answer key before knowledge check;
- guided solution before completing phase 2;
- L03 instructor solution;
- oral clarifications during first run.

Collect:

- completion time per component;
- questions asked;
- places reread;
- terms misunderstood;
- missing instructions;
- confidence before/after;
- L03 errors.

---

# 15. Module acceptance criteria

M06 can move from `CONTENT-COMPLETE DRAFT` to `PILOT-READY` only after:

- [x] substantive lessons exist;
- [x] casebook exists;
- [x] guided exercise exists;
- [x] knowledge check + answer key exist;
- [x] reference sheet exists;
- [x] common-errors/remediation exists;
- [x] instructor guide exists;
- [x] independent lab L03 exists;
- [x] current primary platform references checked;
- [ ] independent human run completed;
- [ ] wording/usability fixes applied;
- [ ] completion time calibrated;
- [ ] final reviewer grading pass completed.

---

# 16. What success looks like

After the module, a student should become **slower to make claims but faster to structure uncertainty**.

The most important behavioural change is hearing:

> «I can establish that A is the earliest source I found, but I cannot establish that A created the material.»

without instructor prompting.