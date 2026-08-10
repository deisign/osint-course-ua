# L03 — Instructor Solution

**Do not distribute with student bundle.**

## 1. Expected hashes

Assuming exact repository files:

```text
clip-A.svg
SHA-256: 584d05ec2b575272d38d86c6ebe1cfc894e5c174bd383c03c7ab7a5b0a06b208

clip-A-crop.svg
SHA-256: fbc223ae7765d0272ee4a8c148d2e1f95d6243d6347c40c8fe83799d0181d7f4
```

Interpretation:

- `clip-A.svg` is the same collected file referenced by R1, R2a/R2b, R3, R4 and R6 in the synthetic dataset.
- `clip-A-crop.svg` is a different byte sequence and a visibly derived representation.
- Identical hashes for the same file establish byte-level identity of the collected representation, **not authorship, event date, location or direction of copying**.

---

## 2. Correct timeline

| Time EEST | Record | Source | Key event |
|---|---|---|---|
| 2026-04-11 21:42 | R1 | @road_cam_archive | earliest known publication in bundle; says subscriber-supplied and location unknown |
| 2026-04-12 08:17 | R2a | @sivernyi_signal | first bundle occurrence of `today near Belgorod` claim |
| 08:26 | R3 | @front_watch | identical text/media to R2a but no explicit forward marker |
| 08:34 | R4 | @news_region | explicit forward from @front_watch |
| 08:45 | R5 | @volnaya_lenta | explicit forward from @news_region; stronger claim; cropped derivative media |
| 09:05 | R2b | @sivernyi_signal | same message ID edited: says clip is not from today and place unconfirmed |
| 09:12 | R6 | synthetic web mirror | mirror identifies @front_watch as its source |
| 10:12 | R7 | @sivernyi_signal | deletion event for message 4112 |

---

## 3. Expected propagation assessment

### OBSERVED edges

```text
R3 -> R4
```

Basis: R4 explicitly displays `forwarded_from = @front_watch`.

```text
R4 -> R5
```

Basis: R5 explicitly displays `forwarded_from = @news_region`.

```text
R3 -> R6
```

Basis: synthetic mirror record explicitly identifies @front_watch as source.

### Reasonable INFERRED edge

```text
R2a -> R3
```

Basis:

- R3 is later;
- R3 has byte-identical collected media representation;
- R3 text is exactly identical to R2a;
- the wording is more specific than R1.

However, the evidence does not exclude a shared unseen source. Correct confidence: **moderate**, not high/absolute.

### R1 relationship

R1 is earlier and uses the same collected media representation, therefore it contradicts the claim that @sivernyi_signal was the first publisher in the bundle.

But the direct edge:

```text
R1 -> R2a
```

is **not observed**.

It may be inferred as plausible reuse, but an unseen intermediary or common subscriber source remains possible.

Best grading response:

```text
R1 -> R2a : UNKNOWN / plausible inferred relationship, insufficient evidence for direct copying
```

---

## 4. Source-tracing findings

### Earliest known publication in the bundle

`R1 — @road_cam_archive — 2026-04-11 21:42 EEST`.

### Original creator

**Unknown.**

R1 itself says the clip was supplied by a subscriber. Therefore even the earliest known publication in the bundle explicitly points to an earlier, unidentified origin.

### Earliest bundle appearance of the “today near Belgorod” claim

`R2a — @sivernyi_signal — 2026-04-12 08:17 EEST`.

This is a different question from earliest media publication.

### Effect of the edit

R2b materially weakens/withdraws the original contextual claim:

- `not from today`;
- `location not confirmed`;
- `subscriber-supplied`.

The same message ID must be represented as two observed states plus the later deletion event.

### Effect of deletion

Deletion does not erase prior provenance if an adequately documented archive snapshot exists.

It does increase reliance on preserved copies and makes live re-verification impossible from that message alone.

Deletion itself is not proof of deception or guilt.

---

## 5. Expected verification of claim

Claim:

> `@sivernyi_signal was the original creator and first publisher of the media.`

### SOURCE

- @sivernyi_signal is a publisher of the item in R2a/R2b.
- Its edited text explicitly states subscriber-supplied material.
- Therefore creator status is unsupported and contradicted by its own later caption.

### ITEM

- The bundle contains the same collected representation in R1 earlier than R2a.
- Therefore @sivernyi_signal is not the earliest known publisher in this bundle.

### CONTENT

- The synthetic media itself does not establish creator, location, date or belligerent.
- The original Belgorod/today caption is later retracted/qualified by the same message ID.

### Result

Recommended status:

```text
CONTRADICTED for claim that @sivernyi_signal was first publisher in the bundle.
INSUFFICIENT DATA for original creator.
INSUFFICIENT DATA for filming location/date.
```

---

## 6. Example analytical conclusion

> У наданому пакеті найранішою відомою публікацією медіа є повідомлення `@road_cam_archive` від 11 квітня 2026 року о 21:42 EEST, тобто воно передує повідомленню `@sivernyi_signal` більш ніж на десять годин. Це суперечить твердженню, що `@sivernyi_signal` був першим видавцем у межах доступного evidence bundle. Водночас `@road_cam_archive` прямо зазначає, що файл надіслав підписник, тому пакет не дозволяє встановити original creator. Формулювання про зйомку «сьогодні під Бєлгородом» уперше з’являється в R2a (`@sivernyi_signal`, 08:17), після чого дослівно повторюється R3; зв’язок R2a→R3 є обґрунтованим, але лише inferred, оскільки explicit forward відсутній. R3→R4 та R4→R5 підтверджені explicit forward metadata. О 09:05 той самий пост `@sivernyi_signal` було відредаговано: канал уточнив, що ролик не є сьогоднішнім і місце не підтверджено. Рівень упевненості високий щодо earliest known publication у bundle та observed forwards, помірний щодо R2a→R3, недостатній щодо original creator, місця й дати зйомки.

### What this does not establish

- who physically created the clip;
- where the clip was filmed;
- when the underlying event occurred;
- what caused the depicted event;
- which actor or belligerent was responsible;
- whether R1 directly supplied R2a.

---

## 7. Common failure modes

### Failure A — sorting by time and declaring authorship

Student says R1 is creator because it is earliest.

Correction: earliest known publisher ≠ creator; R1 itself says subscriber-supplied.

### Failure B — treating identical text as explicit forwarding

Student marks R2a→R3 OBSERVED.

Correction: identical wording supports inference but does not create platform metadata that is absent.

### Failure C — ignoring edit state

Student uses only R2a and misses R2b.

Critical because edit materially changes the contextual claim.

### Failure D — hash mysticism

Student says identical hash proves R1 supplied R2a.

Correction: it proves identical collected bytes, not transmission direction.

### Failure E — proving Belgorod from caption

Student treats a repeated caption as independent confirmation.

Correction: repeated text in dependent propagation chain is not external corroboration.

---

## 8. Instructor test before pilot

Before assigning the lab, instructor should independently:

1. clone/download the current repository;
2. compute SHA-256 of both media files;
3. verify that expected hashes above match;
4. open `messages.csv` in a spreadsheet and confirm timestamps parse correctly;
5. complete the task from student instructions only;
6. record actual completion time;
7. report ambiguous wording as a course bug rather than explaining it orally.
