# Paul Bradshaw — MED7369 Specialist Journalism, Investigations and Coding

**Автор:** Paul Bradshaw  
**Організаційний контекст:** Birmingham City University, MA in Data Journalism / journalism programmes  
**Репозиторій:** `paulbradshaw/MED7369-Specialist-Investigative-Journalism`  
**Перевірено:** 2026-08-10  
**Статус аудиту:** `PARTIAL-REVIEWED` — README + file-level review ключових network analysis, cleaning, Python/scraping, accounts та storytelling матеріалів; statistics/notebooks і частина exercises ще потребують окремого проходу.

---

## 1. Чому це корисний donor

MED7369 цінний не як готовий OSINT-курс, а як приклад навчання investigative journalism через системне мислення, формулювання гіпотез, картування джерел і зв’язків, роботу з даними, автоматизацію та самостійний проєкт.

Для нашого курсу особливо важливий принцип:

> **спочатку зрозуміти систему та дослідницьке питання, потім обирати інструмент.**

Це протилежність типовій побудові OSINT-курсів як каталогу сервісів.

---

## 2. Заявлена структура, релевантна нашому курсу

За README репозиторію виділено:

- systems thinking та `Mapping the territory`;
- story / hypothesis та Story-Based Inquiry;
- systems of accountability, documents, data, FOI;
- company accounts / following the money;
- network analysis та OSINT;
- APIs;
- scraping;
- statistics та cognitive bias;
- text as data, grep / regex;
- cleaning data / OpenRefine;
- project-driven learning та production weeks;
- longform / investigative storytelling.

---

# 3. File-level review

## 3.1. `networkanalysis/readme.md`

Bradshaw визначає network analysis як інструмент **двох різних етапів**:

1. planning investigation — mapping networks and identifying actors;
2. storytelling — showing patterns / allowing audience exploration.

Це важливе розділення для нашого curriculum.

### Рішення

`ADOPT + EXPAND`.

У нашому M15 network graph спочатку є **аналітичним об’єктом з provenance**, а лише потім може стати public visualisation.

Не оцінюємо студента за красою графа.

---

## 3.2. `networkanalysis/kumuexercise.md`

Найцінніша частина вправи — не Kumu UI, а **data model** з двох таблиць:

### Entities / nodes

Типові поля:

- name / label;
- type;
- description / URL / address;
- tags;
- інші attributes.

### Relationships / connections

Типові поля:

- from;
- to;
- direction;
- relationship type;
- quantitative dimension;
- description;
- tags.

Bradshaw також показує, що одна й та сама структура може бути використана в Kumu, JSON/R, NodeXL, Gephi, Neo4j тощо.

### Curriculum decision

**Беремо data model, не UI.**

Наш мінімальний `edges` schema має бути суворішим:

```text
edge_id
from_entity
from_entity_id
to_entity
to_entity_id
relationship_type
direction
observed_or_inferred
source_object_id
valid_from
valid_to
quantitative_value
confidence
notes
```

Додаємо те, чого журналістському visualisation exercise не вистачає для evidence-first роботи:

- source;
- temporal validity;
- observed vs inferred;
- confidence;
- stable entity IDs.

### Tool policy

Kumu / Gephi / NodeXL / Neo4j / Flourish — лише replaceable implementations.

Студент повинен розуміти network data незалежно від конкретного інтерфейсу.

---

## 3.3. `cleaning/readme.md`

Це один із найкорисніших file-level donors.

Bradshaw послідовно розбирає:

- whitespace / capitalisation / formatting;
- XML/JSON import;
- clustering similar values;
- multiple clustering algorithms;
- combining files/sheets;
- malformed/multi-row headings;
- blank rows;
- faceting;
- separating mixed semantic types inside one column;
- fill-down / reshaping;
- regex / converted-PDF cleanup.

### Особливо важлива методична деталь

У clustering вправі студенту прямо пропонується **не зливати всі схожі значення автоматично**: наприклад, два схожих restaurant/business names можуть бути різними businesses.

Це майже готовий педагогічний міст до нашого:

