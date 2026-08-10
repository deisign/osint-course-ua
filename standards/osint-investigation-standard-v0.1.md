# OSINT Investigation Standard v0.1

## Внутрішній стандарт відкритого дослідження курсу «Професійний практик OSINT»

**Версія:** 0.1  
**Дата:** 10 серпня 2026 року  
**Статус:** draft standard / ready for internal testing  
**Зовнішня юридична валідація:** НЕ ПРОЙДЕНА

---

# 1. Призначення

Стандарт встановлює мінімальні вимоги до дослідження, яке вважається професійно виконаним у межах курсу.

Його мета — забезпечити:

- відтворюваність;
- прозоре походження матеріалів;
- належне збереження digital items;
- системну verification;
- контроль inferential gaps;
- перевірку competing hypotheses;
- явне формулювання uncertainty;
- мінімізацію шкоди;
- можливість незалежного peer review;
- підготовку матеріалу до професійного handoff без необґрунтованих заяв про його юридичний статус.

Стандарт застосовується до навчальних і реальних open-source research tasks, якщо для конкретної роботи не встановлено суворіші правила.

---

# 2. Методологічна основа

Стандарт використовує як core donor:

- **Berkeley Protocol on Digital Open Source Investigations** (OHCHR + Human Rights Center, UC Berkeley School of Law).

Внутрішній audit:

- `research/donors/berkeley-protocol.md`.

Додаткові шари нашої методології:

- systems thinking / territory mapping;
- hypothesis-driven investigation;
- competing hypotheses;
- statistical and cognitive-bias discipline;
- explicit confidence assessment;
- mandatory peer review for substantive findings;
- separate internal evidence/research package and audience-facing output.

Стандарт не є заміною Berkeley Protocol, українського законодавства, внутрішніх правил правоохоронного органу або професійної експертизи.

---

# 3. Нормативні слова

У документі:

- **MUST / ОБОВ’ЯЗКОВО** — вимога, без якої робота не проходить відповідний gate;
- **SHOULD / СЛІД** — стандартна практика; відхилення має бути пояснено;
- **MAY / МОЖНА** — допустима опція залежно від контексту.

---

# 4. Основне правило

> **Жоден висновок не може бути сильнішим за задокументований evidence trail, який його підтримує.**

З цього випливають п’ять заборон:

1. `знайдено` ≠ `перевірено`;
2. `перевірено` ≠ `доведено юридично`;
3. `належить до підрозділу` ≠ `був присутній`;
4. `був присутній` ≠ `виконав конкретну дію`;
5. `виконав дію` ≠ автоматичний юридичний висновок про відповідальність.

---

# 5. Мінімальний investigation lifecycle

Будь-яке substantively assessed дослідження MUST пройти такі етапи:

```text
0. Intake / scope
1. Research question
2. Territory & digital landscape mapping
3. Threat / risk / harm assessment
4. Working + competing hypotheses
5. Collection plan
6. Discovery / online inquiry
7. Preliminary assessment
8. Collection
9. Preservation
10. Verification: source + item + content
11. Data structuring / analysis preparation
12. Investigative analysis
13. Confidence + limitations
14. Peer review / red team
15. Corrections / response to review
16. Evidence/research package
17. Handoff and/or reporting
18. Retention / closure
```

Цикл є **ітеративним**. Новий факт MAY повернути дослідника до mapping, hypotheses, collection requirements або verification.

Повернення назад MUST бути відображене в research log, якщо воно суттєво змінило напрям або висновок.

---

# 6. Stage 0 — Intake / scope

До початку активної роботи MUST існувати case record.

Мінімальні поля:

- case ID;
- working title;
- owner/researcher;
- creation date/time;
- requester / intended audience, якщо є;
- subject matter;
- geographical scope;
- temporal scope;
- known constraints;
- sensitivity classification;
- expected output.

### Заборонено

Починати живий high-risk case як «погуглимо й подивимося», якщо відсутній хоча б базовий scope і threat assessment.

