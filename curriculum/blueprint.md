# Curriculum Blueprint v0.2

## Професійний практик OSINT

**Статус:** робочий curriculum design  
**Версія:** 0.2  
**Дата:** 10 серпня 2026 року  
**Пов’язані документи:**

- `docs/00-course-concept.md`
- `docs/01-graduate-profile.md`
- `docs/02-competency-map.md`
- `docs/03-terminology.md`
- `standards/osint-investigation-standard-v0.1.md`
- `research/donors/paulbradshaw-MED7369.md`
- `research/donors/berkeley-protocol.md`

---

# 1. Принцип побудови

Курс будується не навколо інструментів, а навколо **дослідницького циклу та перевірюваних компетентностей**.

Поточна нормативна послідовність:

```text
research question
→ systems / territory mapping
→ digital landscape assessment
→ threat / risk / harm assessment
→ working + competing hypotheses
→ collection plan
→ discovery / online inquiry
→ preliminary assessment
→ collection
→ preservation
→ verification: source + item + content
→ data structuring / hygiene
→ investigative analysis
→ confidence + limitations
→ peer review / red team
→ corrections
→ evidence/research package
→ handoff and/or reporting
```

Цикл ітеративний. Analysis може створити нові collection requirements і повернути дослідника до попередніх етапів.

Інструмент з’являється в курсі лише тоді, коли він потрібен для конкретної дослідницької дії. Заміна сервісу не повинна руйнувати модуль, якщо навчальна мета залишається тією самою.

---

# 2. Дві несучі методологічні рамки

## 2.1. Paul Bradshaw / investigative journalism donor

Дає нам:

- systems thinking;
- mapping the territory;
- hypothesis-driven inquiry;
- systems of accountability;
- network analysis;
- statistics + cognitive bias;
- text-as-data;
- data cleaning;
- project-driven learning.

Його головний педагогічний внесок:

> **спочатку зрозуміти систему та питання, потім обирати інструмент.**

## 2.2. Berkeley Protocol

Дає нам:

- professional / methodological / ethical principles;
- security before investigation;
- digital threat/risk assessment;
- digital landscape assessment;
- investigation planning;
- distinction between discovery, preliminary assessment, collection and preservation;
- verification model `source + item + content`;
- investigative analysis;
- reporting discipline;
- benchmark templates.

Його головний процесуальний внесок:

> **знайти матеріал недостатньо: потрібно вирішити, чи збирати його, зберегти provenance, перевірити source/item/content і лише потім будувати finding.**

Наш curriculum поєднує обидві рамки та додає:

- competing hypotheses;
- explicit confidence;
- statistical/cognitive-bias discipline;
- mandatory peer review для substantively important work;
- явні limitations;
- attribution ladder;
- evidence-first separation of internal package and public story.

---

# 3. Архітектура програми

Програма складається з п’яти шарів:

1. **Professional Foundations** — питання, система, безпека, planning, collection/preservation.
2. **Search & Verification** — source tracing, image/video, geolocation, chronolocation, spatial evidence.
3. **Entities, Data & Scale** — люди, організації, data hygiene, мережі, automation, statistics.
4. **Analysis & Professional Output** — competing hypotheses, confidence, peer review, evidence package, reporting.
5. **Ukraine–Russia–War Specialization** — регіональне джерельне середовище, військові структури, incident reconstruction, international-crime documentation і handoff boundaries.

---

# 4. Формат одного модуля

Кожен модуль MUST містити:

1. learning outcomes із competency IDs;
2. коротку теоретичну основу;
3. demonstration case;
4. guided exercise;
5. independent practice / lab;
6. checklist;
7. common failure modes;
8. `what this method does not establish`;
9. sources / donor traceability;
10. rubric / acceptance criteria;
11. актуальність інструментів і зовнішніх посилань;
12. tool validation, якщо модуль залежить від технічного сервісу;
13. instructor solution;
14. independent test run перед статусом `pilot-ready`.

---

# 5. PHASE A — PROFESSIONAL FOUNDATIONS

## M01. OSINT як професійна дисципліна

**Мета:** сформувати модель OSINT як відтворюваного відкритого дослідження.

**Темы:**

- OSINT / open source investigation;
- data, information, observation, indicator, claim, conclusion;
- open information vs ethical permission to use;
- uncertainty;
- professional principles: accountability, competence, objectivity, legality, security awareness;
- methodological/ethical discipline;
- limits of competence.

