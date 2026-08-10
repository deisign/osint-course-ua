# M06 — Search Strategy, Source Tracing & Provenance Chains

**Статус:** `DRAFT`  
**Phase:** Search & Verification  
**Competencies:** C04, C05; supports C13  
**Primary lab:** `labs/L03-telegram-source-tracing/`  
**Standard:** `standards/osint-investigation-standard-v0.1.md`

---

# 1. Module purpose

Модуль навчає відповідати не на питання:

> «Де я це побачив?»

а на питання:

> «Яке найраніше доступне джерело конкретного матеріалу/твердження я можу встановити, як він поширювався, які зв’язки observed, які inferred, і що залишається невідомим?»

Source tracing — це не гонка за найстарішим timestamp. Це reconstruction provenance chain.

---

# 2. Learning outcomes

Після модуля студент здатний:

1. відрізняти creator, uploader, publisher, republisher і aggregator;
2. використовувати багатомовні search variants та archives для source tracing;
3. знаходити earliest known available source;
4. не називати earliest known source доведеним original creator;
5. розрізняти explicit forward/repost metadata і inferred copying;
6. виявляти circular reporting;
7. враховувати edit/deletion history;
8. будувати provenance timeline/edge list;
9. оцінювати source-tracing claim через SOURCE / ITEM / CONTENT;
10. формулювати bounded conclusion з confidence і limitations.

Target level: C04 → L3; C05 reinforcement.

---

# 3. Five identities that students commonly collapse

Для одного media item можуть існувати різні ролі:

## Creator

Особа/система, що фактично створила content/file.

## Uploader

Хто завантажив конкретну copy на platform.

## Publisher

Хто опублікував material для audience.

## Source for a later publisher

Звідки later outlet реально отримав material.

## Earliest known available publisher

Найраніша publication, яку investigator зміг встановити.

Ці ролі можуть збігатися, але це MUST бути встановлено evidence, а не припущено.

---

# 4. Source tracing workflow

```text
claim / media received
→ identify distinctive features
→ search current web/platform
→ search language/name variants
→ locate earlier copies
→ compare text/media/context
→ inspect explicit forward/repost metadata
→ inspect archives/edit history
→ build timeline
→ build observed/inferred propagation edges
→ test alternative source paths
→ state earliest known source + limitations
```

---

# 5. Search strategy

Студент повинен планувати search variants.

For text:

- exact phrase;
- distinctive fragment;
- spelling variants;
- quoted/unquoted;
- Ukrainian/Russian forms;
- transliteration;
- typo variants;
- names before/after rename.

For media:

- reverse image / visual search;
- keyframe search;
- cropped variants;
- mirrored variants;
- filenames/metadata when useful;
- context text around reposts.

For accounts:

- username history where observable;
- display-name variants;
- mirrors;
- syndication/aggregation patterns.

---

# 6. Time is evidence, not authorship

If A appears at 08:00 and B at 09:00, the evidence supports:

> A is earlier than B in the observed dataset.

It does NOT automatically support:

> B copied from A.

Possible alternatives:

- both copied from unseen C;
- B had item before publication;
- timestamps reflect different timezones/platform displays;
- archive did not capture an earlier source;
- A reposted material created offline.

Therefore direct propagation edges need additional basis.

---

# 7. Observed vs inferred propagation

## OBSERVED edge

Explicit evidence indicates relationship.

Examples:

- forwarded-from metadata;
- syndication field;
- direct source citation;
- embedded original post;
- explicit link to source.

## INFERRED edge

Relationship is analytically plausible but not directly encoded.

Possible indicators:

- later timestamp;
- identical unusual text;
- same media;
- same typo;
- same crop;
- same ordering of multiple attachments;
- unique caption change repeated downstream.

Inference MUST state confidence and alternative paths.

---

# 8. Media equality and similarity

## Byte-identical

Same cryptographic hash of compared files.

Supports:

> these collected files contain identical bytes.

Does not prove:

- creator;
- transmission direction;
- event truth;
- first publication.

## Visually same but byte-different

Possible causes:

- platform recompression;
- crop;
- resize;
- screenshot;
- metadata change;
- transcoding;
- edit/manipulation.

Source tracing may require both technical and contextual comparison.

---

# 9. Text fingerprinting

Repeated distinctive wording can help reconstruct propagation.

Strong clues:

- unusual phrase;
- same rare typo;
- same punctuation error;
- same mistranslation;
- same specific order of details.

But repeated text can still derive from shared upstream source.