---

# 7. Stage 1 — Research question

Research question MUST:

- бути перевірюваним;
- мати визначений subject;
- мати часові/географічні межі, де це релевантно;
- не містити бажаної відповіді як передумову;
- дозволяти сформулювати stopping condition.

### Погано

> «Довести, що X скоїв злочин».

### Краще

> «Які відкриті дані дозволяють встановити місцезнаходження X у період Y та його задокументовану роль щодо події Z?»

---

# 8. Stage 2 — Territory & digital landscape mapping

До широкого collection SHOULD бути створена карта:

- actors/entities;
- institutions;
- systems of accountability;
- records/documents;
- platforms;
- databases;
- relevant languages/orthographies;
- potential source classes;
- known information gaps;
- excluded/underrepresented groups;
- platform/legal/technical constraints.

Результатом є **source map + initial collection requirements**.

Для України/Росії SHOULD окремо враховуватися:

- українська / російська орфографія;
- транслітерації;
- `е/ё`;
- попередні назви населених пунктів;
- перейменування інституцій;
- старі/нові позначення військових частин;
- регіональні платформи й локальні медіа.

---

# 9. Stage 3 — Threat, risk and harm assessment

До ризикової online activity MUST бути проведено threat/risk assessment.

Мінімальна структура:

| Action | Asset/person at risk | Threat actor | Vulnerability | Likelihood | Impact | Mitigation | Residual risk |
|---|---|---|---|---|---|---|---|

Окремо MUST оцінюватися harm, який може виникнути через:

- collection;
- contact;
- storage;
- sharing;
- publication;
- identification;
- aggregation of previously dispersed data.

### Gate

Якщо residual risk неприйнятний, дія MUST NOT виконуватися без escalation/approval.

---

# 10. Stage 4 — Hypotheses

Для substantively disputed питання MUST існувати:

- working hypothesis;
- щонайменше одна plausible competing hypothesis;
- evidence that would support each;
- evidence that would weaken/refute each;
- known gaps.

Форма:

| Hypothesis | Supporting indicators sought | Disconfirming indicators sought | Current evidence | Gaps | Status |
|---|---|---|---|---|---|

### Правило

Дослідник MUST активно шукати disconfirming information, а не лише матеріал на користь початкової версії.

---

# 11. Stage 5 — Collection plan

Collection plan MUST визначати:

- collection requirements;
- priority;
- source classes;
- method;
- expected risk;
- expected data type;
- collection profile;
- stopping/review point.

Collection plan SHOULD регулярно переглядатися.

---

# 12. Stage 6 — Discovery / online inquiry

Discovery включає:

- searching;
- monitoring;
- browsing known source ecosystems;
- structured queries;
- API/scraping where appropriate;
- archive research;
- document/database search.

### Research log MUST record

Для суттєвих пошукових дій:

- timestamp;
- researcher;
- system/source;
- query/parameters where reproducibility matters;
- result/relevance;
- next action.

Не потрібно логувати кожен випадковий click, якщо це не впливає на відтворюваність.

---

# 13. Stage 7 — Preliminary assessment

Перед collection digital item MUST пройти достатню preliminary assessment.

Перевіряється:

1. relevance;
2. potential probative/research value;
3. duplicative nature;
4. privacy/sensitivity;
5. data minimization;
6. collection safety;
7. volatility / risk of deletion;
8. legal/ethical restrictions known to researcher.

Рішення:

- `COLLECT`;
- `COLLECT WITH RESTRICTIONS`;
- `DO NOT COLLECT`;
- `ESCALATE`;
- `DEFER`.

### Ключове правило

> Discovery does not create an automatic duty to collect everything.

---

# 14. Stage 8 — Collection

Collection MUST прагнути зафіксувати digital item у native або максимально близькому до доступного original state форматі.

Будь-які transformations caused by collection SHOULD бути задокументовані.

## 14.1. Universal minimum

Для кожного substantive digital item MUST бути:

