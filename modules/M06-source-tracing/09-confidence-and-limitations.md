# M06.9 — Confidence, bounded conclusions і limitations

## Навчальна мета

Після цього розділу студент має вміти формулювати source-tracing висновок так, щоб сила формулювання відповідала силі evidence, а прогалини не маскувалися загальними словами на кшталт «ймовірно» або «майже точно».

---

## 1. Source tracing рідко дає абсолютний origin

У реальному OSINT часто відсутні:

- private messages;
- deleted earlier posts;
- unpublished files;
- inaccessible groups;
- platform-internal logs;
- complete archive coverage;
- creator testimony.

Тому професійний результат часто має форму:

> «Найраніша доступна нам публікація — X; downstream relationships Y→Z observed, A→B inferred; creator не встановлений».

Це сильніший аналітичний продукт, ніж вигаданий «original source».

---

## 2. Confidence має належати конкретному claim

Погана практика:

> «Confidence: high».

Незрозуміло — у чому саме.

Краще:

- high confidence: R4 є explicit forward of R3;
- high confidence: collected files A і B byte-identical;
- medium confidence: R3 derived wording from R2a or common upstream;
- low confidence: R1 uploader knew creator identity;
- unknown: original creator.

Один case може одночасно містити claims з різною confidence.

---

## 3. Qualitative confidence scale

У цьому курсі базово використовуємо:

### High

Evidence прямо й стабільно підтримує claim; серйозні alternative explanations малоймовірні в доступному scope.

### Medium

Evidence підтримує claim, але лишаються реалістичні альтернативи або неповний provenance.

### Low

Claim можливий і має деякі supporting indicators, але evidence слабкий/непрямий або alternatives не виключені.

### Insufficient / Unknown

Evidence не дозволяє відповідально зробити позитивний висновок.

---

## 4. Confidence — не відсоток

Не пишіть `87%`, якщо у вас немає валідованої probabilistic model.

Число створює фальшиву точність.

Qualitative confidence має пояснюватися:

- supporting evidence;
- contradicting evidence;
- alternatives;
- missing data;
- search scope.

---

## 5. Bounded conclusion

Bounded conclusion прямо обмежує claim.

### Надто сильне

> «Канал A є першоджерелом відео».

### Краще

> «A — найраніша доступна нам публікація цього media у перевіреному наборі станом на 10 серпня 2026 року».

### Ще важливе доповнення

> «A заявляє, що отримав media від підписника; creator не встановлений».

Тепер conclusion точно відповідає evidence.

---

## 6. Limitation categories

### Coverage limitation

Не всі platforms/groups/indexes доступні або перевірені.

### Temporal limitation

Archives не гарантують capture усіх earlier states.

### Attribution limitation

Uploader/source relationship не встановлює creator identity.

### Technical limitation

Recompression/cropping ускладнює exact file matching.

### Platform limitation

Forward/edit/delete behaviour може приховувати частину lineage.

### Access limitation

Private/deleted/inaccessible content unavailable.

### Language/search limitation

Можливі невраховані spelling/transliteration variants.

---

## 7. Search scope statement

Для high-stakes роботи корисно додавати короткий scope:

> «Пошук включав exact/reduced phrase variants українською та російською, два web indexes, public Telegram results, доступні archive captures і reverse visual search; private groups та закриті accounts не перевірялися».

Тепер читач розуміє, що означає «earliest known».

---

## 8. Contradicting evidence

Confidence не можна оцінювати, перелічуючи лише supporting evidence.

Для кожного ключового claim запитайте:

> Що в нашому dataset суперечить цій версії?

Наприклад:

H: `A → B`.

Supporting:

- A earlier;
- identical rare typo.

Contradicting/weakening:

- C має ще earlier same typo;
- B іноді отримує матеріали через common feed;
- exact forward absent.

Conclusion має змінитися.

---

## 9. Negative conclusion

Правильний результат може бути:

> «Недостатньо evidence для встановлення direction між A і B».

Не треба замінювати його на:

> «A, скоріше за все, source»

лише тому, що завдання психологічно хочеться «закрити».

У цьому курсі добре обґрунтований negative result оцінюється вище за красиву overclaim.

---

## 10. Confidence update

Confidence має змінюватися при появі нового evidence.

### Початково

A earlier than B + same text → `A→B: medium`.

### Нове discovery

C earlier than both with same text.

Тепер:

- `A→B` може впасти до low/unknown;
- common upstream hypothesis зростає.

Якщо ваша confidence ніколи не змінюється після нових даних, ви, можливо, захищаєте hypothesis, а не тестуєте її.

---

## 11. Writing pattern

Для ключового source-tracing claim використовуйте:

### Claim

Що саме стверджується.

### Evidence

Які objects/fields це підтримують.

### Alternatives

Які інші моделі залишаються.

### Confidence

High / medium / low / insufficient.

### Limitation

Чого немає або що не перевірено.

Приклад:

> **Claim:** R3, імовірно, походить від R2a або спільного upstream source. **Evidence:** R3 пізніший і дослівно повторює distinctive wording R2a. **Alternative:** unseen common source. **Confidence:** medium. **Limitation:** explicit forwarding metadata відсутня.

---

## 12. Words to be suspicious of

Ці слова часто маскують відсутність calibration:

- очевидно;
- безсумнівно;
- точно;
- ясно, що;
- майже напевно;
- усі знають;
- підтверджено;
- verified.

Вони допустимі лише якщо claim і evidence чітко визначені.

Замість «verified video» пишіть:

> «location verified to X»;

або:

> «publication provenance verified from B to A».

---

## 13. Mini exercise

Дано:

- A 08:00;
- B 08:05;
- same unusual caption;
- no explicit link;
- archive C 07:50 with same caption found later.

### До C

`A→B` — максимум medium, common upstream possible.

### Після C

`A→B` — weak/unknown unless additional evidence.

Earliest known source becomes C, але creator все ще unknown.

---

## 14. Checklist

- [ ] confidence assigned per claim;
- [ ] no fake percentages;
- [ ] strongest alternative stated;
- [ ] contradicting evidence included;
- [ ] search scope described;
- [ ] earliest known bounded by time/scope;
- [ ] creator not inferred from uploader;
- [ ] unknown accepted as valid outcome;
- [ ] limitations specific, not boilerplate;
- [ ] conclusion would survive reviewer asking «what exactly do you know?»

---

## 15. Основне правило

**Сила професійного OSINT-висновку визначається не категоричністю мови, а точністю меж, усередині яких він справді доведений.**