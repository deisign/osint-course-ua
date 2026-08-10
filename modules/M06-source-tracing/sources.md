# M06 Sources & Donor Traceability

**Last checked:** 2026-08-10

Цей файл розділяє:

- normative / methodological sources;
- platform-primary sources;
- practitioner guides;
- course-specific synthetic materials.

Наявність source у списку не означає автоматичного копіювання його тексту або exercises.

---

# 1. Methodological core

## Berkeley Protocol on Digital Open Source Investigations

**Role:** methodology / preservation / verification / documentation  
**Status in project:** core-reviewed donor  
**Project audit:** `research/donors/berkeley-protocol.md`

Official publication:

https://www.ohchr.org/en/publications/policy-and-methodological-publications/berkeley-protocol-digital-open-source

Used in M06 for:

- separation of discovery/collection/preservation/verification;
- provenance mindset;
- reproducibility;
- source/item/content distinction as adapted in project standard;
- bounded documentation.

---

# 2. Telegram — primary platform documentation

These sources are temporally unstable and must be rechecked before live delivery.

## Telegram FAQ

https://www.telegram.org/faq

Used for:

- editing/deletion behaviour;
- channel/group baseline behaviour;
- warning that platform documentation itself may evolve.

Checked: 2026-08-10.

## Telegram API — Message constructor

https://core.telegram.org/constructor/message

Relevant fields:

- `fwd_from`;
- `edit_date`;
- `date`;
- `peer_id`;
- media-related message structure.

Checked: 2026-08-10.

## TDLib — messageForwardInfo

https://core.telegram.org/tdlib/docs/classtd_1_1td__api_1_1message_forward_info.html

Used for understanding that forwarded-message objects may carry origin/date/source information.

Checked: 2026-08-10.

## TDLib — inputMessageForwarded

https://core.telegram.org/tdlib/docs/classtd_1_1td__api_1_1input_message_forwarded.html

Important teaching implication:

copy options can produce a content copy without preserving a visible reference to the original sender. Therefore `no forward marker` cannot be treated as proof of independent creation.

Checked: 2026-08-10.

## Telegram Bot API

https://core.telegram.org/bots/api

Used as an additional current field reference, including `edit_date` and protected-content indicators.

Checked: 2026-08-10.

---

# 3. Internet Archive / Wayback Machine — primary service documentation

## Using the Wayback Machine

https://archivesupport.zendesk.com/hc/en-us/articles/360004651732-Using-The-Wayback-Machine

Used for:

- archive scope and limitations;
- missing captures;
- dynamic content issues;
- capture/search interpretation.

Checked: 2026-08-10.

## Save Pages in the Wayback Machine

https://archivesupport.zendesk.com/hc/en-us/articles/360001513491-Save-Pages-in-the-Wayback-Machine

Used for:

- Save Page Now behaviour;
- single-page capture limits;
- archive URL preservation.

Checked: 2026-08-10.

## Wayback Machine General Information

https://archivesupport.zendesk.com/hc/en-us/articles/360004716091-Wayback-Machine-General-Information

Used for:

- archive provenance/crawl context;
- dynamic-page limitations;
- non-exhaustive archive coverage.

Checked: 2026-08-10.

---

# 4. Practitioner donor

## Bellingcat — A Beginner's Guide to Social Media Verification

https://www.bellingcat.com/resources/2021/11/01/a-beginners-guide-to-social-media-verification/

**Type:** practitioner methodology / examples  
**Publication:** 2021  
**Use:** conceptual support for tracing earlier versions of social-media media, testing contextual claims, and combining simple search/reverse-search methods with critical reasoning.

Do not use as current platform documentation. Platform-specific claims must be revalidated separately.

---

# 5. Project internal standard

## OSINT Investigation Standard v0.1

`standards/osint-investigation-standard-v0.1.md`

M06 inherits:

- provenance requirements;
- observed/inferred distinction;
- qualitative confidence;
- source/item/content verification structure;
- limitations;
- peer review.

---

# 6. Synthetic educational materials

## L03 Telegram Source Tracing

`labs/L03-telegram-source-tracing/`

Synthetic controlled lab. It does not depend on live Telegram search or real persons/events.

## M06 guided exercise

`modules/M06-source-tracing/guided-exercise/`

Synthetic staged exercise designed to test model revision after discovery of earlier evidence.

## M06 Casebook

`modules/M06-source-tracing/examples/casebook.md`

Twelve synthetic micro-cases isolating distinct provenance mistakes.

---

# 7. Freshness policy

Before every live cohort, revalidate at minimum:

- Telegram forward/copy/edit/delete fields and relevant user-visible behaviour;
- archive capture/save limitations;
- optional search/reverse-search tools referenced in live demonstrations.

Core reasoning should remain valid if a particular service disappears.

Any platform-specific statement not rechecked for the current cohort should be marked `STALE / NEEDS REVALIDATION` rather than silently taught as current fact.