- unique object ID;
- source/location identifier (URL/URI/message reference/etc.);
- date/time of collection;
- collector;
- item type;
- collected file/capture;
- context sufficient to interpret the item;
- collection notes;
- integrity marker/hash for file-based objects where feasible and useful.

## 14.2. Web page profile

SHOULD include, where applicable:

- target URL;
- full-page capture;
- source/HTML capture;
- embedded media;
- embedded metadata;
- page title/account/source;
- publication timestamp;
- surrounding context;
- collection timestamp;
- hash(es) of collected files.

## 14.3. Social media / messenger profile

SHOULD include:

- platform;
- account/channel/group identifier;
- post/message identifier;
- permalink where available;
- displayed author/uploader;
- displayed publication time;
- message text;
- attachments in best available form;
- relevant reply/forward/context information;
- collection timestamp;
- screenshots only as supplementary representation where richer capture is available.

## 14.4. Image/video/document profile

SHOULD include:

- source page/context;
- best available file;
- filename as obtained;
- byte size;
- MIME/type;
- embedded metadata where available;
- collection hash;
- separate working copy before transformations.

---

# 15. Object identifiers

Рекомендований формат:

```text
CASEID-YYYYMMDD-TYPE-NNNN
```

Приклади:

```text
KYIV01-20260810-WEB-0001
KYIV01-20260810-VID-0002
KYIV01-20260810-DOC-0003
```

IDs MUST NOT кодувати неперевірені висновки типу `WARCRIMINAL-IVANOV`.

---

# 16. Stage 9 — Preservation

Collection і preservation MUST розглядатися як різні процеси.

Preservation system SHOULD підтримувати:

- authenticity;
- availability;
- identity;
- persistence;
- renderability;
- understandability.

## 16.1. Reference/evidence copy

Після collection SHOULD існувати незмінювана reference copy або еквівалентний контрольований original-state object.

## 16.2. Working copy

Будь-який аналіз, конвертація, frame extraction, transcription, annotation або enhancement MUST виконуватися на working copy, якщо це технічно можливо.

## 16.3. Transformation log

Для суттєвих transformations MUST записуватися:

- input object ID/hash;
- tool/version;
- operation;
- parameters;
- output filename/object ID;
- output hash;
- researcher;
- timestamp.

## 16.4. Chain of custody / handling history

Для матеріалів, які готуються до external handoff, SHOULD вестися chronological handling record.

Його юридичний статус у конкретному провадженні НЕ ПРИПУСКАЄТЬСЯ автоматично.

---

# 17. Stage 10 — Verification

Verification MUST розділяти:

```text
SOURCE
ITEM
CONTENT
```

## 17.1. Source analysis

Перевіряються, де релевантно:

- identity/status of source;
- proximity/access to event;
- publication history;
- motive/incentives;
- reliability indicators;
- account continuity;
- possibility of impersonation;
- independence from other sources.

## 17.2. Item analysis

Перевіряються:

- file identity;
- available metadata;
- format;
- signs/history of transformations;
- earliest available version;
- technical consistency;
- relation between collected copy and claimed source.

## 17.3. Content analysis

Перевіряються:

- what can actually be seen/heard/read;
- internal consistency;
- location;
- time;
- language/signage;
- environmental indicators;
- external corroboration;
- contradiction with other established facts.

### Заборонено

Одне твердження `VERIFIED = YES` без пояснення, що саме було перевірено.

---

# 18. Verification status

Рекомендовані стани digital item:

- `UNASSESSED`;
- `PARTIALLY VERIFIED`;
- `VERIFIED FOR SPECIFIED CLAIM`;
- `CONTRADICTED`;
- `MISCONTEXTUALIZED`;
- `INSUFFICIENT DATA`;
- `EXCLUDED`.

`VERIFIED FOR SPECIFIED CLAIM` MUST супроводжуватися формулюванням claim.

Наприклад:

> `Verified for claim: video was recorded at intersection X no later than date Y.`

