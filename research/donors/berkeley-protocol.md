# Berkeley Protocol on Digital Open Source Investigations — core audit

**Організації:** United Nations Office of the High Commissioner for Human Rights (OHCHR) + Human Rights Center, UC Berkeley School of Law  
**Документ:** *Berkeley Protocol on Digital Open Source Investigations: A Practical Guide on the Effective Use of Digital Open Source Information in Investigating Violations of International Criminal, Human Rights and Humanitarian Law*  
**Офіційна сторінка:** https://humanrights.berkeley.edu/publications/berkeley-protocol-on-digital-open-source-investigations/  
**Офіційний PDF:** https://humanrights.berkeley.edu/wp-content/uploads/archive/2024/02/Berkeley-Protocol.pdf  
**Перевірено:** 2026-08-10  
**Статус аудиту:** `CORE-REVIEWED` — перевірено структуру, principles, security/preparation, investigation process, collection/preservation/verification/analysis і annex templates; legal framework потребує окремого юридичного аудиту.

---

## 1. Чому це фундаментальний donor

Berkeley Protocol не є каталогом OSINT-інструментів. Він задає професійні, методологічні, етичні, безпекові та процесуальні стандарти digital open source investigation у контексті міжнародного кримінального, гуманітарного та правозахисного документування.

Для нашого курсу це означає: Protocol слід використовувати не як один спеціальний модуль наприкінці, а як **несучу методологічну рамку**, що проходить через foundations, safety, preservation, verification, analysis, reporting і Ukraine–Russia–War specialization.

---

# 2. Структура Protocol, релевантна curriculum

У документі виділено:

1. Introduction;
2. Principles;
3. Legal Framework;
4. Security;
5. Preparation;
6. Investigation Process;
7. Reporting on Findings;
8. Glossary;
9. Annexes з робочими шаблонами.

У розділі `Investigation Process` визначено шість основних фаз:

1. `online inquiry`;
2. `preliminary assessment`;
3. `collection`;
4. `preservation`;
5. `verification`;
6. `investigative analysis`.

Protocol прямо підкреслює, що цей цикл не є жорстко лінійним і може повторюватися багато разів під час case-building.

### Curriculum decision

**`ADOPT`** як базову процесну рамку, але додати наші попередні етапи:

`research question → territory mapping → competing hypotheses → threat/harm assessment → Protocol investigation cycle → peer review → evidence package / reporting`.

Таким чином, Berkeley cycle стає ядром операційної частини нашої ширшої evidence-first моделі.

---

# 3. Professional, methodological and ethical principles

Protocol розділяє принципи на три групи.

## 3.1. Professional principles

Для курсу критичні:

- accountability;
- competence;
- objectivity;
- legality;
- security awareness.

### Curriculum implication

Це підтверджує, що професійність не може оцінюватися лише за успішністю пошуку. У certification gate мають входити accountability, competence boundaries, objectivity і security.

**Цільові модулі:** M01, M04, M18, M19, M20.

---

## 3.2. Methodological principles

Protocol називає серед мінімальних принципів:

- accuracy;
- data minimization;
- data preservation;
- security by design.

### Curriculum implication

`Data minimization` необхідно зробити явною вимогою всього курсу, а не лише privacy/ethics темою.

`Preservation` не є просто технічною операцією архівування: вона співіснує з minimization, тому дослідник повинен одночасно уникати і бездумного over-collection, і втрати потенційно релевантного матеріалу.

**Цільові модулі:** M04, M05, M06, M12, M14, M20, U04–U05.

---

## 3.3. Ethical principles

Перевірений core включає, зокрема:

- dignity;
- humility;
- inclusivity;
- інші пов’язані етичні вимоги Protocol.

Особливо важливий для нашої моделі принцип **humility**: дослідник повинен усвідомлювати межі власних знань, звертатися до експертів за необхідності, визнавати та виправляти помилки.

### Curriculum implication

Наше правило `what the material does not allow us to claim` є не стилістичною звичкою, а частиною професійної етики.

Потрібно додати до rubric:

- recognition of competence limits;
- documented corrections;
- escalation to subject-matter expert;
- confidence downgrade after valid challenge.

**Цільові компетентності:** C13–C17.

---

# 4. Security before investigation

Protocol розглядає security як підготовчу умову, а не окремий набір «безпечних інструментів».

Ключові рішення:

- risk assessment до початку online investigative activities;
- регулярне оновлення assessment;
- security at organization / investigation / task level;
- infrastructure + user behaviour;
- protection measures відповідно до конкретних threats and vulnerabilities;
- digital, physical and psychosocial dimensions.

