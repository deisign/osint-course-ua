# Project status

**Дата:** 2026-08-10  
**Стадія:** pre-alpha / first golden-module implementation + three-lab mini-pilot preparation

## Готово

- [x] Концепція курсу v0.1
- [x] Базова структура репозиторію
- [x] Реєстр зовнішніх джерел
- [x] Профіль компетентностей випускника v0.1
- [x] Карта компетентностей v0.1
- [x] Термінологія v0.1
- [x] Curriculum Blueprint v0.2
- [x] OSINT Investigation Standard v0.1
- [x] Core audit Berkeley Protocol
- [x] Partial file-level audit Paul Bradshaw / MED7369
- [x] Initial core templates
- [x] Draft M05 — Preliminary Assessment, Collection, Preservation & Research Logging
- [x] **M06 golden-module candidate — Content-Complete Draft**
- [x] L01 Territory Map — synthetic controlled lab assembled
- [x] L01 structural/internal validation
- [x] L03 Telegram Source Tracing — synthetic controlled lab assembled
- [x] L03 machine/data validation
- [x] L12 Wrong Attribution — synthetic controlled lab assembled
- [x] L12 structural/bias validation
- [x] Submission templates for L01 and L12
- [x] Mini-pilot v0.1 protocol for L01 → L03 → L12

## M06 — Golden-module candidate

**Статус:** `CONTENT-COMPLETE DRAFT`

M06 тепер не є curriculum skeleton. Він містить повний authored learning path:

### Core lessons

1. `01-why-provenance-matters.md`
2. `02-source-roles.md`
3. `03-propagation-models.md`
4. `04-search-strategy.md`
5. `05-telegram-specifics.md`
6. `06-web-and-archives.md`
7. `07-media-provenance.md`
8. `08-circular-reporting.md`
9. `09-confidence-and-limitations.md`

### Practice & assessment

- 12-case micro-casebook;
- two-phase guided exercise with model revision;
- guided instructor solution;
- 20-question knowledge check + answer key;
- reference sheet;
- 20-error remediation guide;
- source dossier + freshness policy;
- instructor guide;
- independent controlled lab L03.

### Current source validation

Checked 2026-08-10:

- official Telegram FAQ/API/TDLib for forward/edit/copy/delete provenance behaviour;
- official Internet Archive / Wayback Machine help for archive/capture limitations;
- Bellingcat used only as practitioner donor, not platform documentation.

Still required before `PILOT-READY`:

- [ ] independent human run without oral hints;
- [ ] measured completion time per component;
- [ ] usability/wording fixes;
- [ ] final reviewer grading pass;
- [ ] optional current live-demo tools validated.

## Lab status

### L01 — Territory Map

**`DRAFT / internally testable`**

Checks passed:

- synthetic scenario and seeds;
- 12 unique seed records;
- deliberate `given / inferred` distinction;
- rubric and instructor solution aligned with task;
- submission template added;
- no real private-person identification required.

Still required for `pilot-ready`:

- [ ] independent human run without oral hints;
- [ ] measured completion time;
- [ ] usability fixes;
- [ ] grading calibration.

### L03 — Telegram Source Tracing

**`DRAFT / internally testable`**

Checks passed:

- CSV structure and chronology;
- explicit-forward logic;
- edit/deletion states;
- expected SHA-256 values for synthetic media;
- now embedded in full M06 learning path.

Still required for `pilot-ready`:

- [ ] independent human run without oral hints;
- [ ] measured completion time;
- [ ] wording/usability fixes from tester;
- [ ] final instructor grading pass.

### L12 — Wrong Attribution

**`DRAFT / internally testable`**

Checks passed:

- 2 synthetic candidate profiles;
- 15 unique observations;
- 10 claims for claim-by-claim assessment;
- mixed provenance strengths (`strong / medium / weak / none`);
- no hidden positive attribution to P-A or P-B;
- task explicitly separates account control / identity / affiliation / presence / action;
- submission templates added.

Still required for `pilot-ready`:

- [ ] independent human run without oral hints;
- [ ] measured completion time;
- [ ] ambiguity review of claims;
- [ ] grading calibration.

## M05 status

M05 remains `DRAFT` and includes:

- learning outcomes;
- core lesson logic;
- demonstration using L03;
- checklist;
- common failure modes;
- limitations;
- donor traceability;
- tool policy.

Before `pilot-ready`:

- [ ] expand to authored golden-module depth after M06 pilot lessons;
- [ ] Mnemonic/WITNESS review;
- [ ] independent practice fixtures;
- [ ] human usability run.

## Mini-pilot v0.1

Protocol: `pilot/mini-pilot-v0.1.md`

Sequence:

1. L01 Territory Map;
2. M06 learning path + L03 Telegram Source Tracing;
3. L12 Wrong Attribution.

The pilot tests three fundamental habits:

`system mapping → provenance → calibrated refusal of over-attribution`.

Primary pilot measurements:

- completion time;
- clarification questions;
- rubric scores;
- critical-fail types;
- participant confidence vs actual performance;
- reviewer disagreement.

## Наступне

- [ ] Run independent human pilot of M06 + L03 first
- [ ] Fix M06 using observed learner failures
- [ ] Then run full mini-pilot v0.1 with 5–8 participants
- [ ] Create `pilot/mini-pilot-v0.1-report.md`
- [ ] Complete remaining Bradshaw audit: statistics + selected notebooks/exercises + licensing
- [ ] Audit Berkeley imagery guide (2024)
- [ ] Audit WITNESS / Mnemonic preservation and video guidance
- [ ] Build M02/M03 around L01 to golden-module depth
- [ ] Build M17/M18 around L12 to golden-module depth
- [ ] Revise Blueprint after pilot evidence

## Поточна архітектура

- 17 базових доменів компетентностей;
- 5 компетентностей спеціалізації «Україна — Росія — війна»;
- 20 core-модулів;
- 5 модулів спеціалізації;
- 16 запланованих лабораторних;
- 1 content-complete golden-module candidate (M06);
- 3 controlled labs assembled and internally testable;
- 3 типи наскрізних кейсів;
- окремий MVP/pilot curriculum;
- evidence-first lifecycle за OSINT Investigation Standard v0.1.

## Core templates created

- `templates/investigation-plan.md`
- `templates/digital-landscape.md`
- `templates/threat-model.md`
- `templates/harm-assessment.md`
- `templates/hypothesis-matrix.md`
- `templates/digital-object-card.md`
- `templates/collection-log.csv`
- `templates/verification-sheet.md`
- `templates/peer-review-form.md`

## Правило готовності

Матеріал вважається частиною курсу лише після внесення до репозиторію із зазначенням джерел, статусу перевірки та версії.

Лабораторна або модуль вважається `pilot-ready` лише після substantive learning content/task, практичного артефакту, rubric/instructor solution where applicable, limitations, перевірених технічних інструкцій та незалежного тестового проходження.