**Компетентності:** C01, C13, C15, C17  
**Артефакт:** факт/claim/inference decomposition exercise.

---

## M02. Systems Thinking, Territory Map & Digital Landscape

**Мета:** описати систему й цифрове середовище до широкого collection.

**Темы:**

- actors, institutions, formal/informal relations;
- systems of accountability;
- documents and registers;
- source ecosystems;
- digital traces;
- platform access and volatility;
- representation gaps;
- language/orthography;
- technical/legal/safety constraints;
- collection opportunities and gaps.

**Компетентності:** C02, C03  
**Donors:** Bradshaw + Berkeley Protocol preparation/Annex III.  
**Артефакт:** territory map + digital landscape assessment.

---

## M03. Research Question, Hypotheses & Collection Plan

**Мета:** перетворити тему на перевірюване питання та disciplined collection plan.

**Темы:**

- research question;
- working hypothesis;
- competing hypotheses;
- falsification / disconfirming search;
- collection requirements;
- priorities;
- stopping/review rules;
- investigation plan;
- change log.

**Компетентності:** C01, C03, C13  
**Donors:** Bradshaw Story-Based Inquiry logic adapted to evidence-first + Berkeley Investigation Plan.  
**Артефакт:** investigation plan + hypothesis matrix.

---

## M04. Threat Model, Ethics, Harm & Resilience

**Мета:** зробити security, harm minimisation і researcher resilience умовою початку роботи.

**Темы:**

- threat actors / assets / vulnerabilities;
- digital, physical and psychosocial risk;
- mitigation and residual risk;
- privacy;
- data minimisation;
- aggregation/re-identification risk;
- vulnerable persons;
- graphic-content exposure;
- resilience/self-care planning;
- stop / restrict / escalate decisions.

**Компетентності:** C15, C16  
**Donor:** Berkeley Protocol Security + Preparation.  
**External review:** trauma-informed details required before v1.0.  
**Артефакт:** threat model + harm assessment.

---

## M05. Preliminary Assessment, Collection, Preservation & Logging

**Мета:** навчити, що discovery, collection і preservation — різні професійні дії.

**Темы:**

- preliminary assessment;
- relevance and collection decision;
- data minimisation;
- volatility/deletion risk;
- native / near-native collection;
- collection profiles by object type;
- object IDs;
- metadata/context;
- hash and its limits;
- reference vs working copy;
- transformation log;
- preservation properties: authenticity, availability, identity, persistence, renderability, understandability;
- handling history / chain of custody as methodological record;
- research logging.

**Компетентності:** C05, C17  
**Donor:** Berkeley Protocol core-reviewed; Mnemonic/WITNESS review pending.  
**Артефакт:** digital object package.

---

# 6. PHASE B — SEARCH & VERIFICATION

## M06. Search Strategy, Source Tracing & Provenance Chains

**Мета:** системно знаходити джерела й відновлювати propagation/origin chain.

**Темы:**

- search operators and multiple indexes;
- multilingual variants;
- archives;
- earliest known source;
- creator vs uploader vs publisher;
- repost/manual copy/forward;
- circular reporting;
- edit/deletion history;
- provenance confidence;
- source verification layer.

**Компетентності:** C04, C05  
**Артефакт:** provenance chain.  
**Pilot lab:** L03 Telegram Source Tracing.

---

## M07. Image Verification

**Темы:**

- source/item/content model;
- reverse image search;
- earliest known appearance;
- crop/mirror/recompression;
- metadata;
- transformations;
- synthetic/manipulated imagery;
- external corroboration;
- AI detector limits.

**Компетентності:** C06  
**Артефакт:** verification sheet with SOURCE / ITEM / CONTENT.

---

## M08. Video & Audio Verification

**Темы:**

- source/item/content model;
- keyframes;
- upload history;
- cuts/editing;
- audio track;
- re-encoding;
- frame comparison;
- transcript provenance;
- synthetic/manipulated media;
- video-as-evidence considerations.

**Компетентності:** C06  
**External donor review:** WITNESS queued.  
**Артефакт:** structured video verification report.

---

## M09. Geolocation

**Темы:** architecture, roads, terrain, vegetation, utilities, signage, maps, panoramas, satellite imagery, alternative-location testing.

**Компетентності:** C07  
**Артефакт:** sourced geolocation dossier.

