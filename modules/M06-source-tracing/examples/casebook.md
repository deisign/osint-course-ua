# M06 Casebook — 12 міні-кейсів source tracing

Ці кейси призначені для короткого розбору після відповідних уроків. Кожен із них ізолює одну помилку або один тип provenance evidence.

Усі приклади синтетичні.

---

# E01 — Earliest known ≠ creator

## Дані

- 08:10 — канал A публікує фото: «Надіслав читач».
- 08:17 — канал B публікує те саме фото без attribution.
- 08:30 — сайт C пише «Фото каналу B».

## Питання

Хто creator?

## Розбір

Невідомо.

A — earliest known publisher у наборі, але сам заявляє upstream contributor. B — later publisher. C помилково або спрощено атрибутує photo B.

## Strongest defensible conclusion

> A є найранішою відомою публікацією фото в наборі; creator не встановлений.

## Failure mode

«A перший, значить A автор».

---

# E02 — Explicit forward

## Дані

- A — post 105.
- B — post 208, platform metadata shows forwarded from A.

## Розбір

B → A є `OBSERVED` propagation edge для конкретного forwarding event.

Це не доводить origin до A.

## Failure mode

«Раз B forward-нув A, A — original creator».

---

# E03 — Manual copy без forward label

## Дані

A о 09:00:

> «Перекрито північний в’їзд. Причина невідомаа».

B о 09:06:

> «Перекрито північний в’їзд. Причина невідомаа».

No forward/citation metadata.

## Розбір

Rare typo `невідомаа` + chronology підтримують relationship, але direction не observed.

Можливі:

- A → B;
- common upstream;
- менш імовірно B мав text раніше, але publish later.

## Conclusion

`A→B: inferred`, confidence залежить від ширшого context.

---

# E04 — Same hash, wrong direction

## Дані

Files from A and B have identical SHA-256.

A posted 10:00, B posted 10:03.

## Розбір

Доведено byte identity collected files.

Не доведено A → B.

Обидва могли отримати один file від C.

## Failure mode

«Hash збігається, отже B скачав у A».

---

# E05 — Different hashes, same media

## Дані

- A: video 1920×1080, 18 MB.
- B: video 1280×720, 4 MB.
- same sequence/content visually.
- hashes differ.

## Розбір

Different bytes можуть бути наслідком platform transcoding.

Потрібна content/technical comparison.

## Failure mode

«Hash не збігся — відео різні».

---

# E06 — Watermark lineage

## Дані

- A version: no watermark.
- B version: watermark `B`.
- C version: crop, watermark `B` still visible + new watermark `C`.

## Розбір

C-version strongly derives from a B-watermarked version or common copy already containing B watermark.

B likely upstream of C-version.

Не встановлено creator original media.

---

# E07 — Edited source and stale repost

## Дані

08:00 A:

> «Подія сталася сьогодні».

08:20 B copies A.

09:00 A edits:

> «Уточнення: відео старе».

09:30 current viewer sees only corrected A.

## Розбір

Якщо pre-edit state не preserved, незрозуміло, чому B має false claim.

Version history reconstructs propagation.

## Lesson

Preserve material edits, do not overwrite.

---

# E08 — Deletion is not confession

## Дані

- post A captured 12:00;
- unavailable 13:10;
- downstream users claim: «видалив, бо спіймали на брехні».

## Розбір

Observed:

- A existed in captured state;
- later unavailable.

Unknown:

- who deleted;
- why;
- motive;
- whether deletion related to truthfulness.

## Failure mode

Interpreting availability event as psychology.

---

# E09 — Old media, new claim

## Дані

- video appears in 2024 post without geolocation claim;
- same media reused in 2026 with caption «сьогодні в N».

## Розбір

Media provenance predates 2026 claim.

Source tracing alone already refutes «знято сьогодні» if identity of media is established.

Location still may require separate verification.

## Lesson

Trace media and caption separately.

---

# E10 — Circular reporting

## Дані

- A Telegram publishes claim X.
- B article cites A.
- C Telegram cites B.
- D article cites C.
- A posts screenshot D: «Навіть медіа підтвердили».

## Розбір

Publication count: 4+.

Independent origin count for X: potentially 1.

D не додає independent evidence merely by having a media brand.

---

# E11 — Archive capture trap

## Дані

- page says `Published: 07:30`;
- earliest Wayback capture 11:45.

## Розбір

Archive proves page state by 11:45 capture.

Page itself claims publication 07:30.

Не можна писати:

> «Page first appeared at 11:45».

Потрібні additional signals to establish actual first availability.

---

# E12 — New earlier discovery changes graph

## Initial dataset

- A 09:00;
- B 09:05, same unusual wording;
- researcher marks A → B medium confidence.

## New discovery

- C 08:40 contains same wording.

## Correct response

Не просто додати C.

Потрібно переглянути:

- A → B confidence;
- C → A/B hypotheses;
- common upstream alternative;
- earliest-known label.

## Lesson

Provenance graph is versioned analytical model, not permanent truth.

---

# Як використовувати casebook

Після кожного кейсу студент має відповісти чотирма рядками:

1. **Observed:** що прямо встановлено?
2. **Inferred:** що обґрунтовано припускається?
3. **Unknown:** що не встановлено?
4. **Overclaim to avoid:** яке найтиповіше надмірне твердження?

Цей формат готує до L03 і привчає не змішувати evidence levels.