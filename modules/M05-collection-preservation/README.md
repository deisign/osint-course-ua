# M05 — Preliminary Assessment, Collection, Preservation & Research Logging

**Статус:** `DRAFT`  
**Phase:** Professional Foundations  
**Competencies:** C05, C17; supports C15  
**Standard:** `standards/osint-investigation-standard-v0.1.md`  
**Primary donor:** Berkeley Protocol core review

---

# 1. Module purpose

Після цього модуля студент має перестати сприймати «зберегти сторінку» як одну кнопку.

Він повинен розрізняти:

```text
discovery
→ preliminary assessment
→ collection
→ preservation
→ working copy / transformation
```

і розуміти, що кожен етап відповідає на різне питання.

---

# 2. Learning outcomes

Після модуля студент здатний:

1. пояснити різницю між discovery, collection і preservation;
2. прийняти documented collection decision до збору sensitive/irrelevant material;
3. присвоїти digital item стабільний object ID;
4. зафіксувати source/context/collection time;
5. зібрати best available representation без необґрунтованої заяви про «original»;
6. пояснити роль і межі hash value;
7. розділити reference copy і working copy;
8. задокументувати transformation;
9. оцінити preservation через authenticity, availability, identity, persistence, renderability, understandability;
10. створити evidence trail, який може перевірити інший дослідник.

Target level: C05 → L3 in this module; L4 confirmed later through capstone/peer review.

---

# 3. Key distinction: finding is not collecting

## Discovery

Ви бачите потенційно релевантний digital item.

На цьому етапі ви ще не повинні автоматично:

- завантажувати всі attachments;
- копіювати персональні дані;
- додавати все у case archive;
- вважати object релевантним.

## Preliminary assessment

Перед collection поставте питання:

1. Чи релевантний item research question?
2. Чи додає він нову information/evidence value?
3. Чи є duplicate?
4. Чи містить sensitive data?
5. Чи виправдано collection з погляду data minimisation?
6. Чи створює collection risk?
7. Чи є ризик швидкого deletion/loss?
8. Чи потрібен specialist/editor escalation?

Decision:

```text
COLLECT
COLLECT WITH RESTRICTIONS
DO NOT COLLECT
ESCALATE
DEFER
```

---

# 4. Collection

Collection — це controlled capture digital item разом із контекстом, необхідним для його подальшого розуміння та verification.

## Universal minimum

Для substantive object:

- object ID;
- source/location reference;
- collection timestamp;
- collector;
- item type;
- captured file/representation;
- sufficient context;
- collection limitations;
- integrity marker where useful.

### Web/social example

Bad collection:

```text
screenshot_123.png
```

Better collection:

```text
Object ID: CASE01-20260810-TG-0004
Platform: Telegram
Channel: @example
Message ID: 551
Displayed time: ...
Collected: ...
Text: ...
Attachment: ...
Forward context: ...
Archive/capture method: ...
Limitations: ...
```

---

# 5. The “original” trap

У курсі заборонено автоматично називати downloaded file `оригіналом`.

Можливі ситуації:

- platform recompressed media;
- uploader copied someone else’s media;
- metadata stripped;
- screenshot rather than file;
- transcoded video;
- archive captured representation, not device original.

Preferred wording:

- best available version;
- collected representation;
- file obtained from source X;
- earliest known available copy.

---

# 6. Hash values

Hash answers a narrow question:

> Are these exact bytes the same as the bytes hashed earlier?

Hash does **not** prove:

- creator;
- truthfulness;
- time/place of event;
- absence of manipulation before collection;
- legal admissibility;
- direction of transmission.

## Guided exercise

Give students two files:

- identical bytes under different filenames;
- visually similar but modified/cropped file.

Ask:

1. what hash can establish;
2. why visual similarity and byte identity differ;
3. what additional provenance is needed.

L03 synthetic media may be reused for this exercise.

---

# 7. Preservation

Collection asks:

> What did we capture and how?

Preservation asks:

> Can this object still be identified, understood and rendered later, and can we show its history?

Berkeley-derived preservation properties:

## Authenticity

Can we demonstrate the item has not been silently changed after collection, or document changes?

