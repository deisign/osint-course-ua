# Paul Bradshaw — MED7369 Specialist Journalism, Investigations and Coding

**Автор:** Paul Bradshaw  
**Організаційний контекст:** Birmingham City University, MA in Data Journalism / journalism programmes  
**Репозиторій:** `paulbradshaw/MED7369-Specialist-Investigative-Journalism`  
**Перевірено:** 2026-08-10  
**Статус аудиту:** `INITIAL` — первинний розбір README та заявленої структури; потрібен окремий file-by-file аудит матеріалів.  

## 1. Чому це корисний donor

MED7369 цінний не як готовий OSINT-курс, а як приклад навчання investigative journalism через системне мислення, формулювання гіпотез, картування джерел і зв’язків, роботу з даними, автоматизацію та самостійний проєкт.

Для нашого курсу особливо важливий принцип: **спочатку зрозуміти систему та дослідницьке питання, потім обирати інструмент**. Це протилежність типовій побудові OSINT-курсів як каталогу сервісів.

## 2. Заявлена структура, релевантна нашому курсу

За README репозиторію виділено такі блоки:

- systems thinking та `Mapping the territory`;
- формування story / hypothesis та Story-Based Inquiry;
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

## 3. Рішення щодо компонентів

| Компонент MED7369 | Цінність для нас | Рішення | Цільовий контур |
|---|---|---|---|
| Systems thinking | Вчить досліджувати систему, а не окремий факт | `ADOPT` | Foundations / Planning |
| Mapping the territory | Карта акторів, інституцій, документів, джерел і точок контролю | `ADAPT` | Research planning |
| Story-Based Inquiry / hypothesis | Формує перевірювану гіпотезу й напрям збору | `ADAPT` | Research question + competing hypotheses |
| Systems of accountability | Корисна логіка пошуку інституційних джерел | `EXPAND` | Registers / official sources / accountability systems |
| Company accounts | Один із типів документальних слідів | `ADAPT` | Organisations / money / documents |
| Network analysis | Структурування зв’язків між людьми, організаціями, місцями | `EXPAND` | Entity resolution + link analysis |
| APIs | Масштабований збір даних | `REBUILD` | Automation / reproducible collection |
| Scraping | Масштабований збір і моніторинг | `REBUILD` | Automation / monitoring |
| Statistics | Захист від неправильних висновків із чисел | `EXPAND` | Analytical discipline |
| Cognitive bias | Критично важливо для атрибуції та перевірки альтернатив | `EXPAND` | Analytical discipline / peer review |
| Text as data / regex | Пошук закономірностей у великих масивах тексту | `EXPAND` | Large-scale OSINT / documents / Telegram corpora |
| Data cleaning | Нормалізація, дедуплікація, контроль якості | `ADOPT + EXPAND` | Data hygiene |
| Production/project weeks | Практика на власному дослідженні | `ADOPT` | Labs / capstone |
| Storytelling | Корисно для публічної версії | `ADAPT` | Reporting, але після evidence package |

## 4. Що це змінює в нашому Curriculum Blueprint

### 4.1. Додати systems thinking раніше

До роботи з пошуком та інструментами студент має навчитися описувати досліджувану систему:

- актори;
- інституції;
- формальні й неформальні відносини;
- документи;
- реєстри;
- механізми підзвітності;
- можливі точки появи цифрового сліду.

### 4.2. Посилити hypothesis-driven investigation

Потрібно чітко розрізняти:

- research question;
- working hypothesis;
- competing hypotheses;
- collection requirement;
- evidence supporting / contradicting hypothesis;
- conclusion and confidence.

Story-Based Inquiry можна використовувати як педагогічну основу, але висновок у нашому курсі має бути evidence-first і не підлаштовуватися під майбутню історію.

### 4.3. Виділити окремий блок Statistics + Cognitive Bias

У початковому плані ця тема була недостатньо виражена. Мінімально потрібні:

- denominator / base-rate problems;
- selection bias;
- survivorship bias;
- confirmation bias;
- availability bias;
- correlation vs causation;
- Simpson’s paradox;
- uncertainty and sampling;
- misleading aggregation;
- оцінка якості та повноти набору даних.

