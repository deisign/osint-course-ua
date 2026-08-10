# Curriculum Blueprint v0.1

## Професійний практик OSINT

**Статус:** робочий curriculum design  
**Версія:** 0.1  
**Дата:** 10 серпня 2026 року  
**Пов’язані документи:**

- `docs/00-course-concept.md`
- `docs/01-graduate-profile.md`
- `research/donors/paulbradshaw-MED7369.md`

---

# 1. Принцип побудови

Курс будується не навколо інструментів, а навколо **дослідницького циклу та перевірюваних компетентностей**.

Основна послідовність:

`питання → система → гіпотези → план збору → пошук → збереження → верифікація → структурування → аналіз → peer review → документування → передавання / публікація`.

Інструмент з’являється в курсі лише тоді, коли він потрібен для конкретної дослідницької дії. Заміна сервісу не повинна руйнувати модуль, якщо навчальна мета залишилася тією самою.

---

# 2. Архітектура програми

Програма складається з п’яти шарів:

1. **Professional Foundations** — мислення, питання, система, безпека та provenance.
2. **Verification** — перевірка походження, зображень, відео, місця й часу.
3. **Entities, Data & Scale** — люди, організації, дані, мережі, автоматизація, статистика.
4. **Analysis & Reporting** — competing hypotheses, confidence, peer review, evidence package.
5. **Ukraine–Russia–War Specialization** — контекстні джерела, військові структури, реконструкція інцидентів і документування ймовірних міжнародних злочинів.

Кожен модуль має завершуватися **артефактом**, який може бути перевірений, а не лише тестом на запам’ятовування.

---

# 3. Формат одного модуля

Кожен модуль повинен містити:

1. learning outcomes;
2. коротку теоретичну основу;
3. демонстраційний розбір;
4. guided exercise;
5. самостійну практику або лабораторну;
6. checklist;
7. common failure modes;
8. limitations;
9. первинні та вторинні джерела;
10. rubric або критерії приймання;
11. дату перевірки інструментів і зовнішніх посилань.

Структура модуля не вважається завершеною без секції **«Що цей метод не дозволяє стверджувати»**.

---

# 4. Модульна карта

## PHASE A — PROFESSIONAL FOUNDATIONS

### M01. OSINT як професійна дисципліна

**Мета:** сформувати правильну модель OSINT як відтворюваного відкритого дослідження.

**Ключові теми:**

- OSINT, open source investigation, fact-checking, investigative journalism, intelligence analysis;
- дані, інформація, факт, індикатор, твердження, висновок, доказ;
- межі відкритих джерел;
- професійна невизначеність;
- роль журналу дослідження;
- етика та принцип мінімізації шкоди.

**Компетентності:** `C01`, `C13`, `C15`, `C17`  
**Артефакт:** розбір публікації на факт / твердження / припущення / висновок / невідоме.

---

### M02. Systems Thinking і Mapping the Territory

**Мета:** навчити досліджувати систему до того, як дослідник починає збирати випадкові знахідки.

**Ключові теми:**

- актори та інституції;
- формальні й неформальні відносини;
- системи підзвітності;
- документи та реєстри;
- цифрові сліди;
- source ecosystem;
- інформаційні прогалини;
- collection requirements.

**Компетентності:** `C02`, `C03`  
**Donor:** Paul Bradshaw / MED7369 — `ADOPT + ADAPT`.  
**Артефакт:** territory map заданої теми.

---

### M03. Research Question, Hypotheses і Collection Plan

**Мета:** перетворити тему на перевірюване питання та план збору.

**Ключові теми:**

- research question;
- working hypothesis;
- competing hypotheses;
- falsification;
- collection requirements;
- stopping rules;
- evidence for / against;
- дослідницький журнал.

**Компетентності:** `C01`, `C03`, `C13`  
**Donor:** Story-Based Inquiry / Bradshaw — `ADAPT` до evidence-first моделі.  
**Артефакт:** investigation plan + hypothesis matrix.

---

