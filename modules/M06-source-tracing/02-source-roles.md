# M06.2 — Source roles: creator, uploader, publisher, source

## Навчальна мета

Після цього розділу студент має вміти розкласти одну публікацію на окремі ролі та не приписувати одній сутності більше, ніж підтверджено evidence.

---

## 1. Чому ролі треба розділяти

Фраза «джерело відео — канал X» часто приховує кілька різних тверджень. Канал X може бути лише місцем, де дослідник знайшов копію. Він може бути publisher, uploader, republisher або aggregator — і при цьому не мати жодного відношення до фізичного створення відео.

У цьому курсі ми використовуємо п’ять базових ролей.

---

## 2. Creator

**Creator** — особа, пристрій або система, що створила первинний content.

Для фото це може бути фотограф або камера. Для відео — оператор або автоматична камера. Для документа — автор/система, яка сформувала файл. Для text claim — первинний автор формулювання.

Creator часто є найскладнішою роллю для доведення.

### Що може підтримувати creator claim

- оригінальний файл із переконливим provenance;
- авторська заява, підтверджена незалежно;
- серія суміжних кадрів/матеріалів, доступних лише автору;
- технічні або контекстні ознаки, які зв’язують creator з item;
- external corroboration.

### Що не доводить creator

- ранній timestamp;
- watermark;
- caption «наше відео» без підтверджень;
- масове цитування каналу іншими;
- наявність файлу в Telegram-каналі.

---

## 3. Uploader

**Uploader** — суб’єкт, який завантажив конкретну copy на конкретну platform.

Uploader може:

- бути creator;
- отримати файл від creator;
- завантажити файл після пересилання;
- завантажити файл, скачаний із іншої платформи;
- не знати точного походження.

Доказ uploader role зазвичай простіший: конкретний account/channel опублікував конкретний object.

Але uploader role не містить автоматично claims про авторство чи істинність content.

---

## 4. Publisher

**Publisher** — суб’єкт, який зробив material доступним своїй аудиторії та надав йому publication context.

Publisher додає:

- заголовок;
- caption;
- location claim;
- date claim;
- attribution;
- interpretation;
- certainty language.

Саме тут часто виникає misinformation: media може залишатися справжнім, але publisher змінює контекст.

---

## 5. Republisher / aggregator

**Republisher** повторно публікує material, отриманий з іншого джерела.

**Aggregator** системно збирає content із багатьох sources.

Для OSINT це важливо, бо популярний aggregator може виглядати як origin лише тому, що:

- має великий search visibility;
- його пост найкраще індексується;
- його цитують медіа;
- ранній origin уже видалений.

Popularity ≠ proximity to origin.

---

## 6. Source for a later publisher

Це окрема роль: **звідки конкретний later publisher отримав item або claim**.

Наприклад:

- сайт C прямо пише «за даними каналу B»;
- Telegram D має explicit forwarded-from B;
- E embed-ить оригінальний пост B.

У цих випадках можна встановити relationship C → B або D → B, навіть якщо B сам не є creator.

---

## 7. Earliest known available publisher

Це не «роль у світі», а статус у нашому поточному evidence set.

Формула:

> найраніша доступна нам публікація, яку ми змогли документально встановити на момент дослідження.

Цей статус завжди умовний і може змінитися після нової знахідки.

Тому в аналітичному тексті корисно вказувати:

- `earliest known as of YYYY-MM-DD`;
- scope пошуку;
- platforms/search methods;
- limitations.

---

## 8. Одна подія — кілька provenance chains

Уявімо:

1. людина P знімає відео;
2. надсилає його адміністратору A;
3. A публікує без credit;
4. B копіює файл і додає неправильну локацію;
5. C forward-ить B;
6. медіа D цитує C.

Тут є щонайменше три різні chains:

### Media provenance

`P → A → B → C → D`

### Caption provenance

`B → C → D`

### False location claim provenance

`B → C → D`

Якщо дослідник скаже «джерело — D», він втратить майже всю структуру.

---

## 9. Role table

Для складного кейсу використовуйте таблицю:

| Object | Entity | Role | Evidence | Confidence | Limitation |
|---|---|---|---|---|---|
| video-v1 | A | uploader/publisher | archived post | high | creator unknown |
| video-v1 | P | possible creator | A says subscriber-supplied | low | no direct identity |
| caption-v2 | B | earliest known publisher of location claim | earliest captured wording | medium | unseen earlier source possible |

Це значно точніше за фразу «source: A».

---

## 10. Типова помилка: watermark = creator

Watermark може бути:

- накладений creator;
- накладений першим publisher;
- доданий republisher;
- автоматично доданий platform/tool;
- частиною screen recording.

Тому watermark — **indicator**, а не автоматичний proof of authorship.

---

## 11. Типова помилка: «наш ексклюзив» = первинне джерело

Таке формулювання є source claim самого publisher.

Його треба оцінювати як claim:

- чи є raw/original material;
- чи є попередні публікації;
- чи є серія related items;
- чи змінювалося формулювання;
- чи має publisher history коректних attribution claims.

Самоназва не замінює verification.

---

## 12. Практична вправа

Для кожного твердження визначте, яку роль воно реально підтримує.

### A

«Канал X опублікував файл `v.mp4` о 10:14».

Підтримує: uploader/publisher для конкретної copy.

Не підтримує автоматично: creator.

### B

«Пост Y містить explicit forwarded-from X».

Підтримує: source relationship Y → X для цього forward event.

### C

«X пише: “відео надіслав читач”».

Підтримує: X сам заперечує creator role та заявляє upstream source.

Не встановлює: хто саме читач.

### D

«Файл у X і Z має однаковий SHA-256».

Підтримує: byte identity collected copies.

Не підтримує: direction X → Z.

---

## 13. Контрольне правило

Перед будь-яким attribution statement запитайте:

> Яку саме роль я зараз приписую сутності — і який evidence підтримує саме цю роль?

Якщо роль неможливо назвати одним словом, висновок, імовірно, сформульований занадто нечітко.