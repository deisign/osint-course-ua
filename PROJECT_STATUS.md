# Project status

**Дата:** 2026-08-10  
**Стадія:** pre-alpha / curriculum design + three-lab mini-pilot preparation

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
- [x] Draft M06 — Search Strategy, Source Tracing & Provenance Chains
- [x] L01 Territory Map — synthetic controlled lab assembled
- [x] L01 structural/internal validation
- [x] L03 Telegram Source Tracing — synthetic controlled lab assembled
- [x] L03 machine/data validation
- [x] L12 Wrong Attribution — synthetic controlled lab assembled
- [x] L12 structural/bias validation
- [x] Submission templates for L01 and L12
- [x] Mini-pilot v0.1 protocol for L01 → L03 → L12

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
- expected SHA-256 values for synthetic media.

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

## M05/M06 status

Both modules are `DRAFT` and already include:

- learning outcomes;
- core lesson logic;
- demonstration using L03;
- guided exercise design;
- independent assessment link;
- checklist;
- common failure modes;
- limitations;
- donor traceability;
- tool policy.

Before `pilot-ready`:

- [ ] independent human run of L03;
- [ ] final guided-exercise fixtures;
- [ ] Mnemonic/WITNESS review for M05;
- [ ] Bellingcat/source-tracing review for M06;
- [ ] current optional tool validation.

## Mini-pilot v0.1

Protocol: `pilot/mini-pilot-v0.1.md`

Sequence:

1. L01 Territory Map;
2. L03 Telegram Source Tracing;
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

- [ ] Run mini-pilot v0.1 with 5–8 participants
- [ ] Create `pilot/mini-pilot-v0.1-report.md`
- [ ] Complete remaining Bradshaw audit: statistics + selected notebooks/exercises + licensing
- [ ] Audit Berkeley imagery guide (2024)
- [ ] Audit WITNESS / Mnemonic preservation and video guidance
- [ ] Build M02/M03 around L01
- [ ] Build M17/M18 around L12
- [ ] Revise Blueprint after pilot evidence

## Поточна архітектура

- 17 базових доменів компетентностей;
- 5 компетентностей спеціалізації «Україна — Росія — війна»;
- 20 core-модулів;
- 5 модулів спеціалізації;
- 16 запланованих лабораторних;
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

Лабораторна або модуль вважається `pilot-ready` лише після learning outcomes / task, практичного артефакту, rubric, instructor solution, limitations, перевірених технічних інструкцій та незалежного тестового проходження.