### M04. Threat Model, Ethics і Harm Assessment

**Мета:** зробити безпеку та допустимість дії частиною планування, а не додатком наприкінці.

**Ключові теми:**

- threat model;
- активи й супротивник;
- персональна й командна безпека;
- приватність;
- vulnerable subjects;
- data minimisation;
- publication harm;
- stop / escalate decisions.

**Компетентності:** `C15`, `C16`  
**Артефакт:** threat model + documented harm assessment.

---

### M05. Provenance, Preservation і Research Logging

**Мета:** навчити зберігати походження й історію роботи з цифровим матеріалом.

**Ключові теми:**

- URL і canonical URL;
- дата створення / публікації / виявлення;
- оригінал і робоча копія;
- хешування;
- скриншот та його обмеження;
- збереження вебконтенту;
- індекс цифрових об’єктів;
- журнал дій;
- reproducibility.

**Компетентності:** `C05`, `C17`  
**Зовнішня валідація:** Berkeley Protocol, Mnemonic, WITNESS — queued.  
**Артефакт:** правильно оформлений digital object package.

---

## PHASE B — SEARCH & VERIFICATION

### M06. Search Strategy і Source Tracing

**Мета:** навчити системному пошуку та відновленню походження інформації.

**Ключові теми:**

- оператори пошуку;
- різні пошукові індекси;
- багатомовний пошук;
- варіанти імен і назв;
- архіви;
- ранні версії;
- перепублікації;
- circular reporting;
- source proximity.

**Компетентності:** `C04`  
**Артефакт:** provenance chain одного твердження або медіаоб’єкта.

---

### M07. Image Verification

**Мета:** перевіряти походження, контекст та зміни зображень.

**Ключові теми:**

- reverse image search;
- earliest known appearance;
- crop / mirror / recompression;
- metadata;
- visual inconsistencies;
- reused imagery;
- synthetic imagery;
- limits of AI detectors.

**Компетентності:** `C06`  
**Артефакт:** image verification sheet.

---

### M08. Video & Audio Verification

**Мета:** системно аналізувати відео- й аудіоматеріали.

**Ключові теми:**

- keyframes;
- upload history;
- editing and cuts;
- audio track;
- re-encoding;
- frame-level comparison;
- content/context distinction;
- synthetic/manipulated media.

**Компетентності:** `C06`  
**Артефакт:** structured video verification report.

---

### M09. Geolocation

**Мета:** встановлювати або звужувати місце зйомки на основі незалежних ознак.

**Ключові теми:**

- architecture;
- road geometry;
- terrain;
- vegetation;
- power infrastructure;
- signage;
- maps and panoramas;
- satellite imagery;
- negative verification of alternatives.

**Компетентності:** `C07`  
**Артефакт:** geolocation dossier з мінімум трьома незалежними ознаками та перевіреною альтернативою.

---

### M10. Chronolocation

**Мета:** визначати доказовий часовий інтервал замість штучної точності.

**Ключові теми:**

- upload time vs event time;
- shadows;
- weather;
- seasonal clues;
- vegetation;
- satellite change;
- local events;
- lower/upper temporal bounds.

**Компетентності:** `C07`  
**Артефакт:** chronolocation sheet з часовим інтервалом і рівнем упевненості.

---

### M11. Maps, Satellite & Spatial Evidence

**Мета:** навчити читати просторові дані як джерело з власними обмеженнями.

**Ключові теми:**

- map layers;
- resolution;
- optical imagery;
- SAR — conceptual introduction;
- change detection;
- fires and damage;
- scale and projection errors;
- source/date metadata.

**Компетентності:** `C07`, `C13`  
**Артефакт:** spatial comparison report.

---

## PHASE C — ENTITIES, DATA & SCALE

### M12. People, Digital Identities & Entity Resolution

**Мета:** перевіряти тотожність відкритих цифрових слідів без надмірної атрибуції.

**Ключові теми:**