---

## M10. Chronolocation

**Темы:** upload vs event time, temporal bounds, shadows, weather, seasonality, satellite change, events, timezone uncertainty.

**Компетентності:** C07  
**Артефакт:** temporal-bounds report.

---

## M11. Maps, Satellite & Spatial Evidence

**Темы:** source metadata, resolution, optical imagery, SAR introduction, change detection, fires/damage, scale/projection errors, spatial uncertainty.

**Компетентності:** C07, C13  
**Артефакт:** spatial comparison report.

---

# 7. PHASE C — ENTITIES, DATA & SCALE

## M12. People, Digital Identities & Entity Resolution

**Темы:** names, aliases, usernames, identifiers, same-name problem, temporal consistency, observed/inferred identity links, supporting/contradicting indicators, do-no-harm limits.

**Компетентності:** C08, C09, C13, C15  
**Артефакт:** identity assessment matrix.

---

## M13. Organisations, Domains, Documents & Accountability Systems

**Темы:** registries, corporate/organisational records, procurement, official publications, documents, domain infrastructure introduction, following the money.

**Компетентності:** C02, C04, C08  
**Donor:** Bradshaw systems of accountability/company accounts.  
**Артефакт:** organisational source map.

---

## M14. Data Hygiene & Normalisation

**Темы:** raw vs processed, dates/URLs/names/geography, transliteration, `е/ё`, rename history, deduplication, false merge/split, audit trail, replaceable cleaning tools.

**Компетентності:** C09  
**Donor:** Bradshaw data cleaning.  
**Артефакт:** raw dataset + cleaned dataset + transformation log.

---

## M15. Timelines & Network Analysis

**Темы:** event vs publication, nodes/edges, observed vs inferred links, source-backed edges, temporal validity, confidence, graph as question generator rather than truth machine.

**Компетентності:** C11, C13  
**Donor:** Bradshaw network analysis.  
**Артефакт:** sourced timeline + sourced graph.

---

## M16. APIs, Scraping, Regex & Text-as-Data

**Темы:** when manual work stops scaling, API concepts, scraping, regex, corpora, reproducible parameters, validation samples, false positives/negatives, legal/ethical constraints, tool validation.

**Компетентності:** C10, C05  
**Donor:** Bradshaw APIs/scraping/text-as-data — rebuild for current environment.  
**Артефакт:** reproducible collection/extraction pipeline + QA note.

---

## M17. Statistics, Uncertainty & Cognitive Bias

**Темы:** denominator/base rate, sampling, selection bias, survivorship bias, correlation/causation, Simpson’s paradox, aggregation, dataset completeness, confirmation bias, availability bias, uncertainty communication.

**Компетентності:** C12, C13, C14  
**Donor:** Bradshaw statistics + cognitive bias.  
**Артефакт:** numerical claim critique + alternative interpretations.

---

# 8. PHASE D — ANALYSIS & PROFESSIONAL OUTPUT

## M18. Investigative Analysis, Competing Hypotheses & Attribution

**Темы:** verified observations, claim records, supporting/contradicting evidence, independence, inferential gaps, competing hypotheses, new collection requirements, attribution ladder, confidence language.

**Компетентності:** C03, C13  
**Donor:** Berkeley investigative analysis + our competing-hypotheses layer.  
**Артефакт:** claim/evidence matrix + analytical assessment.

---

## M19. Peer Review, Red Team & Correction

**Темы:** reproducibility review, source challenge, alternative hypothesis challenge, error taxonomy, confidence downgrade, correction log, reviewer response.

**Компетентності:** C14, C13, C05  
**Артефакт:** peer review + response/correction record.

---

## M20. Evidence/Research Package, Analytical Memo & Public Reporting

**Темы:** evidence index, raw vs analysis, digital-object cards, limitations, analytical memo, public report, redaction, sensitive annexes, storytelling after evidence, handoff package, legal-status boundaries.

**Компетентності:** C17, C05, C13, C15  
**Donors:** Berkeley reporting + Bradshaw storytelling adapted after evidence layer.  
**Артефакт:** internal package + memo + public-facing summary.

---

# 9. UKRAINE–RUSSIA–WAR SPECIALIZATION

Цей контур починається після core safety/evidence gates.

## U01. Українське та російське джерельне середовище

