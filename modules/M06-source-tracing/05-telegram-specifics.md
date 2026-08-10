# M06.5 — Telegram-specific source tracing

**Перевірено на актуальність:** 2026-08-10  
**Platform-specific section:** так; потребує періодичного повторного аудиту.

## Навчальна мета

Після цього розділу студент має вміти читати Telegram-публікацію як provenance object: розрізняти те, що платформа прямо показує/кодує, те, що могло бути втрачено під час copy/repost, і те, що взагалі не можна встановити з одного current post.

---

## 1. Telegram не є прозорим журналом походження

Telegram дає корисні provenance signals, але вони не створюють повного chain of custody.

Платформа може зберігати/показувати:

- message ID;
- publication time;
- forwarded-message metadata;
- edit state / edit date в API-моделі;
- channel/account identity;
- reply/repost context;
- media attachment;
- view/forward counters для окремих типів posts.

Але Telegram також дозволяє:

- копіювати content без reference на original sender;
- видаляти messages;
- редагувати messages;
- repost-ити media як новий upload;
- змінювати caption/context downstream.

Тому відсутність forward marker **не доводить**, що content не був запозичений.

---

## 2. Message ID — сильний локальний identifier

У межах конкретного chat/channel message ID допомагає:

- посилатися на specific publication object;
- відрізняти два posts з однаковим content;
- фіксувати edit/deletion history;
- зіставляти archive snapshots.

Але message ID сам по собі не є global identifier content.

Один і той самий video може існувати в десятках chats з різними message IDs.

---

## 3. Forward metadata

Telegram API-модель містить окрему інформацію про forwarded messages (`fwd_from` / forward origin). Це сильний provenance signal для **конкретного forwarding event**.

Якщо B містить explicit forward origin A, ми можемо підтримати statement:

> «Ця публікація B була створена як forward із origin, який Telegram представляє як A».

Але це не дозволяє автоматично сказати:

- A створив media;
- A був першим publisher;
- A правильно описав event;
- A не отримав content від третьої особи.

### Privacy / hidden-origin caveat

Forward attribution може залежати від privacy/platform conditions. Дослідник повинен документувати **те, що реально observable**, а не припускати, що всі forwards завжди містять однаковий набір origin fields.

---

## 4. Copy ≠ forward

Це принципово важливо.

Telegram tooling/API допускає копіювання message content без reference на original sender. На практиці publisher також може вручну:

- скопіювати текст;
- завантажити media заново;
- зробити screenshot;
- screen-record video;
- змінити caption.

Тому:

> no forward label

означає лише:

> explicit forwarding provenance не спостерігається в цій copy.

Воно **не означає**:

> content незалежно створений цим publisher.

---

## 5. Edit history

Telegram messages можуть редагуватися; у поточній API-моделі існує `edit_date` для message object.

Для OSINT важливо відрізняти:

- original publication time;
- last observed edit time;
- archive capture time;
- time, коли downstream outlet процитував певну version.

### Material edits

Особливо важливі edits, що змінюють:

- location;
- date/time;
- casualty count;
- source attribution;
- certainty;
- accusation;
- identity;
- correction/retraction.

Якщо ви маєте pre-edit і post-edit state, зберігайте їх як **окремі observed states одного message object**.

Не overwrite-те стару version у research package.

---

## 6. Deletion

Telegram FAQ прямо попереджає, що deleted messages можуть не залишати видимого сліду в chat history.

Для дослідника це означає:

- current absence не доводить, що message ніколи не існував;
- screenshot без provenance слабший за archived capture + metadata;
- deletion event сам по собі не доводить guilty intent або deception;
- потрібно фіксувати, **коли саме** message був доступний і коли його absence було observed.

Коректна мова:

> «Message 4112 був зафіксований у стані X о 09:20; під час перевірки о 10:12 він був недоступний».

Некоректна:

> «Автор видалив доказ, бо злякався».

Останнє — claim про мотив, якого deletion alone не встановлює.

---

## 7. Channel post ≠ eyewitness source

Канал може публікувати:

- власний content;
- content subscribers;
- прес-реліз;
- матеріал іншого каналу;
- копію без attribution;
- synthetic/edited content.

Тому фрази publisher-а мають source value, але повинні класифікуватися.