### Curriculum decision

**`ADOPT + EXPAND`**.

M04 має бути gate-модулем перед живими або ризиковими кейсами.

У студентській роботі threat model повинен бути пов’язаний з конкретними діями:

| Planned action | Threat | Vulnerability | Potential harm | Mitigation | Residual risk |
|---|---|---|---|---|---|

Не приймається універсальна анкета без прив’язки до кейсу.

---

# 5. Preparation

Protocol до початку основного investigation process передбачає:

- digital threat and risk assessment;
- digital landscape assessment;
- online investigation plan;
- resilience plan and self-care;
- data policies and tools.

### 5.1. Digital landscape assessment

Цей елемент особливо добре поєднується з Bradshaw `mapping the territory`.

Bradshaw допомагає відповісти:

> Яка система породжує інформаційні сліди?

Berkeley додає:

> Яким є цифровий ландшафт, доступність, representativeness, ризики, платформи, закони та технічні умови?

### Curriculum decision

Об’єднати у M02 дві рамки:

`systems/territory map + digital landscape assessment`.

Для U01 ця зв’язка повинна бути адаптована до конкретного українського/російського регіону та платформи.

---

## 5.2. Resilience and self-care

Protocol окремо враховує вторинну травматизацію від тривалої роботи з graphic/traumatic material і рекомендує планування resilience до початку роботи.

### Curriculum decision

Це не факультативний welfare-блок.

Додати до M04:

- exposure planning;
- graphic-content handling;
- work/rest limits;
- team buddy / paired work where appropriate;
- escalation when exposure affects judgement or security.

Детальні trauma-informed процедури мають бути зовнішньо рецензовані.

---

# 6. Preliminary assessment before collection

Одна з найкорисніших для нашого курсу деталей: між `discovery` і `collection` Protocol ставить окрему **preliminary assessment**.

Її сенс — вирішити, чи слід матеріал взагалі збирати, з урахуванням:

- relevance;
- focused investigation;
- data minimization;
- privacy;
- safety;
- ризику втрати матеріалу.

### Curriculum correction

У поточному Blueprint цикл був надто простим:

`search → preservation`.

Потрібно зафіксувати:

`discovery → preliminary assessment → collection → preservation`.

Це важлива відмінність: **знайшов ≠ повинен збирати**.

---

# 7. Collection standard

Protocol рекомендує збирати digital material у native format або максимально близькому до оригінального стані та документувати зміни, спричинені collection process.

Для web content сильна основа включає, залежно від контексту:

- target URL/URI;
- source code where applicable;
- full-page capture;
- embedded media;
- embedded metadata;
- contextual data;
- collection data;
- hash value.

Collection data може включати collector, timestamp, technical environment/identity details та інші параметри, релевантні автентифікації.

### Curriculum decision

**`ADOPT`**, але не перетворювати список Protocol на механічну вимогу для кожного типу об’єкта.

Створити типові `collection profiles`:

- webpage;
- social media post;
- Telegram message;
- image;
- video;
- document;
- structured dataset.

Кожен profile визначає minimum + optional context.

---

# 8. Preservation

Protocol відрізняє collection від preservation.

Мета preservation — підтримувати матеріал так, щоб він залишався доступним, автентичним і придатним для подальшого використання.

Для довготривалого збереження Protocol виділяє властивості digital item:

- authenticity;
- availability;
- identity;
- persistence;
- renderability;
- understandability.

Також окремо розглядається chain of custody як хронологічне документування контролю, передачі, аналізу та disposition матеріалу.

### Curriculum decision

M05 треба будувати не навколо команди `sha256sum`, а навколо шести preservation properties.

Hash — лише один із механізмів підтримки integrity/authenticity, а не магічний сертифікат «це доказ».

---

# 9. Verification

Protocol визначає verification як встановлення accuracy/validity online-collected information та розділяє її на три взаємопов’язані рівні:

1. source;
2. digital item/file;
3. content.

### Curriculum decision

Це має стати єдиною verification model для M06–M11.

Для будь-якого media verification student sheet має містити три окремі секції:

```text
SOURCE
- who/what published it?
- credibility / reliability indicators
- proximity to event
- motive / access / history

ITEM
- file identity
- metadata
- transformations
- technical integrity indicators

CONTENT
- what is visibly/audibly established?
- location/time
- internal consistency
- external corroboration
```

Студент не повинен змішувати «цей акаунт надійний» з «цей конкретний файл правдивий».

---

# 10. Investigative analysis

Protocol визначає investigative analysis як інтерпретацію factual information для substantive findings, decision-making/case-building і виявлення прогалин для подальшого дослідження.