**Темы:** Telegram/VK/OK and relevant platforms; regional media; local administrations; memorial/award publications; public registers; language variants; renaming; source reliability; digital landscape by region/topic.

**Компетентності:** U01, C02, C04, C09  
**Артефакт:** regional/topic source ecosystem + digital landscape.

---

## U02. Військові структури, підрозділи та attribution ladder

Обов’язкова модель:

```text
належність
→ присутність
→ участь / функціональна роль
→ конкретна індивідуальна дія
→ юридична відповідальність
```

Кожен перехід потребує окремого evidence basis.

**Компетентності:** U02, C08, C11, C13  
**Артефакт:** time-bounded unit/person attribution assessment.

---

## U03. Реконструкція воєнного інциденту

**Темы:** event model, location, time, sequence, damage, possible means, military presence, source conflicts, alternative scenarios, unknowns.

**Компетентності:** U03, C06, C07, C11, C13  
**Артефакт:** incident reconstruction dossier.

---

## U04. Digital Open Source Documentation of Potential International Crimes

**Статус:** curriculum shell; зовнішня експертна валідація REQUIRED.

**Темы:** documentation vs legal qualification, preservation/provenance, incident elements, vulnerable persons, public/confidential material, Berkeley Protocol, professional competence limits, escalation.

**Компетентності:** U04, C05, C15, C17  
**Donors required:** Berkeley, WITNESS, Mnemonic/Ukrainian Archive, Truth Hounds, Murad Code guide where relevant.  
**Артефакт:** structured documentation package on safe historical/synthetic case.

---

## U05. Передавання матеріалів та межі правової оцінки

**Статус:** external Ukrainian legal review REQUIRED.

**Темы:** transfer package, source protection, sensitive annexes, recipient needs, transfer documentation, distinction between research finding and legal conclusion.

**Компетентності:** U05, C17, C15  
**Артефакт:** simulated handoff package.

---

# 10. Лабораторна система

Чотири типи:

1. **Controlled verification** — стабільний synthetic dataset із відомою логікою.
2. **Historical reconstruction** — публічно завершені кейси.
3. **Synthetic/anonymised sensitive cases** — identity/network/high-risk learning without live targets.
4. **Open research** — лише після safety/ethics gates.

---

# 11. Каталог лабораторних

| ID | Назва | Основні модулі | Статус / артефакт |
|---|---|---|---|
| L01 | Territory Map | M02–M03 | planned |
| L02 | Competing Hypotheses | M03, M18 | planned |
| L03 | Telegram Source Tracing | M05–M06 | **internally testable**; provenance package |
| L04 | Image Context Verification | M07 | planned |
| L05 | Video Origin & Context | M08 | planned |
| L06 | Геолокація без очевидної пам’ятки | M09 | planned |
| L07 | Chronolocation Range | M10 | planned |
| L08 | Dirty Entities | M12, M14 | planned |
| L09 | Sourced Network | M15 | planned |
| L10 | Text as Data | M16 | planned |
| L11 | Numbers Can Lie | M17 | planned |
| L12 | Wrong Attribution | M18 | planned |
| L13 | Peer Review Attack | M19 | planned |
| L14 | Unit Membership ≠ Crime | U02 | planned |
| L15 | Incident Reconstruction | U03 | planned |
| L16 | Evidence Handoff | U04–U05 | planned / external review required |

---

# 12. Наскрізні кейси

## Case A — Provenance & Verification

Один media object: discovery → preliminary assessment → collection/preservation → source tracing → verification → geo/time where applicable → finding.

## Case B — Entity & Network Investigation

Documents/profiles/data: entity resolution → cleaning → timeline/network → hypotheses → review.

## Case C — Ukraine/Russia Incident Case

Safe historical/public incident: unit attribution → incident reconstruction → evidence package → peer review.

До legal review Case C не вимагає від студента самостійно кваліфікувати international crime.

---

# 13. MVP / Pilot curriculum

Пілот повинен пройти весь цикл, але не всі 25 модулів.

| Pilot block | Source modules |
|---|---|
| P01. OSINT, claims, ethics | M01 + M04 |
| P02. Territory/digital landscape + hypotheses | M02 + M03 |
| P03. Preliminary assessment, collection, preservation | M05 |
| P04. Source tracing | M06 + L03 |
| P05. Image/video | M07 + M08 |
| P06. Geolocation/chronolocation | M09 + M10 |
| P07. Data hygiene + statistics + reasoning | M14 + M17 + M18 |
| P08. UA/RU source environment | U01 + intro U02 |
| P09. Peer review + package | M19 + M20 |