- names and aliases;
- usernames;
- reused identifiers;
- phones/emails where lawful and appropriate;
- profile continuity;
- temporal consistency;
- same-name problem;
- supporting vs contradicting indicators.

**Компетентності:** `C08`, `C09`, `C13`, `C15`  
**Артефакт:** identity assessment matrix.

---

### M13. Organisations, Domains, Documents & Accountability Systems

**Мета:** знаходити інституційні та документальні сліди організацій.

**Ключові теми:**

- registries;
- corporate records;
- organisational documents;
- procurement and accountability systems;
- domain infrastructure at introductory level;
- official publications;
- document provenance;
- following the money as one investigative path.

**Компетентності:** `C02`, `C04`, `C08`  
**Donor:** Bradshaw systems of accountability / company accounts — `EXPAND + ADAPT`.  
**Артефакт:** organisational source map.

---

### M14. Data Hygiene & Normalisation

**Мета:** зробити очищення даних доказово контрольованою процедурою.

**Ключові теми:**

- raw vs processed data;
- normalisation rules;
- dates and URLs;
- names and geography;
- transliteration;
- deduplication;
- false merge / false split;
- audit trail;
- OpenRefine or equivalent tools as replaceable implementation.

**Компетентності:** `C09`  
**Donor:** Bradshaw data cleaning — `ADOPT + EXPAND`.  
**Артефакт:** raw dataset + cleaned dataset + transformation log.

---

### M15. Timelines & Network Analysis

**Мета:** структурувати складні події та зв’язки без втрати джерел і часової валідності.

**Ключові теми:**

- event vs publication;
- timeline construction;
- nodes and edges;
- observed vs inferred links;
- temporal edges;
- confidence;
- graph provenance;
- network analysis as question generator, not truth machine.

**Компетентності:** `C11`, `C13`  
**Donor:** Bradshaw network analysis — `EXPAND`.  
**Артефакт:** sourced timeline + sourced graph.

---

### M16. APIs, Scraping, Regex & Text-as-Data

**Мета:** навчити масштабувати збір і пошук, не перетворюючи курс на окремий курс програмування.

**Ключові теми:**

- when manual collection stops scaling;
- API concepts;
- reproducible requests;
- scraping concepts;
- robots/terms/legal-ethical constraints;
- regex;
- text corpora;
- validation samples;
- false positives / negatives;
- logging parameters and versions.

**Компетентності:** `C10`, `C05`  
**Donor:** Bradshaw APIs / scraping / text-as-data — `REBUILD + EXPAND`.  
**Артефакт:** reproducible collection or extraction pipeline + validation note.

---

### M17. Statistics, Uncertainty & Cognitive Bias

**Мета:** захистити дослідника від переконливих, але неправильних числових і когнітивних висновків.

**Ключові теми:**

- denominator and base-rate problems;
- sampling;
- selection bias;
- survivorship bias;
- correlation vs causation;
- Simpson’s paradox;
- misleading aggregation;
- confirmation bias;
- availability bias;
- dataset completeness;
- uncertainty communication.

**Компетентності:** `C12`, `C13`, `C14`  
**Donor:** Bradshaw statistics + cognitive bias — `EXPAND`.  
**Артефакт:** critique of a numerical claim + alternative interpretations.

---

## PHASE D — ANALYSIS & PROFESSIONAL OUTPUT

### M18. Analytical Reasoning & Competing Hypotheses

**Мета:** перейти від набору перевірених об’єктів до обґрунтованого висновку.

**Ключові теми:**

- evidence statements;
- supporting / contradicting evidence;
- independent corroboration;
- competing hypotheses;
- disconfirming evidence;
- inferential gaps;
- attribution ladders;
- confidence language.

**Компетентності:** `C03`, `C13`  
**Артефакт:** analytical assessment with evidence matrix.

---

### M19. Peer Review, Red Team & Error Correction

**Мета:** зробити перевірку іншою людиною обов’язковим етапом дослідницького циклу.

**Ключові теми:**