Це не означає verification усіх тверджень, пов’язаних із відео.

---

# 19. Geolocation standard

Geolocation finding SHOULD:

- містити щонайменше кілька незалежних spatial indicators;
- не рахувати один і той самий feature двічі під різними назвами;
- перевіряти plausible alternative locations;
- фіксувати map/satellite/source dates;
- відрізняти exact point від bounded area;
- мати confidence.

Для high-confidence exact geolocation рекомендовано мінімум **три незалежні сильні ознаки**, але це не механічна математична гарантія.

---

# 20. Chronolocation standard

Chronolocation SHOULD:

- відрізняти upload/publication time від event time;
- формувати lower/upper bounds;
- документувати погодні/тіньові/сезонні/супутникові clues;
- враховувати clock/timezone uncertainty;
- уникати exact time, якщо data підтримують лише range.

---

# 21. Stage 11 — Data structuring and hygiene

Raw data MUST зберігатися окремо від processed data.

Normalization MUST бути documented.

Для entity resolution SHOULD фіксуватися:

- source records;
- normalization rule;
- match indicators;
- conflicting indicators;
- false merge risk;
- false split risk;
- final decision + confidence.

Усі derived datasets SHOULD мати provenance до raw inputs.

---

# 22. Automated collection / AI / scripts

## 22.1. Automation

API, scraper, regex, script або інший automated process MUST мати:

- purpose;
- source/endpoint;
- date/time;
- code/version or reproducible configuration;
- parameters;
- pagination/range limitations;
- error handling notes;
- validation sample;
- known false-positive/false-negative risks.

## 22.2. AI use

Generative AI MAY використовуватися для:

- translation assistance;
- transcription assistance;
- entity extraction suggestions;
- clustering/classification drafts;
- query expansion;
- code assistance;
- contradiction discovery prompts.

AI output MUST NOT бути самостійним джерелом факту.

Критичні claims MUST посилатися на underlying sources, а не на model output.

AI-assisted transformations SHOULD бути зазначені, якщо вони впливають на analysis trail.

---

# 23. Stage 12 — Investigative analysis

Analysis MUST починатися з verified/qualified observations, а не з narrative conclusion.

Для кожного substantive finding SHOULD бути claim record:

| Claim ID | Claim | Supporting items | Contradicting items | Alternative explanations | Confidence | Reviewer status |
|---|---|---|---|---|---|---|

### Аналіз MUST

- розрізняти observation / indicator / inference / conclusion;
- включати contradicting evidence;
- розглядати competing hypotheses;
- позначати inferential gaps;
- створювати new collection requirements, якщо gaps критичні.

---

# 24. Attribution ladder

Для person/unit/action attribution MUST використовуватися рівні:

```text
1. Identity / membership
2. Presence
3. Participation / functional involvement
4. Specific individual action
5. Legal responsibility
```

Перехід на наступний рівень MUST мати окремий evidence basis.

### Rule

Evidence for level 1 MUST NOT автоматично використовуватися як proof of levels 3–5.

Level 5 у рамках курсу зазвичай формулюється лише як **питання для юридичної оцінки**, якщо немає окремої експертної/процесуальної основи.

---

# 25. Stage 13 — Confidence

Курс використовує чотирирівневу якісну шкалу.

## HIGH CONFIDENCE

Висновок підтримується кількома сильними, переважно незалежними evidence lines; ключові alternatives перевірено; суттєвих невирішених суперечностей немає.

## MODERATE CONFIDENCE

Evidence переважно підтримує висновок, але існують meaningful gaps, dependency між джерелами або plausible alternatives, які не вдалося повністю виключити.

## LOW CONFIDENCE

Існують певні supporting indicators, але data sparse/weak, alternatives залишаються сильними або source/item reliability суттєво обмежена.

## INSUFFICIENT FOR CONCLUSION

Наявні дані не дозволяють професійно обрати одну версію або сформулювати substantively useful finding.

### Заборонено