Особливо важливо: цикл повертається назад, коли analysis показує gaps.

### Curriculum decision

Підтверджено архітектуру M18:

`verified observations → analysis → findings → gaps → new collection requirements`.

Competing hypotheses і confidence language є нашими додатковими дисциплінуючими шарами поверх Protocol, а не заміною його процесу.

---

# 11. Reporting and peer review

Protocol має окремий розділ reporting on findings і вказує на користь peer review для accuracy/quality залежно від context/confidentiality.

### Curriculum decision

M19 + M20 залишаються окремими модулями.

Reporting не повинен бути початком побудови «історії». Він є продуктом уже збереженого, перевіреного й проаналізованого evidence trail.

---

# 12. Annexes — майже готові прототипи наших форм

Protocol містить:

- Annex I — Online Investigation Plan Template;
- Annex II — Digital Threat and Risk Assessment Template;
- Annex III — Digital Landscape Assessment Template;
- Annex IV — Online Data Collection Form;
- Annex V — Considerations for Validating New Tools.

### Curriculum decision

Не копіювати annexes сліпо.

Використати їх як benchmark для наших:

- `templates/investigation-plan.md`;
- `templates/threat-model.md`;
- `templates/digital-landscape.md`;
- `templates/digital-object-card.md`;
- `templates/tool-validation.md`.

Кожна наша форма має містити traceability до відповідного Protocol annex і пояснення, де саме ми адаптували її для навчальної/української практики.

---

# 13. Що Berkeley змінює в Blueprint v0.1

## Обов’язкові зміни для v0.2

1. Явно вставити `preliminary assessment` між discovery і collection.
2. Додати `digital landscape assessment` до M02.
3. Додати resilience/self-care до M04.
4. У M05 розрізнити collection і preservation.
5. Побудувати preservation навколо authenticity / availability / identity / persistence / renderability / understandability.
6. Побудувати verification modules навколо `source + item + content`.
7. Додати data minimization як наскрізний criterion.
8. Додати `tool validation` до Definition of Done технічних модулів.
9. У capstone вимагати preliminary collection decision для sensitive/irrelevant material.
10. Зберегти наші додаткові шари: territory mapping, competing hypotheses, confidence, peer review, explicit limitations.

---

# 14. Що Protocol не вирішує за нас

Protocol не повинен використовуватися як підстава стверджувати, що:

- будь-який матеріал, зібраний за його процедурою, автоматично є допустимим доказом у конкретному українському кримінальному провадженні;
- OSINT-дослідник може самостійно встановити юридичну відповідальність;
- одна універсальна security configuration підходить усім;
- технічне виконання collection form замінює source/content verification;
- міжнародний framework автоматично враховує всі норми українського процесуального права.

Ці питання потребують окремої зовнішньої юридичної валідації.

---

# 15. Статус використання в курсі

| Component | Decision | Curriculum |
|---|---|---|
| Professional principles | `ADOPT` | M01, M18–M20 |
| Methodological principles | `ADOPT` | entire core |
| Ethical principles | `ADOPT + EXPAND` | M01, M04, M12, U04 |
| Security framework | `ADOPT + ADAPT` | M04 |
| Digital threat/risk assessment | `ADOPT` | M04 |
| Digital landscape assessment | `ADOPT + MERGE` | M02 + U01 |
| Investigation plan | `ADOPT + ADAPT` | M03 |
| Resilience/self-care | `ADOPT`, external review | M04 |
| Six-phase investigation cycle | `ADOPT` | course backbone |
| Preliminary assessment | `ADOPT` | M05/M06 boundary |
| Collection model | `ADOPT + ADAPT` | M05 |
| Preservation model | `ADOPT` | M05 |
| Verification: source/item/content | `ADOPT` | M06–M11 |
| Investigative analysis | `ADOPT + EXPAND` | M18 |
| Reporting | `ADOPT + ADAPT` | M20 |
| Annex templates | `ADAPT` | templates/ |
| Legal framework | `REVIEW REQUIRED` | U04–U05 |

---

# 16. Audit scope / next review

`CORE-REVIEWED` не означає завершеного юридичного аудиту всіх 102 сторінок.

Наступний review pass має окремо пройти:

- Chapter III — Legal Framework;
- privacy/data protection implications for Ukrainian course practice;
- virtual identities / misrepresentation;
- data retention/deletion/sharing policies;
- reporting details;
- Annex V tool validation;
- порівняння з українським кримінальним процесом через зовнішнього експерта.

Після цього статус може бути підвищено до `REVIEWED`.
