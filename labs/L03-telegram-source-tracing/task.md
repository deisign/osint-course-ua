# L03 — Завдання

## Ситуація

До редакції/аналітичної групи надходить твердження:

> «Відео нічного удару по переправі було знято 12 квітня 2026 року під Бєлгородом і вперше опубліковане каналом `@sivernyi_signal`.»

Вам передано synthetic evidence bundle, зібраний після того, як частина повідомлень була відредагована або видалена.

Ваше завдання — **не довести чи спростувати сам удар**, а перевірити походження конкретного медіаоб’єкта та твердження про його першоджерело.

---

# 1. Research question

Дайте відповідь на питання:

> Яке найраніше доступне джерело цього медіаоб’єкта міститься в evidence bundle, які зв’язки між подальшими публікаціями можна встановити, і що пакет НЕ дозволяє стверджувати про original creator, місце та дату зйомки?

---

# 2. Матеріали

Використовуйте лише файли в `input/`.

Інтернет-пошук для основної оцінки **не потрібен і не зараховується як заміна аналізу пакета**.

---

# 3. Обов’язкові дії

## A. Inventory

1. Присвойте substantive objects object IDs.
2. Заповніть collection / object register настільки, наскільки це можливо з bundle.
3. Обчисліть hash для `clip-A.svg` та `clip-A-crop.svg`.
4. Зафіксуйте, що hash equality / inequality дозволяє і чого не дозволяє стверджувати.

## B. Timeline

Побудуйте часову таблицю всіх записів:

| Time | Channel/source | Message ID | Relationship | Media version | Important text change |
|---|---|---|---|---|---|

Використовуйте один timezone, вказаний у manifest.

## C. Propagation graph

Побудуйте мінімальний graph або edge list.

Кожен edge позначте як:

- `OBSERVED` — explicit evidence у bundle;
- `INFERRED` — логічний висновок;
- `UNKNOWN` — зв’язок неможливо встановити.

Для `INFERRED` edge обов’язково вкажіть basis і confidence.

## D. Source tracing

Визначте:

1. earliest known publication у bundle;
2. earliest publication of the **Belgorod/today claim**;
3. перший explicit forward у ланцюгу;
4. які пости є manual copies / likely copies;
5. що сталося з caption `@sivernyi_signal` після edit;
6. який вплив має deletion на provenance.

## E. Verification

Заповніть `verification-sheet.md` для claim:

> `@sivernyi_signal was the original creator and first publisher of the media.`

Окремо оцініть:

- SOURCE;
- ITEM;
- CONTENT.

## F. Analytical conclusion

Напишіть 150–250 слів.

Висновок MUST містити:

- earliest known source;
- observed propagation link(s);
- inferred link(s), якщо є;
- confidence;
- contradicting evidence;
- limitations;
- секцію `What this does not establish`.

---

# 4. Заборонені shortcuts

Не зараховується як достатній метод:

- «найстаріший timestamp = original creator»;
- «однаковий файл = доведено, хто в кого взяв»;
- «канал видалив пост = він брехав»;
- «пізніший канал повторив текст = точно скопіював саме з попереднього» без додаткових ознак;
- `verified = yes` без specified claim.

---

# 5. Що здати

```text
submission/
├── object-register.md
├── collection-log.csv
├── timeline.md
├── propagation-edges.csv
├── hashes.txt
├── verification-sivernyi-signal.md
└── conclusion.md
```

## `propagation-edges.csv`

Мінімальні поля:

```text
from_record,to_record,edge_type,basis,confidence
```

`edge_type`:

- OBSERVED
- INFERRED
- UNKNOWN

---

# 6. Pass gate

Critical fail, якщо студент:

- стверджує original creator без evidence;
- ігнорує запис, старший за `@sivernyi_signal`;
- видає inferred edge за observed;
- не фіксує edit history;
- робить висновок про геолокацію/дату зйомки, яких bundle не підтверджує;
- не залишає evidence trail до центрального висновку.

---

**Standard:** `standards/osint-investigation-standard-v0.1.md`
