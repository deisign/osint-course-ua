# M06.6 — Web, mirrors and archives

**Перевірено на актуальність:** 2026-08-10

## Навчальна мета

Після цього розділу студент має вміти використовувати web archives і mirrors як provenance evidence, не плутаючи archive capture time з publication time і не вважаючи відсутність сторінки в архіві доказом її неіснування.

---

## 1. Архів — це ще один observation layer

Web archive не є машиною часу, яка гарантує повну копію минулого Інтернету.

Він є системою з власним:

- crawl coverage;
- capture timestamps;
- exclusions;
- technical failures;
- incomplete assets;
- dynamic-page limitations;
- indexing delays.

Тому archive evidence потрібно оцінювати так само критично, як будь-яке інше джерело.

---

## 2. Publication time ≠ capture time

Сторінка могла бути опублікована 10:00, а заархівована 13:40.

Archive timestamp підтримує:

> «Станом на 13:40 archive system зафіксувала цю сторінку в такому стані».

Він не доводить:

> «Сторінка була вперше опублікована о 13:40».

Якщо publication page сама містить timestamp, це окремий claim/field, який треба зберегти.

---

## 3. Earliest capture ≠ earliest publication

Найраніший Wayback capture — це **earliest known archive capture**.

Можливі попередні стани, які crawler не зафіксував.

Тому пишіть:

> «Найраніший доступний capture у перевіреному archive — ...»

а не:

> «Саме тоді сторінка з’явилася в Інтернеті».

---

## 4. Відсутність capture — слабкий negative evidence

Internet Archive прямо зазначає, що сторінки можуть бути відсутні через:

- crawler не знав про URL;
- password/access restrictions;
- robots/exclusions;
- dynamic rendering;
- page owner requests;
- technical failures.

Тому:

> «Wayback не має capture»

не дорівнює:

> «Сторінки в той час не існувало».

---

## 5. Save Page Now: useful, but scoped

Internet Archive’s Save Page Now може створити permanent archived URL для конкретної сторінки, але офіційна документація попереджає, що це **single-page capture**, а не повний crawl site; окремі assets або dynamic functionality можуть не зберегтися.

У research log фіксуйте:

- live URL;
- archive URL;
- capture time;
- хто ініціював capture, якщо це ваша дія;
- missing assets/issues.

---

## 6. Mirrors

Mirror — це copy content на іншому URL/domain/platform.

Він може бути:

- official mirror;
- syndication partner;
- cache;
- scraper;
- republication;
- malicious clone;
- web archive.

Mirror корисний для відновлення deleted material, але його provenance теж треба встановити.

### Питання до mirror

- Чи вказує original URL?
- Чи зберігає timestamps?
- Чи змінює text/layout?
- Чи зберігає embedded media?
- Чи має own publication time?
- Чи є ознаки automatic scraping?

---

## 7. URL archaeology

Старі/видалені pages часто залишають clues у:

- backlinks;
- search snippets;
- social shares;
- RSS feeds;
- sitemaps;
- quoted URLs;
- old slug patterns;
- redirects;
- embedded links.

Навіть якщо live page зникла, URL pattern може допомогти знайти archive capture.

---

## 8. Comparing archived versions

Для source tracing особливо цінні multiple captures.

Порівнюйте:

- title;
- body text;
- byline;
- source attribution;
- embedded media;
- timestamp;
- update note;
- links;
- certainty language.

Це дозволяє реконструювати correction/republishing chain.

---

## 9. Dynamic pages і false completeness

Архів може показати page shell, але не завантажити:

- JS-generated content;
- video player;
- images;
- interactive data;
- comments;
- API-loaded tables.

Не робіть висновок «цього елементу не було» лише тому, що archived rendering його не показує.

Перевірте:

- page source/assets;
- direct media URLs;
- інші captures;
- screenshots from other sources;
- mirrors.

---

## 10. Archive as provenance evidence, not authentication oracle

Archived page підтримує claim, що archive system зберіг певний representation.

Вона не автоматично підтверджує:

- truth of page content;
- identity of human author;
- correctness of timestamp;
- authenticity of embedded media.

Це все окремі verification questions.

---

## 11. Практичний workflow

```text
live page/post found
→ record URL + current state
→ search known archives
→ search earliest available captures
→ compare versions
→ inspect source links/embeds
→ preserve current page where appropriate
→ record archive limitations
→ map mirror/citation relationships
→ separate publication time from capture time
```

---

## 12. Приклад

Article B live now says:

> «Updated 14:20: location not confirmed».

Wayback captures:

- 12:10 — «confirmed location N»;
- 15:00 — current corrected text.

Channel C at 12:40 repeats «confirmed location N» and links B.

Provenance conclusion:

- B’s earlier version is a documented upstream source for the claim available before C;
- C → B is observed through link;
- correction happened before 15:00 capture, but exact edit time needs additional evidence unless page exposes it;
- current live B alone would hide the historical wording.

---

## 13. Archive checklist

- [ ] archive URL preserved;
- [ ] capture timestamp separated from page timestamp;
- [ ] earliest capture not called earliest publication;
- [ ] missing archive result not treated as proof of absence;
- [ ] dynamic/missing assets noted;
- [ ] multiple versions compared where relevant;
- [ ] mirror relationship classified;
- [ ] current/live and archived states both referenced;
- [ ] archive evidence not used as truth oracle.

---

## 14. Первинні references

Перевірено 2026-08-10:

- Internet Archive Help — Using the Wayback Machine: https://archivesupport.zendesk.com/hc/en-us/articles/360004651732-Using-The-Wayback-Machine
- Internet Archive Help — Save Pages in the Wayback Machine: https://archivesupport.zendesk.com/hc/en-us/articles/360001513491-Save-Pages-in-the-Wayback-Machine
- Internet Archive Help — Wayback Machine General Information: https://archivesupport.zendesk.com/hc/en-us/articles/360004716091-Wayback-Machine-General-Information

Перед live cohort archive-specific details should be rechecked.