- reproducibility review;
- source challenge;
- alternative-hypothesis challenge;
- blind spots;
- error taxonomy;
- confidence downgrade;
- correction log;
- reviewer response.

**Компетентності:** `C14`, `C13`, `C05`  
**Артефакт:** peer-review report + author response.

---

### M20. Evidence Package, Analytical Memo & Public Reporting

**Мета:** навчити перетворювати одну доказову основу на різні професійні продукти без втрати provenance.

**Ключові теми:**

- evidence index;
- digital object cards;
- research limitations;
- analytical memo;
- public investigation/report;
- redaction;
- sensitive data;
- storytelling after evidence;
- transfer package;
- distinction between investigative documentation and legal admissibility.

**Компетентності:** `C17`, `C05`, `C13`, `C15`  
**Donor:** Bradshaw storytelling — `ADAPT`; evidence-first layer is our required addition.  
**Артефакт:** internal package + analytical memo + public-facing summary.

---

# 5. UKRAINE–RUSSIA–WAR SPECIALIZATION

Цей контур проходить лише після базових модулів, оскільки контекст війни підвищує ціну помилки й шкоди.

---

### U01. Українське та російське джерельне середовище

**Ключові теми:**

- Telegram, VK, OK та інші релевантні платформи;
- регіональні медіа;
- сайти органів влади;
- локальні адміністративні джерела;
- нагородні й меморіальні публікації;
- військові й ветеранські спільноти;
- судові та інші відкриті реєстрові системи;
- українська/російська орфографія;
- транслітерації;
- перейменування;
- local source reliability.

**Компетентності:** `U01`, `C02`, `C04`, `C09`  
**Артефакт:** source ecosystem map заданого російського або українського регіону/теми.

---

### U02. Військові структури, підрозділи та attribution ladder

**Ключові теми:**

- unit identity;
- subordination;
- time-bounded membership;
- awards and official traces;
- fellow servicemen and public networks;
- equipment and markings as indicators;
- unit presence;
- individual presence;
- participation;
- action;
- responsibility.

**Обов’язкова модель:**

`належність → присутність → участь → індивідуальна дія → юридична відповідальність`.

Кожна стрілка потребує окремого набору підтверджень.

**Компетентності:** `U02`, `C08`, `C11`, `C13`  
**Артефакт:** time-bounded unit/person attribution assessment.

---

### U03. Реконструкція воєнного інциденту

**Ключові теми:**

- event model;
- location;
- time;
- sequence;
- damage;
- possible means;
- military presence;
- casualties where ethically appropriate;
- source conflicts;
- alternative scenarios;
- unknowns.

**Компетентності:** `U03`, `C06`, `C07`, `C11`, `C13`  
**Артефакт:** incident reconstruction dossier.

---

### U04. Digital Open Source Documentation of Potential International Crimes

**Статус:** curriculum shell; остаточний зміст потребує зовнішньої експертної рецензії.

**Ключові теми:**

- documentation vs legal qualification;
- preservation and provenance;
- incident elements;
- vulnerable persons;
- public vs confidential material;
- limits of civilian open-source investigation;
- Berkeley Protocol framework;
- escalation to qualified specialists.

**Компетентності:** `U04`, `C05`, `C15`, `C17`  
**Required donor review:** Berkeley Protocol, WITNESS, Mnemonic/Ukrainian Archive, Truth Hounds.  
**Артефакт:** structured documentation package on a historical/public training case.

---

### U05. Передавання матеріалів та межі правової оцінки

**Статус:** потребує зовнішньої рецензії українського фахівця з кримінального процесу / міжнародних злочинів.

**Ключові теми:**

- transfer package;
- source protection;
- redaction;
- sensitive annexes;
- recipient needs;
- documentation of transfer;
- what OSINT practitioner can state;
- what requires investigator, prosecutor, lawyer or expert.

**Компетентності:** `U05`, `C17`, `C15`  
**Артефакт:** simulated handoff package.

---

# 6. Лабораторна система

Лабораторні поділяються на чотири типи.

## Type A — Controlled verification