### Mandatory pilot labs

- L01 Territory Map;
- L03 Telegram Source Tracing;
- L06 Geolocation;
- L08 Dirty Entities;
- L12 Wrong Attribution;
- mini-capstone.

---

# 14. Assessment model

П’ять груп критеріїв:

## A. Method

Question, planning, preliminary assessment, method selection, alternatives.

## B. Evidence quality

Source/item/content verification, provenance, independence, preservation.

## C. Reproducibility

Can another researcher repeat central steps?

## D. Reasoning

Does conclusion match evidence? Were bias, alternatives and uncertainty addressed?

## E. Safety & Ethics

Was data minimisation applied? Was harm/security handled proportionately?

Critical failures C05, C13, C15, C16 or C17 cannot be averaged away.

---

# 15. Capstone package

Minimum:

- research question;
- territory map + digital landscape;
- threat/risk/harm assessment;
- hypotheses;
- collection plan;
- preliminary collection decisions where sensitive;
- source register;
- object/provenance records;
- raw/reference and working objects;
- verification outputs;
- transformation log;
- timeline/network where relevant;
- claim matrix;
- confidence + limitations;
- peer review + response;
- evidence/research package;
- audience-facing output.

A professionally justified negative result is valid.

---

# 16. Dependency map

```text
M01
 ├─ M02 ─ M03
 ├─ M04
 └─ M05 ─ M06
          ├─ M07
          ├─ M08
          ├─ M09 ─ M10 ─ M11
          └─ M12 ─ M14 ─ M15
                    └─ M16
M03 + M14 + M15 ─ M17 ─ M18 ─ M19 ─ M20

Core safety/evidence gates → U01 → U02 → U03 → U04 → U05
```

---

# 17. Donor-to-curriculum mapping

| Donor | Уже інтегровано | Статус |
|---|---|---|
| Paul Bradshaw / MED7369 | M02, M03, M13–M17, M20, project-driven model | initial audit integrated |
| Berkeley Protocol | M01–M06, M18–M20, U04–U05, templates | **core-reviewed and integrated** |
| Berkeley imagery guide (2024) | M07–M11 | queued |
| Murad Code open-source guide (2025) | M04, U04 high-risk survivor-centred practice | queued |
| WITNESS | M08, U04 | queued |
| Mnemonic / Ukrainian Archive | M05, U04–U05 | queued |
| Truth Hounds | U03–U05 | queued |
| Bellingcat | M06–M11, selected entity methods | queued |

Donor integration does not mean copying materials or assuming tool freshness.

---

# 18. Tool validation rule

A tool-dependent module cannot become `pilot-ready` until the tool/service has been checked for:

- current availability;
- ownership/developer;
- data handling/privacy;
- input/output behaviour;
- known error modes;
- coverage/rate limits;
- reproducibility;
- security implications;
- replacement path.

The curriculum teaches a method; tool is replaceable implementation.

---

# 19. Definition of Done for module

Module becomes `pilot-ready` only when:

- outcomes map to competency IDs;
- lesson complete;
- demonstration case exists;
- independent task produces a checkable artefact;
- rubric exists;
- instructor solution exists;
- limitations and harm risks documented;
- sources registered;
- tools/links validated;
- another tester completes it without oral explanation.

Any necessary oral explanation is a documentation/course bug.

---

# 20. Current production order

1. OSINT Investigation Standard v0.1 — **done**;
2. core planning/evidence templates — **initial set done**;
3. L03 Telegram Source Tracing — **internally testable**;
4. independent human run of L03;
5. create pilot-ready M05/M06 around L03;
6. complete file-by-file Bradshaw audit;
7. audit Berkeley imagery guide;
8. audit WITNESS/Mnemonic preservation/video guidance;
9. build L01 + L12;
10. run first mini-pilot;
11. revise Blueprint/Standard to next versions.

---

# 21. Known unresolved design questions

- final course duration;
- pilot cohort profile;
- exact certification thresholds;
- public/open vs controlled access to sensitive specialization;
- Ukrainian legal terminology;
- retention/deletion policy;
- virtual identity policy;
- trauma-informed workflow details;
- final confidence-language style guide.

These are explicit open design questions, not hidden assumptions.