Приклади:

### «Наше відео»

Claim of ownership/authorship. Потребує verification.

### «Надіслав підписник»

Важлива provenance statement: publisher заявляє upstream source і фактично не претендує на creator role.

### «Пишуть, що…»

Слабке невизначене attribution. Потрібно шукати source of claim.

### «За даними X»

Direct claimed source relationship; перевіряємо X.

---

## 8. Forward counter і view counter

Counters можуть бути корисними для diffusion analysis, але не для truth assessment.

Велика кількість views/forwards не доводить:

- authenticity;
- independent corroboration;
- original authorship;
- factual accuracy.

Virality — характеристика поширення, не доказ істини.

---

## 9. Public post URL як research reference

Для public channels message URL може бути зручним identifier/reference.

Але research package не повинен залежати тільки від live URL, бо post може:

- бути видалений;
- змінений;
- стати недоступним;
- змінити public accessibility.

Тому для material object зберігайте, де доречно:

- URL;
- channel/account;
- message ID;
- observed timestamp;
- capture timestamp;
- preserved copy/snapshot;
- media file;
- hash;
- notes про edit/forward state.

---

## 10. Telegram source-tracing workflow

```text
1. capture current post
2. record channel + message ID + observed timestamps
3. record forward/edit indicators
4. preserve media separately
5. extract distinctive caption fragments
6. inspect surrounding posts
7. search same media/text elsewhere
8. search earlier Telegram/web copies
9. preserve earlier states
10. classify edges observed/inferred
11. separate media lineage from caption lineage
12. state earliest known available source + limitations
```

---

## 11. Приклад із L03

### R1

`@road_cam_archive` публікує synthetic media раніше за інших і пише:

> «Прислав подписчик».

Висновки:

- R1 — earliest known publication у bundle;
- publisher/uploader відомий;
- creator unknown;
- publisher прямо заявляє upstream contributor.

### R2a

Пізніший channel додає location/time claim без explicit forward.

Висновок:

- claim lineage може починатися тут у доступному bundle;
- media creator тут не встановлюється;
- relationship R1 → R2a не observed лише через chronology.

### R4

Explicit forwarded-from R3.

Висновок:

- R4 → R3 provenance edge observed;
- це нічого автоматично не доводить про origin до R3.

### R2b

Same message ID, material edit із qualification/retraction.

Висновок:

- одна publication identity має дві observed states;
- downstream copies pre-edit wording важливі для reconstruction spread.

---

## 12. What Telegram alone cannot tell you

Навіть ідеально задокументований Telegram post сам по собі може не встановлювати:

- who filmed;
- where filmed;
- when filmed;
- whether caption is true;
- whether account administrator personally witnessed event;
- whether uploader received file directly from creator;
- whether unseen earlier private/public copy existed;
- intent behind edit/deletion.

Для цього потрібні інші verification methods.

---

## 13. Platform-specific checklist

- [ ] channel/account зафіксований;
- [ ] message ID зафіксований;
- [ ] publication vs capture time separated;
- [ ] edit indicator/state зафіксований;
- [ ] forward metadata зафіксована дослівно/структуровано;
- [ ] no-forward не інтерпретовано як independent origin;
- [ ] media preserved separately;
- [ ] source claim publisher-а класифікований;
- [ ] surrounding context перевірений;
- [ ] deletion interpreted only as observed availability change;
- [ ] live URL не є єдиною preserved evidence copy.

---

## 14. Первинні platform references

Перевірено 2026-08-10:

- Telegram FAQ — message editing/deletion and general platform behaviour: https://www.telegram.org/faq
- Telegram API message constructor — `fwd_from`, `edit_date`, message fields: https://core.telegram.org/constructor/message
- TDLib `messageForwardInfo` — forward origin/date model: https://core.telegram.org/tdlib/docs/classtd_1_1td__api_1_1message_forward_info.html
- TDLib `inputMessageForwarded` — copy options / forwarding behaviour: https://core.telegram.org/tdlib/docs/classtd_1_1td__api_1_1input_message_forwarded.html
- Telegram Bot API — current message fields including `edit_date`: https://core.telegram.org/bots/api

Platform behaviour may change. Перед live cohort цей розділ має проходити quick revalidation.