Підготовлені матеріали з відомою відповіддю для перевірки базової техніки.

## Type B — Historical reconstruction

Публічно завершені історичні кейси, де студент повторює або критично перевіряє шлях дослідження.

## Type C — Synthetic / anonymised cases

Спеціально створені або знеособлені набори для identity resolution, network analysis та sensitive topics.

## Type D — Open research

Реальне нове дослідження лише після проходження базових safety/ethics gates.

---

# 7. Початковий каталог лабораторних

| ID | Назва | Основні модулі | Головний артефакт |
|---|---|---|---|
| `L01` | Territory Map | M02–M03 | карта системи й collection plan |
| `L02` | Competing Hypotheses | M03, M18 | hypothesis/evidence matrix |
| `L03` | Відновлення першоджерела Telegram-публікації | M05–M06 | provenance package |
| `L04` | Image Context Verification | M07 | verification sheet |
| `L05` | Video Origin & Context | M08 | video verification report |
| `L06` | Геолокація без очевидної пам’ятки | M09 | geolocation dossier |
| `L07` | Chronolocation Range | M10 | temporal bounds report |
| `L08` | Dirty Entities | M12, M14 | cleaned entity dataset + audit log |
| `L09` | Sourced Network | M15 | graph with observed/inferred edges |
| `L10` | Text as Data | M16 | reproducible extraction + QA sample |
| `L11` | Numbers Can Lie | M17 | statistical critique |
| `L12` | Wrong Attribution | M18 | justified rejection / confidence downgrade |
| `L13` | Peer Review Attack | M19 | review + response |
| `L14` | Unit Membership ≠ Crime | U02 | bounded attribution assessment |
| `L15` | Incident Reconstruction | U03 | incident dossier |
| `L16` | Evidence Handoff | U04–U05 | structured transfer package |

---

# 8. Сквозні кейси

Курс повинен мати щонайменше три сквозні кейси різного типу.

## Case A — Provenance & Verification

Один медіаоб’єкт проходить шлях від першого виявлення до збереження, source tracing, image/video verification, geolocation/chronolocation та короткого висновку.

## Case B — Entity & Network Investigation

Набір документів, профілів і публікацій використовується для entity resolution, data cleaning, timeline, network analysis та competing hypotheses.

## Case C — Ukraine/Russia Incident Case

Історичний публічний епізод війни, достатньо безпечний для навчання, використовується для unit attribution, incident reconstruction, evidence package і peer review.

До зовнішньої правової рецензії Case C не повинен вимагати від студента самостійної юридичної кваліфікації міжнародного злочину.

---

# 9. MVP / Pilot curriculum

Перший пілот не потребує всіх модулів. Мінімальна працездатна версія курсу:

| Pilot block | Джерело |
|---|---|
| P01. OSINT, факт, висновок, етика | M01 + M04 |
| P02. Territory map, питання й гіпотези | M02 + M03 |
| P03. Provenance і першоджерело | M05 + M06 |
| P04. Зображення / відео | M07 + M08 |
| P05. Геолокація / хронолокація | M09 + M10 |
| P06. Data hygiene + evidence reasoning | M14 + M17 + M18 |
| P07. Українсько-російське джерельне середовище | U01 + introduction to U02 |
| P08. Peer review + evidence package | M19 + M20 |

### Pilot labs

Обов’язкові:

- `L01 Territory Map`;
- `L03 Telegram Source Tracing`;
- `L06 Geolocation`;
- `L08 Dirty Entities`;
- `L12 Wrong Attribution`;
- фінальний mini-capstone.

Пілот має бути достатньо коротким для швидкого тестування, але повинен містити весь дослідницький цикл.

---

# 10. Assessment model

Оцінювання будується за п’ятьма групами критеріїв.

## A. Method

Чи була постановка задачі, план, належний вибір методів і перевірка альтернатив?

## B. Evidence quality

Чи відповідають джерела твердженням? Чи збережено provenance? Чи є незалежні підтвердження?

## C. Reproducibility

