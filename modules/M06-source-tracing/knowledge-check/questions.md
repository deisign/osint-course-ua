# M06 Knowledge Check

## Інструкція

Відповідайте коротко, але конкретно. Якщо питання стосується confidence або provenance, називайте **яке саме твердження** ви оцінюєте.

---

## 1. Multiple choice

Канал A опублікував відео о 09:00, канал B — о 09:05. Файли byte-identical. Яке твердження підтримано найкраще?

A. A є creator.
B. B скопіював відео з A.
C. Зібрані files є byte-identical, а A у observed dataset опублікований раніше.
D. A є original source.

---

## 2. Short answer

Чим відрізняються `creator` і `uploader`?

---

## 3. Multiple choice

Post B має explicit forwarded-from A. Що це доводить?

A. A створив media.
B. B був створений як forward із origin A для цього event.
C. A опублікував material першим у світі.
D. Caption A правдивий.

---

## 4. Short answer

Чому відсутність forward label не доводить незалежне походження post?

---

## 5. Classification

Класифікуйте edge:

A о 10:00 пише «вул. Північна перекритааа».
B о 10:04 повторює той самий rare typo. Explicit source absent.

`OBSERVED / INFERRED / UNKNOWN` — і чому?

---

## 6. Multiple choice

Найраніший Wayback capture сторінки — 14:20. На сторінці написано `Published 09:10`. Який висновок коректний?

A. Сторінка точно з’явилась о 14:20.
B. Сторінка точно з’явилась о 09:10.
C. Archive зафіксував цей state о 14:20; сама сторінка заявляє publication time 09:10.
D. Archive timestamp не має evidence value.

---

## 7. Short answer

Що таке circular reporting?

---

## 8. Scenario

Telegram A публікує claim. Site B цитує A. Channel C цитує B. Newspaper D цитує C.

Скільки independent origins ми можемо впевнено рахувати для цього claim без додаткового evidence?

---

## 9. Multiple choice

Post був captured о 08:00 і видалений до 09:00. Яке твердження НЕ підтримується deletion event?

A. Post був доступний у captured state о 08:00.
B. Пізніше він був недоступний.
C. Автор видалив його, бо визнав брехню.
D. Current live verification стала складнішою.

---

## 10. Short answer

Наведіть два приклади material edit, які треба version-preserve.

---

## 11. Scenario

Video є в post 2024 року. У 2026 same media публікують із caption «це сталося сьогодні в N».

Що source tracing може встановити ще до геолокації?

---

## 12. Multiple choice

Що означає однаковий SHA-256 двох collected files?

A. Один publisher передав файл іншому.
B. Files містять однакові bytes.
C. Files створила одна людина.
D. Caption обох правдивий.

---

## 13. Short answer

Що таке `earliest known available source` і чому це формулювання bounded?

---

## 14. Confidence

Дано:

- A earlier than B;
- same unusual text;
- no forward/citation;
- common upstream possible.

Який confidence доречний для claim `B copied directly from A` і чому?

---

## 15. Red-team

Знайдіть overclaim:

> «Ми верифікували відео: канал A опублікував його раніше за інші знайдені нами канали».

Перепишіть висновок професійно.

---

## 16. Source roles

Publication X каже «відео надіслав підписник».

Що це говорить про:

- X as publisher;
- X as creator;
- subscriber identity?

---

## 17. Archive negative evidence

Wayback не має жодного capture URL до 2025 року. Чи можна стверджувати, що page не існувала у 2024? Поясніть.

---

## 18. New evidence

Після завершення provenance graph знайдено earlier record, який містить той самий distinctive wording.

Назвіть щонайменше три речі, які треба переглянути в analysis.

---

## 19. Independent corroboration

Який із варіантів додає найсильніший independent evidence path до Telegram claim про пошкодження будівлі?

A. П’ять reposts Telegram claim.
B. Article, який цитує один із reposts.
C. Незалежно датоване satellite imagery, що показує damage.
D. Screenshot того самого Telegram post у Facebook.

---

## 20. Final principle

Закінчіть речення:

> «Source tracing встановлює provenance публікацій/claims/media, але сам по собі не встановлює...»

Наведіть щонайменше три приклади.