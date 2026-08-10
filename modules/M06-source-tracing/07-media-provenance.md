# M06.7 — Media provenance: однаковий контент, різні файли

## Навчальна мета

Після цього розділу студент має вміти розрізняти byte identity, visual similarity, derived copies та context reuse, не роблячи з технічної схожості надмірних висновків про авторство або напрям передачі.

---

## 1. «Те саме відео» — нечітке формулювання

У практиці OSINT фраза «це те саме відео» може означати щонайменше чотири різні речі:

1. **byte-identical file** — однакові байти;
2. **same visual content** — однакова сцена, але файл змінений;
3. **derived version** — crop, resize, transcode, screenshot, watermark;
4. **same event, different recording** — інший ракурс/пристрій.

Ці рівні мають різну доказову силу.

---

## 2. Byte identity

Якщо SHA-256 двох collected files однаковий, коректний висновок:

> «Порівняні файли є byte-identical».

Це сильний technical fact.

Але він не доводить:

- creator;
- direction transmission;
- first publication;
- truth of caption;
- event date/location.

Два publishers могли незалежно скачати один файл із третього source.

---

## 3. Byte difference не означає різний content

Platform processing часто змінює файл:

- recompression;
- transcoding;
- metadata stripping;
- resolution;
- thumbnail generation;
- container format.

Тому різні hashes не виключають common media origin.

Потрібні content-level comparisons.

---

## 4. Derived copies

Типові transformations:

### Crop

Видалена частина кадру.

### Resize

Змінена resolution без суттєвої зміни content.

### Screenshot

Media перетворено на screenshot UI/player.

### Screen recording

Original video став частиною нового recording.

### Watermark overlay

Publisher додає logo/channel name.

### Caption burned-in

Текст стає частиною pixels.

### Re-encode

Змінюються codec/bitrate/container.

Кожна transformation може створити provenance clue.

---

## 5. Transformation direction

Деякі ознаки дозволяють підтримати direction.

Наприклад:

- B містить watermark A;
- B crop-ить рамку, яка є у A;
- B містить screenshot UI публікації A.

Це сильніше підтримує:

`A-version → B-version`

ніж проста similarity.

Але все одно потрібно розглядати:

- unseen common source already carrying watermark;
- downloaded/re-uploaded copy;
- mirrored version.

---

## 6. Keyframes для video source tracing

Для відео використовуйте кілька keyframes:

- opening frame;
- visually distinctive frame;
- signage/text frame;
- rare object;
- closing frame.

Чому кілька:

- платформи можуть обрізати початок;
- thumbnail може бути не representative;
- mirrored/cropped version може приховати одну clue;
- один кадр може давати false match.

---

## 7. Watermarks

Watermark корисний як fingerprint, але має обмеження.

### Може означати

- branding publisher;
- claim of ownership;
- automated repost system;
- downstream source clue.

### Не доводить

- creator;
- eyewitness status;
- original publication;
- authenticity of event.

Завжди перевіряйте, чи watermark:

- був у ранній version;
- з’явився downstream;
- перекриває інший watermark;
- є частиною screenshot.

---

## 8. Metadata

Metadata може допомогти, але її статус треба оцінювати обережно.

Проблеми:

- platforms strip metadata;
- metadata can be edited;
- export/transcode changes fields;
- creation time може означати file creation after download/conversion.

Metadata — один indicator серед інших, а не абсолютний truth source.

---

## 9. Same media, different claim

Критична вправа source tracing — побудувати окремі timelines:

### Media timeline

Коли і де з’являється visual object.

### Caption/claim timeline

Коли з’являється конкретне твердження.

Приклад:

- video — 2024;
- claim «знято сьогодні в N» — 2026.

Media authentic у сенсі «реальне відео», але current contextual claim false/misleading.

---

## 10. Same event, different media

Інший сценарій:

- video A;
- photo B;
- CCTV C;

усі можуть показувати ту саму подію.

Це не propagation chain одного item, а **corroboration across separate items**.

Не змішуйте ці моделі.

---

## 11. Media object card

Для кожного важливого object зберігайте:

- object ID;
- collected filename;
- source publication ID;
- collection time;
- hash;
- size/dimensions/duration;
- observed watermark;
- transformation notes;
- related objects;
- similarity basis;
- original/reference vs working copy.

---

## 12. L03 example

`clip-A.svg` і `clip-A-crop.svg`:

- не byte-identical;
- content явно related;
- crop є derived representation;
- наявність crop downstream не означає, що downstream publisher знає creator;
- provenance треба описувати як transformation relationship між objects.

---

## 13. Типові помилки

1. Different hash = different event.
2. Same hash = direct transmission A → B.
3. Watermark = creator.
4. Earliest visible watermark = original camera source.
5. Screenshot = adequate preservation of original file.
6. Metadata field = unquestionable fact.
7. Same scene = same file lineage.
8. Same video = same caption provenance.

---

## 14. Checklist

- [ ] byte identity перевірена окремо від visual similarity;
- [ ] transformations описані;
- [ ] source publication object linked;
- [ ] media lineage separated from claim lineage;
- [ ] watermark treated as indicator;
- [ ] hashes interpreted narrowly;
- [ ] original/reference and working copies separated;
- [ ] direct transmission not inferred from equality alone;
- [ ] alternative common upstream considered.

---

## 15. Основне правило

Технічна схожість відповідає на питання **про files/content**. Вона не повинна непомітно перетворюватися на висновок **про людей, авторство або істинність події**.