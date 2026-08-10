# M06.4 — Search strategy: як шукати не «інформацію», а попередні стани

## Навчальна мета

Після цього розділу студент має вміти побудувати відтворювану search strategy для source tracing та пояснити, чому жоден окремий search engine або platform search не є повним реєстром минулого.

---

## 1. Source tracing має іншу мету, ніж звичайний пошук

Звичайний пошук часто відповідає:

> «Що відомо про X?»

Source tracing питає:

> «Де й у якій формі цей конкретний item/claim з’являвся раніше?»

Тому пошукова одиниця — не просто тема, а **fingerprint**.

Fingerprint може бути:

- distinctive text fragment;
- unusual typo;
- exact phrase;
- username;
- filename;
- watermark;
- quoted sentence;
- rare number combination;
- image fragment;
- video keyframe;
- title pattern;
- URL slug;
- message ID + channel;
- document phrase.

---

## 2. Починайте з inventory

Перед пошуком запишіть, що вже маєте.

### Для text claim

- повний текст;
- 2–5 distinctive fragments;
- names;
- locations;
- numbers;
- unusual errors;
- language;
- possible translations.

### Для media

- collected file;
- dimensions/duration;
- hash;
- watermark;
- visible text;
- keyframes;
- audio clues;
- crop characteristics.

### Для publication

- URL/message ID;
- channel/account;
- timestamp;
- edit label;
- forward metadata;
- surrounding posts;
- comments/replies where relevant.

Цей inventory потім дозволяє пояснити search path іншому досліднику.

---

## 3. Search ladder

Зручно йти від найспецифічнішого до ширшого.

### Level 1 — exact fingerprint

- exact quoted phrase;
- exact typo;
- exact filename;
- full username;
- specific URL fragment.

### Level 2 — reduced fingerprint

Якщо exact search нічого не дає:

- коротший distinctive fragment;
- прибрати змінювані числа;
- прибрати punctuation;
- варіант без emoji;
- інший відмінок імені.

### Level 3 — language variants

Для українсько-російського середовища особливо важливі:

- українська / російська форма;
- `ё/е`;
- `и/і` у транслітераціях;
- старі/нові назви населених пунктів;
- латиниця / кирилиця;
- прізвище + ініціали;
- common misspellings.

### Level 4 — semantic context

- event + rare object;
- location + date;
- quoted speaker + unique phrase;
- visual clue + event type.

---

## 4. Не шукайте лише одним індексом

Різні search systems мають різні:

- crawl coverage;
- ranking;
- indexing delays;
- deletion behaviour;
- geographic/language biases;
- treatment of social platforms.

Тому «Google не знайшов» означає лише:

> «У цьому запиті, в цьому індексі, на цей момент результат не знайдено».

Це не дорівнює:

> «Раніше цього ніде не було».

---

## 5. Search log

Source tracing без search log погано відтворюється.

Мінімальні поля:

| time | system | query | filters | result | action |
|---|---|---|---|---|---|
| 10:12 | search engine A | `"rare phrase"` | none | 3 hits | opened 1,2 |
| 10:18 | platform search | phrase variant | channel | no hit | widened query |

Лог не потрібен для кожного випадкового кліку, але повинен фіксувати **значущі search decisions**.

---

## 6. Search backwards from downstream citation

Іноді простіше починати не з item, а з того, хто його цитує.

Article D може містити:

- embedded post;
- hyperlink;
- channel name;
- «за даними…»;
- screenshot із username;
- filename;
- quoted caption.

Ці ознаки стають новими fingerprints.

Source tracing — iterative process:

`result → new fingerprint → earlier result → new fingerprint`.

---

## 7. Контекстні сусіди

Якщо знайдено ранній post, перевірте posts до/після нього.

Це може дати:

- «нам надіслали відео»;
- correction;
- continuation;
- second angle;
- acknowledgement of another source;
- discussion of location uncertainty.

Ізольований screenshot часто втрачає саме цей provenance context.

---

## 8. Search by mistakes

Помилки часто кращі за правильний текст.

Якщо claim містить рідкісну помилку:

> «Белгордская облсть»

і та сама помилка з’являється downstream, це сильний fingerprint propagation lineage.

Але пам’ятайте common upstream alternative.

---

## 9. Search media separately from caption

Для поста з відео робіть два паралельні пошуки:

### Media lineage

- visual/reverse search;
- keyframes;
- watermarks;
- derived crops;
- transcodes.

### Claim lineage

- exact phrases;
- location/date wording;
- casualty figures;
- accusation wording.

Можливо, media старіше за claim на місяці або роки.

---

## 10. Stop conditions

Без stop conditions source tracing може тривати нескінченно.

Заздалегідь визначайте, наприклад:

- earliest known publication досягнута в заданому time window;
- перевірено N основних platform/search paths;
- explicit upstream source знайдений;
- додатковий пошук не змінює conclusion;
- risk/cost перевищує value;
- питання потребує закритих/неетичних методів — stop/escalate.

Stop condition не означає «ми знайшли абсолютний origin». Він означає «ми виконали достатній і задокументований search scope».

---

## 11. Приклад search path

Маємо caption:

> «Удар по мосту сьогодні вранці, місто N».

### Step 1

Exact phrase — знаходимо три reposts.

### Step 2

Беремо рідкісну фразу без location — знаходимо пост на 40 хвилин раніше.

### Step 3

У ранньому пості інший caption: «відео від підписника, місце не знаємо».

### Step 4

Візуальний пошук keyframe — знаходимо старішу публікацію на іншій платформі два місяці тому.

### Result

Media lineage і claim lineage розходяться:

- media — старе;
- current location claim — з’явився downstream сьогодні.

Саме це й було об’єктом дослідження.

---

## 12. Search reproducibility checklist

- [ ] object/claim fingerprints зафіксовані;
- [ ] exact + reduced variants використані;
- [ ] language/transliteration variants перевірені;
- [ ] media і caption шукалися окремо;
- [ ] significant queries записані;
- [ ] downstream citations перевірені на links/embeds;
- [ ] context around early posts переглянуто;
- [ ] stop condition описаний;
- [ ] negative search results не перетворені на absolute absence claim.

---

## 13. Основне правило

Search engine — це **інструмент спостереження**, а не реєстр реальності.

Source tracing висновок завжди повинен відповідати scope пошуку, а не звучати сильніше за нього.