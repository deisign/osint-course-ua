# M06.8 — Circular reporting і фальшива незалежність

## Навчальна мета

Після цього розділу студент має вміти відрізняти кількість publications від кількості independent evidence origins і виявляти ситуації, коли «багато джерел» насправді є одним upstream claim.

---

## 1. Чому це одна з головних OSINT-помилок

Дослідник знаходить:

- три Telegram-канали;
- два медіа;
- блог;
- пост у соцмережі.

Усі пишуть одне й те саме.

Спокуса:

> «Сім незалежних джерел підтверджують подію».

Але якщо всі вони походять від одного anonymous post, ми маємо:

> **сім publications, один evidence origin.**

Це принципово різні речі.

---

## 2. Publication count vs origin count

Для кожного claim рахуйте окремо:

### Publication count

Скільки разів claim був опублікований.

### Independent origin count

Скільки незалежних ланцюгів evidence підтримують claim.

Приклад:

```text
A Telegram
├─ B site
│  └─ D channel
└─ C channel
   └─ E site
```

Publication count: 5.

Якщо B і C обидва походять від A, origin count для claim може лишатися 1.

---

## 3. Що означає independent

У цьому курсі два sources не вважаються незалежними для конкретного claim, якщо один:

- прямо цитує іншого;
- forward-ить іншого;
- повторює його exclusive material;
- використовує той самий upstream press release;
- отримав data з того самого single-origin dataset;
- очевидно відтворює той самий source claim без нового evidence.

Незалежність завжди **claim-specific**.

Два outlets можуть бути незалежними організаціями, але залежними щодо одного факту.

---

## 4. Common source не завжди visible

Іноді A і B не посилаються один на одного, але мають:

- однакову rare typo;
- однакову неправильну цифру;
- однаковий порядок details;
- однаковий mistranslation;
- однаковий crop.

Це може підтримувати common upstream hypothesis.

Не обов’язково доводити, хто саме upstream, щоб **не рахувати A і B як повністю незалежні**.

---

## 5. Circular reporting

Найнебезпечніша форма:

```text
A publishes claim
→ B cites A
→ C cites B
→ D cites C
→ A cites D as “media confirmation”
```

Тепер A може виглядати «підтвердженим зовнішніми медіа», хоча evidence never left the original circle.

---

## 6. Citation laundering

Claim може ставати «соліднішим» лише через зміну оболонки:

1. anonymous Telegram post;
2. regional website «повідомляють соцмережі»;
3. larger outlet cites regional site;
4. analyst cites larger outlet;
5. original channel posts screenshot analyst’s report.

Авторитет downstream publisher не створює нового primary evidence, якщо він просто ретранслює upstream claim.

---

## 7. Corroboration vs repetition

### Repetition

Джерело повторює existing claim.

### Corroboration

Джерело додає **незалежний evidence path**.

Наприклад:

Claim: «Будівля пошкоджена до 12:00».

- Telegram A пише про пошкодження.
- Site B цитує A. → repetition.
- Satellite image independently shows damage by 11:40. → corroboration.
- Local authority statement based on own assessment. → potentially independent corroboration, evaluate source basis.

---

## 8. Independence matrix

Для складного case корисна таблиця:

| Source | Claim | Upstream | New primary evidence? | Independent for this claim? |
|---|---|---|---|---|
| A | X | unknown | yes/unknown | baseline |
| B | X | A | no | no |
| C | X | A | no | no |
| D | X | own satellite | yes | yes |

Це швидко руйнує ілюзію «4 sources».

---

## 9. Press releases та official statements

Official source може бути важливим, але downstream media, які всі цитують один official statement, не створюють multiple independent confirmations.

Ви маєте:

- один official origin;
- N republishers.

Якщо another agency separately reports own observations — це вже інший evidence path.

---

## 10. Data reuse

Circularity буває не лише у текстах.

Три аналітичні reports можуть мати однакові numbers, бо всі використовують:

- один leaked spreadsheet;
- один public dataset;
- один NGO database;
- один Telegram monitoring list.

Тоді agreement between reports не є independent confirmation underlying data.

---

## 11. Типові linguistic clues

Шукайте:

- «за даними...»;
- «повідомляють ЗМІ»;
- «як пишуть Telegram-канали»;
- «за інформацією джерел у мережі»;
- «раніше повідомлялося»;
- same rare wording;
- same sequence of facts;
- same error.

Невизначене «повідомляють ЗМІ» часто потребує reverse tracing до конкретного origin.

---

## 12. Міні-кейс

A о 08:00:

> «У районі N закрили міст через пошкодження».

B о 08:20:

> «Як повідомляє A, міст закритий».

C о 08:45:

> «Місцеві медіа повідомляють про закриття» — hyperlink B.

D о 09:00:

> фото дорожнього знаку «проїзд закрито», own photographer.

E о 09:10:

> цитує C і D.

### Правильний count

- A/B/C claim chain = 1 origin path;
- D = separate observational evidence;
- E aggregates two paths but не є третім independent origin.

---

## 13. Практичний workflow

```text
collect publications
→ extract exact claims
→ record explicit citations
→ identify text/media fingerprints
→ group likely common-origin publications
→ search upstream
→ mark independent evidence paths
→ count origins, not pages
→ report uncertainty where upstream unknown
```

---

## 14. Common failure modes

1. «Багато посилань у Google» = багато джерел.
2. Три медіа = три підтвердження.
3. Reputable outlet automatically treated as independent primary evidence.
4. Aggregator counted as new origin.
5. Same dataset analysed three times counted as three data sources.
6. Citation chain not traced upstream.
7. Unknown relationship assumed independent instead of classified as unknown.

---

## 15. Checklist

- [ ] exact claim isolated;
- [ ] explicit citations traced;
- [ ] common wording/media fingerprints checked;
- [ ] upstream origins grouped;
- [ ] repetition separated from corroboration;
- [ ] official single-origin syndication not overcounted;
- [ ] data-source dependence considered;
- [ ] independent origin count stated where useful;
- [ ] unknown dependence labelled unknown.

---

## 16. Основне правило

**Незалежність — це не властивість логотипа видання. Це властивість evidence path для конкретного твердження.**