Чи може інший дослідник повторити ключові кроки?

## D. Reasoning

Чи не перевищує висновок силу матеріалу? Чи враховано uncertainty, bias та competing hypotheses?

## E. Safety & Ethics

Чи було мінімізовано шкоду? Чи дотримано меж роботи з чутливими матеріалами?

Критичні провали `C05`, `C13`, `C15`, `C16` або `C17` не можуть бути компенсовані високими балами за технічні інструменти.

---

# 11. Capstone

Фінальна робота — не «знайти щось цікаве», а виконати відтворюване дослідження.

Мінімальний пакет визначено у `docs/01-graduate-profile.md` і включає:

- research question;
- territory map;
- threat/harm assessment;
- hypothesis matrix;
- collection plan;
- source register;
- provenance objects;
- verification outputs;
- data transformation log;
- timeline/network where relevant;
- analytical conclusion + confidence;
- limitations;
- peer review + response;
- evidence package;
- audience-facing output.

Правильний negative result допускається й оцінюється позитивно, якщо процедура виконана якісно.

---

# 12. Dependency map

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

Core completion → U01 → U02 → U03 → U04 → U05
```

Це логічні залежності, а не обов’язково календарний порядок. Частина модулів може викладатися паралельно.

---

# 13. Donor-to-curriculum mapping

Поточний research layer використовується так:

| Donor | Уже інтегровано | Статус |
|---|---|---|
| Paul Bradshaw / MED7369 | M02, M03, M13–M17, M20, project-driven model | initial audit integrated |
| Berkeley Protocol | M05, U04, U05 | queued for full audit |
| WITNESS | M08, M15? / U04 ethics & video evidence | queued |
| Mnemonic / Ukrainian Archive | M05, U04–U05 | queued |
| Truth Hounds | U03–U05 | queued |
| Bellingcat | M06–M11, selected entity methods | queued |

Включення donor idea в blueprint не означає автоматичного копіювання матеріалів або підтвердження їхньої актуальності.

---

# 14. Що не входить до core curriculum

Без окремої спеціалізації або зовнішньої валідації курс не навчає:

- exploit development або несанкціонованого доступу;
- malware analysis;
- forensic extraction із вилучених пристроїв;
- професійного HUMINT;
- undercover operations;
- допиту / forensic interviewing постраждалих;
- самостійної юридичної кваліфікації міжнародних злочинів;
- профільної експертизи зброї та боєприпасів;
- будь-яких практик, де навчальна цінність не виправдовує ризик для реальних людей.

---

# 15. Definition of Done для модуля

Модуль переходить зі статусу `draft` у `pilot-ready`, коли:

- learning outcomes прив’язані до competency IDs;
- навчальний текст завершено;
- є щонайменше один демонстраційний кейс;
- є практичний артефакт;
- rubric описує прийнятний і неприйнятний результат;
- усі зовнішні технічні інструкції перевірено на актуальність;
- джерела внесено до registry/bibliography;
- sensitive-content risks оцінено;
- limitations описано;
- instructor solution існує;
- інший тестовий користувач здатний пройти завдання без усного пояснення автора.

---

# 16. Наступні кроки

Після Blueprint v0.1 виробничий порядок:

1. `docs/03-terminology.md` — термінологічний словник v0.1;
2. `standards/osint-investigation-standard-v0.1.md`;
3. повний file-by-file аудит Paul Bradshaw / MED7369;
4. аудит Berkeley Protocol;
5. створення `L03` — відновлення та документування першоджерела Telegram-публікації;
6. створення першого pilot-ready модуля M05/M06;
7. внутрішній прогін лабораторної;
8. корекція Blueprint до v0.2.

---

# 17. Статус документа

Blueprint v0.1 фіксує **архітектуру**, а не остаточну кількість годин або календарний розклад.

До визначення годин потрібно провести щонайменше один реальний pilot run, оскільки тривалість OSINT-лабораторних залежить не лише від обсягу теорії, а й від складності пошуку, якості даних і кількості false leads.
