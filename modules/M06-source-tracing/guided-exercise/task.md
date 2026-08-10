# M06 Guided Exercise — Provenance graph that changes

## Мета

Навчитися будувати provenance model поетапно та **переглядати її**, коли з’являється нове earlier evidence.

Це guided exercise перед незалежною L03.

---

## Формат

Вправа має дві фази.

1. Спочатку ви отримуєте `phase-1.csv`.
2. Після фіксації першої моделі відкриваєте `phase-2.csv`.

Не читайте phase 2 раніше.

---

# Phase 1

Прочитайте `input/phase-1.csv`.

Виконайте:

1. створіть timeline;
2. визначте earliest known publication;
3. для кожного relationship позначте `observed / inferred / unknown`;
4. окремо сформулюйте, що відомо про creator;
5. дайте confidence кожному propagation claim;
6. запишіть одну strongest alternative hypothesis.

### Обов’язковий короткий висновок

Максимум 120 слів.

---

# Freeze point

Перед переходом до phase 2 збережіть свій phase-1 output.

Не виправляйте його заднім числом.

Мета — побачити, як legitimately змінюється analytical model.

---

# Phase 2

Тепер відкрийте `input/phase-2.csv`.

Новий record був знайдений в іншому archive після початкового аналізу.

Виконайте:

1. додайте record до timeline;
2. перерахуйте earliest known publication;
3. перегляньте всі propagation edges;
4. позначте, які claims змінили confidence;
5. поясніть, чому саме;
6. сформулюйте новий bounded conclusion.

---

# Submission

- `phase-1-analysis.md`
- `phase-2-analysis.md`
- `edges.csv`

Рекомендовані columns для edges:

```text
from,to,status,basis,confidence,alternative,evidence_ref
```

---

# Підказки

Підказка 1: timestamp встановлює порядок observed publications, але не обов’язково transmission direction.

Підказка 2: explicit forward є сильнішим evidence relationship, ніж однаковий текст.

Підказка 3: новий earlier source повинен впливати не лише на label `earliest`, а й на confidence старих hypotheses.

Підказка 4: creator може залишитися unknown після обох фаз — це допустимий і очікуваний результат.