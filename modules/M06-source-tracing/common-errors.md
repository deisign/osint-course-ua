# M06 Common Errors — діагностика і remediation

Цей файл призначений і для студента, і для викладача. Він описує не лише помилку, а й **яку звичку треба виправити**.

---

## E01. «Найстаріший timestamp = оригінал»

### Симптом

> «A був першим джерелом, бо опублікував о 08:00».

### Чому помилка

Timestamp встановлює chronology observed publications, а не creator/original status.

### Remediation

Переписати conclusion із фразою `earliest known available publication in the checked scope` і окремо вказати creator status.

---

## E02. «Uploader = creator»

### Симптом

Канал, який завантажив media, названий автором без додаткового evidence.

### Remediation

Створити role table: creator / uploader / publisher / source for later publisher.

---

## E03. «Same hash = direct copy»

### Симптом

> «B отримав file від A, бо SHA-256 однаковий».

### Чому помилка

Hash доводить byte identity collected files, не transmission path.

### Remediation

Додати common upstream hypothesis.

---

## E04. «Different hash = unrelated media»

### Симптом

Platform transcode прийнятий за інший media origin.

### Remediation

Порівняти visual content, duration, keyframes, crop/resize/transcode characteristics.

---

## E05. «No forward label = independent source»

### Симптом

Відсутність explicit provenance сприймається як доказ independent creation.

### Remediation

Позначити edge `unknown/inferred`, перевірити text fingerprints/media lineage і common upstream.

---

## E06. «Same text = observed copy»

### Симптом

Стрілка малюється лише через identical wording.

### Remediation

Змінити edge на `INFERRED`, записати basis і alternative.

---

## E07. «Five outlets = five confirmations»

### Симптом

Publication count підміняє origin count.

### Remediation

Побудувати citation/provenance graph і independence matrix.

---

## E08. «Reputable outlet = primary evidence»

### Симптом

Brand authority downstream publisher замінює upstream tracing.

### Remediation

Відкрити citation/source link і пройти chain upstream до evidence origin.

---

## E09. «Deleted = guilty»

### Симптом

Deletion event інтерпретується як мотив або confession.

### Remediation

Переписати statement тільки як availability history.

---

## E10. «Current edited post = whole history»

### Симптом

Research package містить лише last state.

### Remediation

Version-preserve pre/post-edit states, якщо edit material.

---

## E11. «Archive timestamp = publication time»

### Симптом

Wayback capture використаний як точний start time сторінки.

### Remediation

В окремих columns зберегти `page claimed timestamp` і `archive capture timestamp`.

---

## E12. «No archive result = page did not exist»

### Симптом

Archive coverage трактується як exhaustive.

### Remediation

Додати archive limitations і шукати mirrors/backlinks/search traces.

---

## E13. «Watermark = author»

### Симптом

Publisher branding перетворюється на creator attribution.

### Remediation

Побудувати watermark/version lineage і перевірити earlier unwatermarked copy.

---

## E14. «Verified» без об’єкта verification

### Симптом

> «Відео verified».

### Remediation

Уточнити claim:

- provenance verified?
- location?
- date?
- file identity?
- publisher relationship?

---

## E15. «Conclusion survives new evidence unchanged»

### Симптом

Новий earlier source знайдений, але old edges/confidence не переглянуті.

### Remediation

Version analytical graph and explain confidence changes.

---

## E16. «Search result rank = source proximity»

### Симптом

Перший Google result названий origin.

### Remediation

Treat search as discovery layer; search earlier versions, citations, archives.

---

## E17. «Search failure = absolute absence»

### Симптом

> «Цього раніше ніде не було».

### Remediation

Bound to scope:

> «У перевірених індексах/платформах earlier result не знайдено».

---

## E18. «Media provenance = claim provenance»

### Симптом

Старий video і новий caption йдуть однією timeline.

### Remediation

Split media timeline and claim timeline.

---

## E19. «Graph arrow without evidence_ref»

### Симптом

Красивий provenance diagram без explanation edge basis.

### Remediation

Кожен edge повинен мати status + basis + evidence reference + confidence.

---

## E20. «Unknown сприймається як особиста невдача»

### Симптом

Студент заповнює прогалини слабкими guesses, щоб мати завершену історію.

### Remediation

Оцінювати `unknown / insufficient` як правильний результат, якщо межа добре обґрунтована.

---

# Reviewer shortcut

Якщо робота виглядає переконливо, але ви хочете швидко знайти проблеми, поставте п’ять питань:

1. **Хто creator — і звідки це відомо?**
2. **Яка стрілка у графі найслабша — чому вона взагалі є?**
3. **Скільки тут independent origins, а не publications?**
4. **Що зміниться, якщо завтра знайдеться earlier post?**
5. **Яке найсильніше твердження автор НЕ має права зробити?**

Якщо студент не може відповісти, source tracing ще не сформований як компетенція.