Цей блок має бути пов’язаний з атрибуцією: студент повинен активно шукати дані, які можуть спростувати його власну версію.

### 4.4. Автоматизація має бути частиною професійної практики

APIs, scraping, regex та text-as-data не слід викладати як «курс Python усередині OSINT». Навчальна мета:

> дослідник розуміє, коли ручний пошук перестає масштабуватися, здатний сформулювати задачу автоматизованого збору, перевірити якість результату та забезпечити його відтворюваність.

### 4.5. Data cleaning — не технічна дрібниця

Нормалізація імен, дат, телефонів, unit names, географічних назв, URL, username та інших ідентифікаторів прямо впливає на якість entity resolution і мережевого аналізу.

Для українсько-російського контуру слід додати:

- українська / російська орфографія;
- транслітерації;
- варіанти ПІБ;
- `ё/е`;
- зміни назв населених пунктів;
- старі / нові назви військових частин та формувань;
- дублікати публікацій і репости.

## 5. Чого не переносимо як є

### 5.1. Journalism-first фінал

У журналістському курсі логічним кінцевим продуктом є story / feature / investigation для аудиторії.

У нашій архітектурі між дослідженням і публікацією обов’язково існує шар:

`provenance → preservation → verification → analysis → confidence → peer review → evidence package`.

Лише після цього формується публічний продукт.

### 5.2. Конкретні технічні інструкції без повторної перевірки

API, scraping, OpenRefine, Python/R, зовнішні сервіси та посилання мають бути перевірені на актуальність станом на дату створення відповідної лабораторної.

Зберігаємо навчальну мету; інструкції та інструментарій перебудовуємо для поточної версії курсу.

### 5.3. Вузько британська інституційна специфіка

FOI, company accounts та systems of accountability мають бути трансформовані у ширший модуль про інституційні джерела, а український і російський контури — розроблені окремо.

## 6. Потенційні лабораторні, що випливають із MED7369

### Territory map

Студент отримує тему, наприклад російську військову частину або регіональну мобілізаційну систему, та створює карту:

- акторів;
- офіційних систем;
- потенційних джерел;
- зв’язків;
- цифрових слідів;
- прогалин у даних.

### Competing hypotheses

За одним набором фактів студент створює не одну «версію», а мінімум три альтернативні пояснення та collection plan для їх перевірки.

### Dirty entities

Набір записів з різними варіантами ПІБ, назв підрозділів, дат і URL потрібно нормалізувати, не об’єднавши різних людей помилково.

### Text as data

На масиві повідомлень або документів студент повинен сформувати відтворюваний спосіб пошуку заданих сутностей / патернів і перевірити false positives.

### Network analysis

Студент будує граф зв’язків, але окремо позначає:

- observed edge;
- inferred edge;
- source;
- temporal validity;
- confidence.

## 7. Питання для повного аудиту репозиторію

- Які саме вправи містяться в `networkanalysis/`?
- Наскільки придатні їхні форми планування розслідування?
- Які notebook-и / scripts містяться в `python/`?
- Чи є вправи, де метод важливіший за конкретний API?
- Які статистичні вправи можна відтворити на наших українсько-російських даних?
- Як викладено cognitive bias: як окрему тему чи у зв’язці зі статистикою?
- Що конкретно є в матеріалах cleaning / OpenRefine?
- Які принципи з `storytelling.md` придатні для перетворення доказового пакета на публічний звіт?
- Які ліцензійні умови репозиторію та вкладених матеріалів?

## 8. Попередній висновок

**Рівень корисності:** високий як педагогічний donor.  
**Рівень готовності до прямого використання:** низький — курс має журналістську мету і містить інструментальні частини, що потребують повторної актуалізації.  
**Найбільший внесок у наш curriculum:** systems thinking, territory mapping, hypothesis-driven inquiry, network analysis, statistics + cognitive bias, text-as-data, data cleaning та project-driven learning.

Наступний статус після повного перегляду файлів: `REVIEWED`.
