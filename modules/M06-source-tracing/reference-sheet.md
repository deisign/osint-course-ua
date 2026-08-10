# M06 Reference Sheet — Source Tracing

Коротка робоча шпаргалка. Не замінює lesson material.

---

## 1. Спочатку уточни «source of what?»

- publication?
- exact file copy?
- media content?
- caption?
- factual claim?
- creator?
- downstream source relationship?

---

## 2. Roles

| Role | Meaning |
|---|---|
| Creator | створив первинний content |
| Uploader | завантажив конкретну copy |
| Publisher | опублікував для audience + додав context |
| Republisher | повторно опублікував existing content |
| Aggregator | системно збирає/ретранслює content |
| Source for later publisher | upstream, на який later publisher реально посилається/forward-ить |
| Earliest known available publisher | найраніший documented publisher у вашому scope |

---

## 3. Edge status

### OBSERVED

Пряме provenance evidence:

- forwarded-from;
- explicit citation/link;
- embed original;
- syndication/source field.

### INFERRED

Непрямі indicators:

- chronology;
- rare identical wording;
- same typo;
- same crop;
- same attachment order;
- version propagation.

### UNKNOWN

Relationship/content similarity є, direction недостатньо встановлений.

---

## 4. Never infer automatically

| Evidence | Does NOT automatically prove |
|---|---|
| oldest timestamp | creator / original source |
| same SHA-256 | A sent file to B |
| same text | direct copying |
| watermark | creator |
| deleted post | deception/motive |
| archive capture | publication time |
| many publications | independent corroboration |
| reputable outlet | primary independent origin |
| no forward label | independent creation |

---

## 5. Search ladder

1. exact distinctive phrase;
2. reduced phrase;
3. typo/punctuation fingerprint;
4. language variants;
5. transliteration/name variants;
6. visual/keyframe search;
7. downstream citations/embeds;
8. archives/mirrors;
9. surrounding posts/context;
10. stop condition.

---

## 6. Separate timelines

### Publication timeline

Who published when?

### Media timeline

Where did the visual/audio/file appear?

### Claim timeline

Where did location/date/accusation wording appear?

### Version timeline

How did edits/corrections change publication states?

---

## 7. Archive rules

- capture time ≠ publication time;
- earliest capture ≠ earliest publication;
- no capture ≠ page did not exist;
- dynamic assets may be missing;
- preserve archive URL + capture time + limitations.

---

## 8. Telegram rules

- record channel + message ID;
- capture forward/edit state;
- no forward marker ≠ no copying;
- deletion ≠ confession;
- preserve media separately;
- current post may not preserve prior wording;
- channel publisher ≠ eyewitness/creator.

---

## 9. Circular reporting test

Ask:

> «Does this publication add new evidence, or only repeat upstream claim?»

Count:

- publications;
- independent origins.

Не плутати.

---

## 10. Confidence statement

Для кожного key claim:

```text
Claim:
Evidence:
Contradicting evidence:
Alternative:
Confidence: high / medium / low / insufficient
Limitation:
```

---

## 11. Bounded conclusion formula

> «Станом на [date], у [search scope], [object X] є найранішою доступною нам публікацією [item/claim]. [Observed relationships]. [Inferred relationships + alternatives]. [Creator/origin unknown if applicable].»

---

## 12. Before submit

- [ ] creator ≠ uploader separated;
- [ ] earliest-known bounded;
- [ ] observed/inferred edges separated;
- [ ] media/claim provenance separated;
- [ ] edits/deletions versioned;
- [ ] archive time interpreted correctly;
- [ ] circular sources collapsed;
- [ ] alternative upstream considered;
- [ ] confidence per claim;
- [ ] limitations specific;
- [ ] no unsupported arrows.