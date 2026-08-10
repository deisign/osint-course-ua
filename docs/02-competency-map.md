# Карта компетентностей v0.1

**Курс:** «Професійний практик OSINT»  
**Версія:** 0.1  
**Дата:** 10 серпня 2026 року  
**Пов’язані документи:**

- `docs/01-graduate-profile.md`
- `curriculum/blueprint.md`

---

## 1. Призначення

Карта показує, **де саме формується і де саме перевіряється кожна компетентність**.

Позначення рівнів:

- `L1` — розуміє;
- `L2` — виконує за інструкцією;
- `L3` — самостійно застосовує;
- `L4` — захищає, рецензує, визнає межі й коригує висновок.

---

## 2. Core competencies

| ID | Компетентність | Основні модулі | Основні лабораторні / assessment | Exit level | Critical gate |
|---|---|---|---|---|---|
| C01 | Постановка дослідницького питання | M01, M03 | L01, L02, capstone | L3 | — |
| C02 | Systems thinking / territory mapping | M02, M13, U01 | L01, U01 source map | L3 | — |
| C03 | Гіпотези та collection plan | M03, M18 | L02, L12, capstone | L4 | — |
| C04 | Пошук і першоджерело | M06, M13, U01 | L03 | L3 | — |
| C05 | Provenance, preservation, reproducibility | M05, M06, M19, M20 | L03, L16, capstone | L4 | YES |
| C06 | Image/video/audio verification | M07, M08 | L04, L05 | L3 | — |
| C07 | Geolocation / chronolocation | M09–M11 | L06, L07, L15 | L3 | — |
| C08 | People / organisations / digital identities | M12, M13, U02 | L08, L14 | L3 | — |
| C09 | Data hygiene / entity resolution | M12, M14, U01 | L08 | L3 | — |
| C10 | Scaled collection / text-as-data | M16 | L10 | L2–L3 | — |
| C11 | Timelines / network analysis | M15, U03 | L09, L15 | L3 | — |
| C12 | Statistics / uncertainty / cognitive bias | M17 | L11, L12 | L3 | — |
| C13 | Analytical reasoning / attribution / confidence | M01, M03, M17–M20, U02–U04 | L02, L11, L12, L14, L15, capstone | L4 | YES |
| C14 | Peer review / red team | M19 | L13, capstone | L4 | — |
| C15 | Ethics / privacy / harm minimisation | M01, M04, M12, M20, U04–U05 | harm assessment, L14–L16, capstone | L4 | YES |
| C16 | Digital security / threat model | M04 | threat model, capstone | L4 | YES |
| C17 | Documentation / professional handoff | M05, M20, U04–U05 | L16, capstone | L4 | YES |

---

## 3. Ukraine–Russia–War specialization

| ID | Компетентність | Основні модулі | Assessment | Exit level | External review |
|---|---|---|---|---|---|
| U01 | Українське та російське джерельне середовище | U01 | regional/source ecosystem map | L3 | desirable |
| U02 | Військові підрозділи та time-bounded attribution | U02 | L14 | L3 | military SME desirable |
| U03 | Реконструкція воєнного інциденту | U03 | L15 | L3 | military/forensic SME desirable |
| U04 | Документування ймовірних міжнародних злочинів | U04 | L16 + Case C | L2–L3 | REQUIRED |
| U05 | Безпечне передавання / межі правової оцінки | U05 | L16 | L2–L3 | REQUIRED |

---

## 4. Critical gates

Наступні компетентності не можуть бути компенсовані середнім балом:

### C05 — provenance і reproducibility

Незарахування, якщо:

- неможливо встановити походження ключового матеріалу;
- оригінал і робоча копія змішані без пояснення;
- суттєві перетворення не задокументовані;
- доказовий trail неможливо повторити.

### C13 — evidence-to-conclusion discipline

Незарахування, якщо:

- висновок сильніший за наявні підтвердження;
- суперечливі дані приховані;
- membership/presence/participation/responsibility змішані без окремих доказів;
- рівень упевненості не відповідає матеріалу.

### C15 — ethics / harm minimisation

Незарахування, якщо:

- студент без потреби розкриває чутливі персональні дані;
- створює невиправданий ризик для джерела, постраждалого або третьої особи;
- порушує правила навчального кейсу щодо реальних людей.

### C16 — security

Незарахування, якщо:

- student workflow створює очевидний і невиправданий ризик компрометації;
- порушено встановлену threat model без документованої причини.

### C17 — documentation / handoff

Незарахування, якщо:

- переданий пакет не дозволяє іншому фахівцю зрозуміти джерела, метод, обмеження та статус тверджень.

---

## 5. Coverage matrix by phase

| Phase | Primary competency range | Main purpose |
|---|---|---|
| Foundations | C01–C05, C15–C16 | правильно поставити і безпечно організувати дослідження |
| Verification | C04–C07 | перевірити походження, item, content, place, time |
| Entities/Data/Scale | C08–C12 | структурувати, очищати, масштабувати і не помилятися в сутностях/числах |
| Analysis/Output | C03, C05, C13–C17 | сформувати обмежений evidence-based висновок і передати його |
| UA/RU/War | U01–U05 + C05/C13/C15/C17 | застосувати core discipline у високоризиковому контексті війни |

---

## 6. Assessment coverage rule

Кожна компетентність повинна мати:

1. **instruction point** — де вона вперше пояснюється;
2. **guided practice** — де виконується за зразком;
3. **independent assessment** — де студент застосовує її без покрокової інструкції;
4. **capstone evidence** — якщо компетентність є професійно критичною.

Компетентність не вважається покритою лише тому, що тема згадана в лекції.

---

## 7. Pilot coverage

Пілотна версія має перевірити мінімально:

- C01–C07;
- C09;
- C12–C17;
- introductory U01/U02.

C08, C10, C11 і повні U03–U05 можуть бути представлені скорочено, якщо це потрібно для реалістичного часу пілоту, але мають бути присутні у повній версії курсу.

---

## 8. Наступна версія

`v0.2` має додати:

- rubric indicators для `L1–L4` по кожній компетентності;
- конкретні assessment weights;
- prerequisite checks;
- mapping до зовнішніх стандартів після завершення donor-аудитів;
- окрему таблицю SME/expert validation requirements.
