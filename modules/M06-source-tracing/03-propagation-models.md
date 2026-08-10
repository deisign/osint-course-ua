# M06.3 — Моделі поширення: observed, inferred, common upstream

## Навчальна мета

Після цього розділу студент має вміти будувати provenance graph, у якому напрям передачі не вигадується з одного лише timestamp або схожості content.

---

## 1. Найнебезпечніша спокуса

Маємо дві публікації:

- A — 08:02;
- B — 08:07;
- однаковий текст і те саме фото.

Інтуїтивний висновок:

`A → B`

Але evidence реально підтримує лише:

- A зафіксований раніше за B;
- content у A і B схожий або ідентичний.

Можливі щонайменше чотири моделі:

```text
1. A → B
2. B отримав content раніше, але опублікував пізніше
3. C → A і C → B
4. A і B отримали content через різні невидимі канали
```

Тому напрям propagation edge — окреме твердження, яке потребує окремої підстави.

---

## 2. OBSERVED edge

Edge має статус `OBSERVED`, коли джерело прямо кодує або заявляє relationship.

Типові приклади:

- explicit forwarded-from metadata;
- direct hyperlink «source»;
- embedded original post;
- RSS/syndication source field;
- article says «as first reported by X»;
- quoted message with stable reference;
- API field linking object to original.

### Важливо

Observed relationship доводить **конкретний зв’язок, який спостерігається**, але не обов’язково всю історію.

Наприклад, explicit forward B ← A підтверджує, що B forward-нув A. Він не доводить, що A є creator або earliest publication globally.

---

## 3. INFERRED edge

Edge має статус `INFERRED`, коли direction/relation реконструюється з непрямих ознак.

Можливі індикатори:

- пізніший timestamp;
- дослівно повторений рідкісний текст;
- однакова помилка;
- однаковий нестандартний crop;
- однакове неправильне число;
- однаковий порядок attachments;
- downstream повторює edit, який з’явився в upstream;
- специфічна watermark chain.

### Правило

Жоден індикатор сам по собі не перетворює inference на observation.

Коректна мова:

> «B, імовірно, запозичив формулювання з A або зі спільного upstream source».

Некоректна:

> «B точно вкрав у A».

---

## 4. UNKNOWN edge

Іноді ми знаємо, що два objects пов’язані content-wise, але не можемо навіть обґрунтовано встановити direction.

Тоді краще зафіксувати:

`A —?— B`

і пояснити:

> «Виявлена сильна схожість content, але напрям поширення невідомий».

Це краще, ніж намалювати стрілку для краси графа.

---

## 5. Common upstream source

Одна з головних альтернатив будь-якому apparent copy relationship:

```text
    C
   / \
  A   B
```

A і B можуть бути незалежними publishers лише в сенсі того, що вони не копіювали один одного. Але вони все одно можуть залежати від **одного upstream source**.

Це критично для corroboration.

Два outlets, які отримали відео від одного press office, не є двома незалежними origins для claim про подію.

---

## 6. Circular reporting

Класичний патерн:

```text
Telegram A
  ↓
Site B
  ↓
Channel C
  ↓
Site D cites C
  ↓
Channel A cites D as confirmation
```

На поверхні:

- Telegram;
- два сайти;
- інший канал;
- багато reposts.

Насправді інформаційний origin може бути один — A.

### Ознаки circular reporting

- усі тексти мають одну специфічну деталь;
- outlets посилаються один на одного;
- немає independent primary material;
- timestamps утворюють downstream chain;
- «confirmation» повертається до початкового джерела.

---

## 7. Propagation edge schema

Для кожного edge зберігайте мінімум:

| Field | Meaning |
|---|---|
| from_object | upstream candidate/source |
| to_object | downstream object |
| status | observed / inferred / unknown |
| basis | explicit forward, citation, identical typo, etc. |
| timestamp_relation | known / approximate |
| confidence | high / medium / low |
| alternatives | common upstream, reverse direction, unknown |
| evidence_ref | source/object IDs |

Граф без basis — це малюнок, а не аналітичний артефакт.

---

## 8. Часова логіка

Timestamp допомагає відкидати неможливі моделі.

Якщо A опубліковано о 12:00, а B о 11:30, модель `A → B` через **публічну публікацію A** неможлива.

Але це не виключає:

- приватної передачі до 11:30;
- scheduled post;
- timezone mismatch;
- некоректного platform timestamp;
- archive timestamp, переплутаного з publication time.

Тому час — сильний constraint, але не повна provenance answer.

---

## 9. Version propagation

Особливо корисний індикатор — поява **версій**.

Приклад:

- A v1: «12 загиблих»;
- A v2 після edit: «2 загиблих»;
- B: «12 загиблих»;
- C: «2 загиблих».

Це може підтримувати різні часові paths:

- B отримав claim до correction;
- C — після correction;
- або B/C мали інші upstream sources.

Version history дозволяє будувати provenance точніше, ніж один current screenshot.

---

## 10. Media transformation chain

Поширення медіа часто залишає технічний слід:

```text
original 1920×1080
→ platform transcode 1280×720
→ crop 1080×720
→ screenshot 1170×2532
→ repost with watermark
```

Це може допомогти встановити **derivation**, але не завжди direction між publishers.

Якщо B має crop, який містить watermark A, це сильніше підтримує `A-version → B-version`.

Якщо A і B мають різні transcodes одного unseen original, common upstream може бути кращою гіпотезою.

---

## 11. Приклад: неправильний граф

Дані:

- A 07:50 — відео без source label;
- B 08:00 — те саме відео;
- C 08:04 — explicit forward from B;
- D 08:15 — article embeds C;
- E 07:45 — archive знайдений пізніше, uploader unknown.

Початковий граф дослідника:

`A → B → C → D`

Після E він має бути переглянутий.

Коректніше:

```text
E  earliest known
|
? relationship to A/B
|
A ? B → C → D
```

Тобто discovery нового earlier object не просто «додає ще один вузол», а змінює confidence у попередніх edges.

---

## 12. Вправа: класифікація edges

### Case 1

B має explicit forwarded-from A.

**Статус:** observed.

### Case 2

B на 4 хвилини пізніше повторює рідкісну друкарську помилку A.

**Статус:** inferred, medium/high залежно від контексту; common upstream лишається альтернативою.

### Case 3

A і B мають однаковий файл, але B опубліковано раніше.

**Статус:** сам факт equality не визначає direction.

### Case 4

Article D прямо посилається на C, а C — на B.

**Статус:** D → C observed; C → B observed. Це не доводить B → origin.

---

## 13. Критерій професійної якості

Кожна стрілка у вашому provenance graph повинна пережити питання reviewer-а:

> «Звідки ви знаєте саме напрям?»

Якщо відповідь — «ну A ж раніше», edge треба понизити до inferred або unknown.