Не перетворювати цю шкалу автоматично на точні відсотки.

Confidence MUST оцінюватися **для конкретного claim**, а не один раз для всього case.

---

# 26. Stage 14 — Limitations and unresolved questions

Кожен substantive report MUST мати:

## Limitations

- source limitations;
- access limitations;
- platform limitations;
- dataset completeness;
- technical limitations;
- temporal/geographic gaps;
- expertise limits;
- potential bias.

## Unresolved questions

Окремий список питань, які залишилися без достатньої відповіді.

Невирішене питання MUST NOT маскуватися як weakly worded assertion.

---

# 27. Stage 15 — Peer review / red team

Substantive capstone/high-risk findings MUST пройти independent review.

Reviewer SHOULD перевірити:

1. reproducibility;
2. source independence;
3. verification logic;
4. contradicting evidence;
5. competing hypotheses;
6. inferential gaps;
7. confidence;
8. safety/ethical issues;
9. wording of conclusions;
10. evidence-to-claim traceability.

Reviewer MUST мати доступ до достатнього evidence package, а не лише до фінального тексту.

---

# 28. Stage 16 — Correction protocol

Після review researcher MUST:

- accept;
- reject with reason;
- partially accept;
- request additional collection.

Суттєві corrections MUST фіксуватися.

Якщо помилка вже була публічно поширена, SHOULD існувати correction mechanism відповідно до контексту.

Приховування відомої суттєвої помилки є critical failure.

---

# 29. Stage 17 — Evidence/research package

Мінімальна структура:

```text
CASE-ID/
├── 00_admin/
│   ├── scope.md
│   ├── threat-model.md
│   └── harm-assessment.md
├── 01_plan/
│   ├── territory-map.*
│   ├── hypotheses.*
│   └── collection-plan.*
├── 02_raw/
│   └── <collected objects>
├── 03_metadata/
│   ├── object-register.*
│   └── collection-log.*
├── 04_working/
│   └── <working copies>
├── 05_analysis/
│   ├── verification.*
│   ├── timeline.*
│   ├── network.*
│   └── claim-matrix.*
├── 06_review/
│   ├── peer-review.*
│   └── response-to-review.*
└── 07_output/
    ├── analytical-memo.*
    ├── limitations.*
    └── public-or-handoff-package.*
```

Конкретна storage architecture MAY відрізнятися, якщо зберігаються ті самі функції й traceability.

---

# 30. Stage 18 — Handoff / reporting

Перед зовнішнім handoff MUST бути зрозуміло:

- хто recipient;
- для якої purpose передається material;
- які limitations;
- які sensitivity restrictions;
- які source-protection issues;
- що є raw material, що analysis, що inference;
- що не було юридично оцінено.

## Public report

Публічний текст SHOULD:

- посилатися на evidence trail настільки, наскільки це безпечно;
- не розкривати зайві sensitive data;
- не перебільшувати confidence;
- відділяти fact від analysis;
- містити methodological note для складних висновків.

## Legal-use disclaimer

До окремої української юридичної валідації заборонено стверджувати, що відповідність цьому стандарту автоматично робить матеріал процесуально допустимим доказом.

---

# 31. Sensitive / high-risk categories

Додатковий review/approval REQUIRED для навчальних або реальних кейсів, що стосуються:

- survivors of torture;
- conflict-related sexual violence;
- children;
- prisoners of war;
- active military operations;
- non-public suspected perpetrators;
- protected witnesses/sources;
- doxxing risk;
- medical data;
- data that may identify vulnerable relatives;
- material whose publication may expose positions or operational patterns.

Студентам без спеціальної підготовки MUST NOT доручатися пряме interviewing vulnerable survivors як частина звичайної OSINT-лабораторної.

---

# 32. Tool validation

Новий інструмент MUST NOT автоматично ставати частиною official workflow лише тому, що він працює в demo.

Перед використанням у pilot-ready module SHOULD бути перевірено:

- developer/source;
- current availability;
- input/output behaviour;
- data handling/privacy;
- reproducibility;
- known error modes;
- rate/coverage limits;
- security concerns;
- independent spot checks;
- replacement path if service disappears.

Курс навчає method; tool is implementation.

---

# 33. Quality gates

## Gate A — Search-ready

Потрібні:

- scope;
- research question;
- territory/digital landscape;
- threat/harm assessment proportional to risk;
- hypotheses;
- collection plan.

## Gate B — Analysis-ready

Потрібні:

- object register;
- collection/provenance data;
- preservation controls;
- verification status;
- cleaned/structured data where needed.

## Gate C — Finding-ready

Потрібні:

- claim matrix;
- supporting + contradicting evidence;
- alternatives;
- confidence;
- limitations.

## Gate D — Publication/handoff-ready

Потрібні:

- peer review;
- response/corrections;
- sensitivity review;
- final evidence/research package;
- audience-appropriate output.

---

# 34. Critical failures

Незалежно від загального quality score робота може бути rejected, якщо виявлено:

- fabricated source or data;
- intentional concealment of contradictory evidence;
- undocumented material alteration presented as original state;
- reckless exposure of protected/sensitive person;
- unjustified identification/accusation of a real private person;
- deliberate bypass of required safety gate;
- legal conclusion presented as established despite known competence limits;
- inability to trace central finding to evidence.

---

# 35. Minimum templates required

Стандарт передбачає створення:

- `investigation-plan.md`;
- `territory-map` template;
- `digital-landscape.md`;
- `threat-model.md`;
- `harm-assessment.md`;
- `hypothesis-matrix`;
- `collection-plan`;
- `digital-object-card`;
- `collection-log`;
- `transformation-log`;
- `verification-sheet`;
- `geolocation-sheet`;
- `chronolocation-sheet`;
- `entity-resolution-sheet`;
- `claim-matrix`;
- `confidence-assessment`;
- `peer-review-form`;
- `handoff-index`.

Templates повинні розроблятися після цього standard, а не навпаки.

---

# 36. Relationship to course assessment

Critical competencies mapped to this standard:

- C05 — provenance/preservation/reproducibility;
- C13 — analysis/confidence/attribution;
- C15 — ethics/harm;
- C16 — security;
- C17 — documentation/handoff.

Failure on one of these MAY make capstone non-passing regardless of technical search quality.

---

# 37. External review requirements

До `v1.0` standard SHOULD пройти щонайменше:

1. digital open-source investigator review;
2. security review;
3. Ukrainian criminal-procedure review;
4. international crimes / IHL review for U04/U05;
5. trauma-informed review for vulnerable-person workflows.

Експертам слід надавати цей конкретний standard + templates + sample case, а не просити «розказати, як правильно робити OSINT».

---

# 38. Known limitations of v0.1

Не завершено:

- українська legal terminology;
- process-specific admissibility requirements;
- retention/deletion schedule;
- classification levels for sensitive data;
- formal incident-response procedure;
- detailed psychosocial safety protocol;
- cryptographic/storage implementation standard;
- policy for virtual identities;
- detailed contact/source interaction protocol.

Ці прогалини є documented limitations, а не implicit assumptions.

---

# 39. Versioning

Кожна зміна MUST фіксуватися в `CHANGELOG.md`.

Major methodological changes SHOULD підвищувати minor version:

- `0.1 → 0.2`.

Editorial corrections MAY не змінювати version, якщо не впливають на procedure.

Після external validation і pilot testing standard може перейти до `1.0`.

---

# 40. Definition of Done для v0.2

Для переходу до v0.2 потрібно:

- створити й протестувати core templates;
- провести L03 Telegram source-tracing lab;
- застосувати standard до одного historical case end-to-end;
- виконати internal peer review;
- завершити Berkeley legal-framework audit;
- перевірити WITNESS/Mnemonic preservation and video guidance;
- зафіксувати всі procedure failures, знайдені під час тесту.