- false merge;
- false split;
- entity resolution;
- manual review of automated suggestions.

### Curriculum decision

`ADOPT METHOD + EXPAND AUDIT TRAIL`.

Нам потрібна L08 `Dirty Entities`, де студент:

1. отримує raw records;
2. робить normalization proposals;
3. позначає automated suggestions;
4. приймає / відхиляє merge;
5. документує rule;
6. зберігає raw values;
7. перевіряє false merge/split risk.

OpenRefine MAY бути одним із інструментів, але laboratory MUST бути solvable іншим current tool / code path.

---

## 3.4. `python/readme.md` + scraper notebook inventory

Python layer містить:

- basic programming concepts;
- Google Colab/Jupyter workflow;
- simple one-page scraping;
- list extraction;
- multiple-item extraction;
- pagination / next-page scraping;
- APIs;
- historical Morph.io / ScraperWiki-era materials;
- separate discussion of scraping law.

### Що беремо

Педагогічну прогресію:

```text
one request
→ one item
→ list of items
→ multiple fields
→ pagination
→ structured output
→ validation
```

Вона дуже придатна для M16.

### Що перебудовуємо

`REBUILD` technical implementation.

Причини:

- частина notebook/tool ecosystem історична;
- Morph.io / ScraperWiki-specific workflow не повинен ставати curriculum dependency;
- сучасний course pipeline має логувати parameters, coverage, errors і validation sample;
- студенту не обов’язково ставати Python developer.

### Наша learning outcome

> Дослідник здатний зрозуміти, коли ручний collection не масштабується, сформулювати автоматизовану процедуру, запустити/адаптувати простий pipeline і перевірити його результат на coverage та errors.

---

## 3.5. `accounts/readme.md`

Company accounts block значно ширший за «читання балансу». Він показує accounts/records як частину **institutional source ecosystem**:

- company growth/decline;
- conflicts of interest;
- related-party relationships;
- money transfers;
- directors/shareholders;
- expenditure;
- financial narrative over time;
- declarations of interest;
- APIs/data-format versions of institutional records;
- cross-checking public claims against records.

### Curriculum decision

Не робити окремий великий UK company-accounts module у core.

`ADAPT` до M13:

> **Institutional records & systems of accountability**.

Для українського/російського specialization потрібні свої класи реєстрів, а не переклад Companies House exercise.

### Потенційний advanced elective

`Follow the money / corporate OSINT` може пізніше стати окремою спеціалізацією.

---

## 3.6. `storytelling.md`

Матеріал детально розбирає narrative structures, plots, human entry points, climax/right of reply, resolution/coda та longform construction.

### Корисне для нас

- investigation може мати різні narrative forms;
- story structure допомагає audience comprehension;
- right of reply / confrontation with responsible actors важливі для journalistic output;
- human case study може пояснювати системну проблему;
- ending має показувати what happens next.

### Ризик для evidence-first OSINT

Narrative structure може створювати **pressure to force evidence into a satisfying plot**.

Тому storytelling MUST з’являтися **після**:

```text
provenance
→ verification
→ analysis
→ confidence
→ peer review
```

### Curriculum decision

`ADAPT` лише в M20.

Вводимо rule:

> Story structure may organise presentation, but MUST NOT organise factual inclusion/exclusion in the evidence package.

Public narrative і internal evidence package — різні продукти.

---

# 4. Що це вже змінило в нашому Curriculum Blueprint

## 4.1. Systems thinking moved before tools

До пошуку студент описує:

- actors;
- institutions;
- records;
- accountability systems;
- source ecosystems;
- digital traces;
- gaps.

Це інтегровано в M02.

## 4.2. Network analysis separated into data model and visualisation

В M15 student learns:

1. entities;
2. relationships;
3. source-backed edges;
4. temporal validity;
5. observed vs inferred;
6. confidence;
7. only then visualisation.

## 4.3. Data cleaning upgraded to evidence discipline

M14 тепер має raw/processed separation, transformation log та entity-resolution controls.