Correct conclusion may be:

> R3 likely copied R2 or a common source carrying the identical wording.

not:

> R3 definitely copied R2.

---

# 10. Circular reporting

Five publications do not equal five independent sources if all derive from one origin.

Student MUST distinguish:

```text
number of publications
vs
number of independent evidence origins
```

A propagation graph can reveal apparent corroboration that is actually duplication.

---

# 11. Edits and deletions

## Edit

A single message ID may have multiple observed states.

Material edit MAY change:

- factual claim;
- source attribution;
- location/date;
- certainty;
- accusation;
- correction.

Both states SHOULD be preserved if material to the analysis.

## Deletion

Deletion:

- makes live verification harder;
- increases importance of preserved snapshots;
- does not prove deception;
- does not invalidate a properly documented earlier capture.

---

# 12. SOURCE / ITEM / CONTENT model for source tracing

## SOURCE

- Who published?
- What relationship do they claim to the media?
- Do they say “our footage”, “subscriber sent”, “repost”, etc.?
- Is source identity stable?

## ITEM

- Same exact file or derived copy?
- Earliest known version?
- Metadata/transformations?
- Edit/recompression/crop history?

## CONTENT

- Does the media itself support contextual claims?
- Does repeated caption provide actual corroboration?
- Do external facts support location/date?

---

# 13. Demonstration case — L03

Use synthetic chain:

```text
R1 @road_cam_archive
R2a @sivernyi_signal
R3 @front_watch
R4 @news_region
R5 @volnaya_lenta
R2b edited @sivernyi_signal
R6 web mirror
R7 deletion event
```

Key teaching moments:

1. R1 is earlier than R2a.
2. R1 says subscriber-supplied → creator unknown.
3. R2a introduces a new context claim.
4. R3 duplicates R2a exactly, but no explicit forward → inferred.
5. R4/R5 have explicit forward paths.
6. R2b materially retracts/qualifies context.
7. deletion does not erase archived states.

---

# 14. Guided exercise

Before full L03, give students a four-record mini-chain:

- A — earliest timestamp, no source claim;
- B — later identical media, explicit “forwarded from A”;
- C — earlier archive than A discovered later;
- D — independent-looking article actually links B.

Ask students to revise their graph after C appears.

Purpose: demonstrate that provenance chain is provisional and evidence-dependent.

---

# 15. Independent assessment

Primary:

`labs/L03-telegram-source-tracing/`

Student submits:

- object register;
- timeline;
- propagation edges;
- hashes;
- verification sheet;
- analytical conclusion.

---

# 16. Checklist

- [ ] earliest known source identified with timestamp/reference;
- [ ] original creator claim separated;
- [ ] all material edits included;
- [ ] deleted content relies on preserved evidence, not memory;
- [ ] observed/inferred edges separated;
- [ ] circular sources collapsed conceptually;
- [ ] media equality/similarity correctly described;
- [ ] alternative source paths considered;
- [ ] SOURCE / ITEM / CONTENT assessed;
- [ ] confidence given per claim;
- [ ] limitations explicit.

---

# 17. Common failure modes

1. Oldest timestamp = creator.
2. Same hash = A sent file to B.
3. Same caption = explicit repost.
4. Ten reposts = ten confirmations.
5. Deleted post = confession.
6. Edited post overwritten instead of versioned.
7. Archive timestamp confused with publication timestamp.
8. Earliest source found in one search engine treated as absolute first publication.
9. Viral caption treated as evidence for location/date.
10. `verified` used without specified claim.

---

# 18. What this method does NOT establish

Source tracing alone does not establish:

- physical creator;
- filming location;
- filming time;
- truth of depicted event;
- responsibility for event;
- intent of publisher;
- whether unseen offline/private source exists.

---

# 19. Sources and donor traceability

Methodological core:

- OSINT Investigation Standard v0.1;
- Berkeley Protocol verification/provenance principles;
- later Bellingcat/archive/platform-specific donor review pending.

L03 is synthetic and intentionally does not depend on live Telegram behaviour or third-party search services.

---

# 20. Tool policy

Search/reverse-search/archive tools are replaceable.

A future live variant may specify current tools, but controlled core assessment must remain solvable if one service changes or disappears.

---

# 21. Status to become pilot-ready

Still required:

- independent human run of L03;
- final guided mini-exercise fixture;
- current search/archive tool validation for optional live demonstration;
- Bellingcat/source-tracing donor review;
- split final lesson material if needed for learning platform.
