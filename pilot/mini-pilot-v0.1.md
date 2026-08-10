# Mini-pilot v0.1

**Статус:** planned  
**Дата:** 2026-08-10

## 1. Навіщо цей пілот

Перший mini-pilot не перевіряє весь курс. Він перевіряє три фундаментальні професійні звички:

1. **L01 Territory Map** — чи планує студент дослідження до масового пошуку;
2. **L03 Telegram Source Tracing** — чи відновлює provenance і розділяє observed / inferred;
3. **L12 Wrong Attribution** — чи здатен зупинитися перед необґрунтованою атрибуцією.

Разом вони утворюють короткий цикл:

`system → collection logic → provenance → contradictory evidence → calibrated conclusion`.

## 2. Група

Оптимально 5–8 учасників:

- 2 новачки без системного OSINT-досвіду;
- 2–3 учасники з практикою журналістики / аналітики / fact-checking;
- 1 технічний або data-oriented учасник;
- 1 досвідчений дослідник як контрольний учасник або reviewer.

Не потрібно набирати лише сильних OSINT-практиків: такий пілот погано виявляє незрозумілі інструкції.

## 3. Правило проведення

### Головне

Учасники отримують **лише письмові матеріали репозиторію**.

Автор / викладач не пояснює завдання усно під час першого проходу.

Якщо учасник ставить запитання, facilitator:

1. не дає відповіді по суті;
2. записує точне питання;
3. за потреби дозволяє учаснику продовжити з власним трактуванням.

Питання учасника є даними про якість курсу.

## 4. Орієнтовна послідовність

### Session 0 — короткий pre-brief

20–30 хвилин.

Пояснюються лише загальні правила:

- різниця між source / claim / conclusion;
- правило не вигадувати відсутні дані;
- формат файлів для здачі;
- етичні правила;
- факт, що частина завдань навмисно не має позитивної відповіді.

Не пояснюються пастки конкретних лабораторних.

### Session 1 — L01 Territory Map

Target window: 60–100 хвилин.

Спостерігаємо:

- чи починає учасник одразу «шукати винного»;
- чи розділяє given / inferred / unknown;
- чи вміє перетворювати тему на collection requirements;
- чи з’являються accountability / documentary systems, а не лише медіа.

### Session 2 — L03 Telegram Source Tracing

Target window: 75–120 хвилин.

Спостерігаємо:

- чи відрізняє earliest observed upload від creator/original source;
- чи помічає edit/deletion history;
- чи зберігає provenance;
- чи правильно працює з derived media;
- чи формулює strongest defensible conclusion.

### Session 3 — L12 Wrong Attribution

Target window: 60–100 хвилин.

Спостерігаємо:

- чи відділяє account control / identity / presence / affiliation / action;
- чи враховує contradicting evidence;
- чи не перестрибує з P-A на P-B;
- чи розрізняє upload time і capture time;
- чи сприймає `insufficient evidence` як повноцінний результат.

## 5. Що записуємо

Для кожної лабораторної:

- start time;
- submission time;
- completion time;
- кількість запитань facilitator-у;
- точний текст запитань;
- місце, де учасник зупинився або повернувся назад;
- rubric score;
- critical fail: yes/no + type;
- self-reported confidence до перевірки;
- confidence after feedback.

## 6. Що оцінюємо не як студентську помилку, а як помилку курсу

Якщо одна й та сама проблема виникає у ≥ 40% учасників, спочатку перевіряємо формулювання / структуру курсу.

Приклади:

- учасники не розуміють, який саме artefact треба здати;
- плутають термін через нашу непослідовну термінологію;
- не знаходять потрібний input-файл;
- одна інструкція допускає два несумісні трактування;
- rubric вимагає того, чого task не просив;
- instructor solution використовує інформацію, якої немає у student bundle.

## 7. Pilot metrics

### Usability

- median completion time;
- range completion time;
- clarification questions per participant;
- abandoned / incomplete submissions.

### Method

- % submissions with critical fail;
- % that preserve given/inferred distinction in L01;
- % that reconstruct correct provenance structure in L03;
- % that refuse positive P-A/P-B attribution in L12.

### Calibration

For each lab compare:

- participant confidence;
- rubric performance;
- severity of errors.

Особливо цікавий випадок: **high confidence + critical fail**.

## 8. Pilot success criteria

Mini-pilot вважається придатним для переходу до v0.2, якщо:

- ≥ 80% учасників завершують усі три лабораторні;
- не більше 20% critical fails виникають через неоднозначність інструкції;
- rubric дозволяє двом reviewers дати близькі результати;
- жодна lab не вимагає прихованої авторської підказки;
- strongest students все одно знаходять інтелектуальну складність, а не проходять lab механічно.

Ці цифри є робочими порогами першого пілоту, а не валідованим освітнім стандартом.

## 9. Reviewer calibration

До реального pilot grading двоє reviewers незалежно оцінюють одну й ту саму тестову submission.

Якщо різниця:

- >10 балів зі 100;
- або один reviewer бачить critical fail, а інший ні,

rubric потребує уточнення до оцінювання студентської групи.

## 10. Після пілоту

Створити:

`pilot/mini-pilot-v0.1-report.md`

Структура:

1. склад групи;
2. completion times;
3. usability failures;
4. методологічні помилки;
5. critical fail distribution;
6. rubric disagreement;
7. unexpected strategies;
8. lab-by-lab revisions;
9. curriculum implications;
10. рішення `keep / revise / replace` для кожної лабораторної.

## 11. Чого pilot не доводить

Навіть успішний mini-pilot не доводить:

- валідність усього курсу;
- професійну компетентність випускника;
- юридичну придатність evidence package;
- ефективність українсько-російської спеціалізації;
- довгострокове утримання навичок.

Це тест **навчального механізму**, а не сертифікація програми.