## 4.4. Automation is professional scaling, not “Python class”

M16 побудовано навколо reproducible collection/extraction + validation, а не syntax mastery.

## 4.5. Statistics + cognitive bias remain a separate analytical block

Повний statistics file-level review ще попереду, але README already justifies dedicated M17.

## 4.6. Storytelling explicitly comes after evidence package

Bradshaw storytelling is retained as communication method, not investigative truth engine.

---

# 5. Рішення щодо компонентів

| Component | Decision | Curriculum |
|---|---|---|
| Systems thinking | `ADOPT` | M02 |
| Territory mapping | `ADAPT` | M02 |
| Story/hypothesis inquiry | `ADAPT` | M03 + M18 |
| Systems of accountability | `EXPAND` | M13 + U01 |
| Company accounts | `ADAPT` | M13 / future elective |
| Network data model | `ADOPT + EXPAND` | M15 |
| Kumu/Gephi/NodeXL/Neo4j UI | `OPTIONAL IMPLEMENTATION` | M15 |
| APIs | `REBUILD` | M16 |
| Scraping | `REBUILD` | M16 |
| Python fundamentals | `MINIMAL / JUST-IN-TIME` | M16 |
| Statistics | `EXPAND` | M17 |
| Cognitive bias | `EXPAND` | M17–M19 |
| Text as data / regex | `EXPAND` | M16 |
| Data cleaning concepts | `ADOPT + EXPAND` | M14 |
| OpenRefine UI | `OPTIONAL IMPLEMENTATION` | M14 |
| Production/project weeks | `ADOPT` | pilot + capstone |
| Storytelling | `ADAPT AFTER EVIDENCE` | M20 |

---

# 6. Labs derived from Bradshaw donor

## L01 — Territory Map

System / source ecosystem / gaps / collection requirements.

## L08 — Dirty Entities

Raw values → clustering suggestions → manual merge decisions → audit log → false merge/split analysis.

## L09 — Sourced Network

Two-table model:

- entities;
- relationships.

But every relationship MUST carry source, observed/inferred status and temporal validity.

## L10 — Text as Data

Reproducible extraction + false-positive validation.

## L11 — Numbers Can Lie

Dataset/claim critique with denominator, aggregation and selection problems.

---

# 7. Technical freshness assessment

## Stable concepts

High confidence these remain pedagogically useful:

- entities/relationships data model;
- systems thinking;
- source/accountability mapping;
- cleaning/normalisation;
- clustering as suggestion rather than truth;
- faceting/grouping;
- scraping progression;
- notebook-as-reproducible-work habit;
- narrative after reporting evidence.

## Time-sensitive implementation

Must be revalidated before use:

- Kumu UI;
- NodeXL;
- Gephi version-specific steps;
- Neo4j/Panama Papers setup;
- Flourish;
- OpenRefine UI/menu details;
- Colab/Jupyter setup;
- Morph.io / ScraperWiki historical workflows;
- API endpoints;
- UK registry links;
- external tutorials.

---

# 8. Remaining review work

Потрібно ще окремо пройти:

- statistics folder/files;
- selected Python notebooks at code level;
- `python/scrapinglaw.md` only as historical/legal donor, not current Ukrainian guidance;
- selected network exercises (`taxpayersalliance`, Neo4j etc.) for lab design;
- `accounts/keypoints.md`;
- licence status of repository and embedded/external materials;
- exercises/data licensing.

Після цього статус можна підняти до `REVIEWED`.

---

# 9. Поточний висновок

**Рівень корисності:** високий як pedagogical donor.  
**Пряме використання матеріалів:** обмежене.  
**Методи, які вже інтегровані:** systems thinking, territory mapping, hypothesis inquiry, two-table network model, data cleaning/entity-resolution caution, automation progression, statistics/bias layer, project-driven learning, storytelling-after-evidence.

Bradshaw дає нам **педагогічний скелет журналістського розслідування**. Berkeley Protocol дає **процесуальну дисципліну digital open source investigation**. Наш курс має залишатися їх синтезом, а не копією будь-якого з них.