## Availability

Can authorised users retrieve it when required?

## Identity

Can we reliably distinguish it from other objects and link metadata to it?

## Persistence

Will it survive device/account/service changes?

## Renderability

Can it still be opened/viewed/heard with available technology?

## Understandability

Does future reviewer have enough context to interpret it?

---

# 8. Reference copy and working copy

## Reference copy

Controlled preserved representation used as baseline.

## Working copy

Used for:

- frame extraction;
- conversion;
- enhancement;
- annotation;
- transcription;
- analysis.

Substantive transformations must be logged.

---

# 9. Transformation log

Minimum:

```text
input object ID
input hash
tool + version
operation
parameters
output object ID
output hash
researcher
timestamp
```

Example:

```text
VID-0002
→ ffmpeg 8.x
→ extract frame at 00:01:13.400
→ IMG-0015
```

The extracted frame is a derived object, not the original video.

---

# 10. Demonstration case

Use L03 objects:

- R2a pre-edit archived Telegram message;
- R2b post-edit archived state;
- R7 deletion event;
- clip-A.svg;
- clip-A-crop.svg.

Demonstrate:

1. why R2a and R2b are two states of same message ID;
2. why both need preservation;
3. why deletion does not erase preserved provenance;
4. why crop gets separate object identity;
5. why edit/deletion history must not be collapsed into one row.

---

# 11. Guided exercise

Student receives five discovered items and must decide:

- COLLECT;
- COLLECT WITH RESTRICTIONS;
- DO NOT COLLECT;
- ESCALATE.

At least one item should be:

- irrelevant sensitive personal data;
- duplicate;
- volatile relevant post;
- graphic content with low research value;
- key media item likely to disappear.

Purpose: teach preliminary assessment before hoarding.

---

# 12. Independent assessment

Primary assessment is embedded in:

`labs/L03-telegram-source-tracing/`

M05-specific grading points:

- stable IDs;
- correct message-state representation;
- hashes;
- provenance;
- collection limitations;
- correct claims about hash;
- reference/derived distinction.

---

# 13. Checklist

Before moving an item to analysis:

- [ ] preliminary assessment recorded where needed;
- [ ] object ID assigned;
- [ ] source/context recorded;
- [ ] collection time recorded;
- [ ] best available representation captured;
- [ ] limitations documented;
- [ ] reference copy controlled;
- [ ] working/derived copies separated;
- [ ] transformations logged;
- [ ] preservation location known;
- [ ] sensitive access restrictions applied.

---

# 14. Common failure modes

1. Screenshot-only preservation when richer capture is available.
2. Calling platform download “original”.
3. Hash treated as authenticity/truth certificate.
4. Editing/annotating preserved reference file directly.
5. No context around cropped post screenshot.
6. Collecting every personal detail because it is public.
7. Losing edit history by overwriting old state.
8. Treating deletion as evidence of guilt/deception.
9. File stored, but no future reader can explain what it is.

---

# 15. What this method does NOT establish

Good collection/preservation does not itself establish:

- truth of the content;
- source credibility;
- creator identity;
- geolocation;
- event time;
- perpetrator;
- legal admissibility.

Those require later verification/analysis/legal assessment.

---

# 16. Required templates

- `templates/digital-object-card.md`
- `templates/collection-log.csv`
- `templates/harm-assessment.md`

---

# 17. Sources / donor traceability

Primary:

- Berkeley Protocol on Digital Open Source Investigations;
- internal audit: `research/donors/berkeley-protocol.md`.

Pending review before v1.0:

- Mnemonic/Ukrainian Archive preservation methods;
- WITNESS video-as-evidence collection/preservation guidance.

---

# 18. Tool policy

No mandatory archiving/downloader tool is fixed at this stage.

A pilot tool must pass `tool validation` in the Investigation Standard.

Module should remain teachable if a specific service disappears.

---

# 19. Status to become pilot-ready

Still required:

- split lesson/demonstration into final student-facing materials;
- guided preliminary-assessment fixture;
- independent test run;
- Mnemonic/WITNESS donor check;
- final tool path validation.
