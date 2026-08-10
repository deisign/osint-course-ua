# L12 — Instructor solution

Ця лабораторна має одну головну педагогічну пастку: студент може правильно помітити, що початкова версія про P-A слабка, але потім просто **перестрибнути на P-B**. Це теж помилка.

Еталонний результат: позитивна атрибуція акаунта до P-A або P-B **не встановлена**.

## 1. Attribution chain

| Layer | Strongest defensible assessment |
|---|---|
| account control | unknown; neither P-A nor P-B established |
| identity behind account | unknown |
| Z-17 affiliation of account operator | plausible but not established |
| P-A physical presence at K-4 at 18:20 | strongly contradicted |
| P-B physical presence at K-4 at 18:20 | insufficient evidence |
| creator of K-4 image | unknown |
| specific action / responsibility | not established for either candidate |

## 2. Observation weighting

### O01 — historical username match to P-A

**Value:** medium support for H1, but not decisive.

Why:

- proves P-A controlled the same string on another service in 2022-2023;
- does not prove cross-platform continuity;
- does not prove control in 2026;
- usernames can be reused, copied or independently chosen.

### O02 — Telegram account first observed only in late 2025

**Value:** weakens simple continuity narrative.

It does not prove a new owner, but creates a temporal gap requiring evidence rather than assumption.

### O03 / O10 — falcon sticker associated with P-B and Telegram image

**Value:** weak support for H2.

The sticker is commercially available and the Telegram image provenance is unknown. This is not a unique physical identifier.

### O04 — Z-17 equipment marking in Telegram image

**Value:** supports that the account has access to, receives, or republishes content associated with Z-17.

It does **not** establish that the operator belongs to Z-17.

### O05 — post captioned `K-4 now`

**Value:** establishes the account made this claim at 18:20.

It does not establish capture time, place or operator presence.

### O06 / O07 — P-A in City R livestream

**Value:** strong contradiction to claim that P-A was physically at K-4 at 18:20.

The event is continuous and timestamped; 620 km distance makes simultaneous physical presence implausible.

This does **not** disprove P-A account control because:

- material may be reposted;
- posting may be scheduled or delegated;
- account may be shared;
- caption may describe someone else's material.

### O08 — P-B location unknown

**Value:** none for positive presence claim.

Critical rule:

> unknown location ≠ evidence of presence.

### O09 — shared phrase

**Value:** very weak / non-discriminating.

Common linguistic habits should not be treated as authorship fingerprint without much stronger controlled analysis.

### O11 — P-B current Z-17 affiliation

**Value:** supports organisational affiliation only.

Does not establish account control, K-4 presence or specific action.

### O12 — P-A transferred away from Z-17

**Value:** contradicts current-affiliation claim for P-A.

Does not prove absence of personal contacts, archived content or continuing access to old materials.

### O13 — rapid repost

**Value:** demonstrates circulation.

Weakens any assumption that possession/upload equals original creation.

### O14 — stripped metadata

**Value:** strong limitation.

Prevents capture-time/device attribution from supplied file.

### O15 — earlier archive-labelled copy

**Value:** medium challenge to `now` claim.

Because archive-label provenance is incomplete, it should not be treated as definitive proof of capture on March 13. But it is enough to require the hypothesis that the image predates the Telegram post.

## 3. Competing hypotheses

### H1 — P-A controls @north_falcon77

**Support:** O01, weak O09.

**Contradictions / weaknesses:**

- long continuity gap;
- account only observed later;
- P-A no longer assigned to Z-17;
- no unique cross-platform identifier.

**Assessment:** possible, low confidence; insufficient evidence.

### H2 — P-B controls @north_falcon77

**Support:** O03, O10, O11.

**Weaknesses:**

- sticker not unique;
- affiliation does not prove account control;
- no direct account-to-person continuity.

**Assessment:** possible, low confidence; insufficient evidence.

### H3 — third unknown person controls account

**Support:** fully compatible with dataset.

**Contradiction:** none known.

**Assessment:** viable alternative; confidence cannot be meaningfully ranked above H1/H2 without more data.

### H4 — shared / delegated / non-real-time posting

**Support:** O05, O13, O14, O15 and strong distinction between upload and capture time.

**Assessment:** viable mechanism and important alternative. It explains how even correct account attribution would fail to establish physical presence.

## 4. Claims assessment

| Claim | Expected status | Reason |
|---|---|---|
| C1 P-A controls account | insufficient evidence | historical username is not enough |
| C2 P-B controls account | insufficient evidence | affiliation/sticker are not enough |
| C3 operator is Z-17 affiliated | partially supported | content suggests access/connection, but operator affiliation not proven |
| C4 P-A at K-4 | contradicted | O06/O07 strongly contradict simultaneous presence |
| C5 P-B at K-4 | insufficient evidence | location unknown |
| C6 image captured ~18:20 | insufficient evidence | upload ≠ capture; O15 challenges recency |
| C7 account controller created image | insufficient evidence | repost/delegation possible; provenance absent |
| C8 Z-17 member present when image created | insufficient evidence | equipment marking is not person presence proof |
| C9 P-A performed described action | contradicted / insufficient evidence | presence strongly contradicted; action never independently established |
| C10 P-B performed described action | insufficient evidence | no presence or action evidence |

For C9, instructor may accept `contradicted` if student explicitly grounds it in physical impossibility for the relevant time, or `insufficient evidence` if they distinguish the unknown capture time. Stronger work should explain this nuance.

## 5. Model final conclusion

> The dataset does not support positive attribution of `@north_falcon77` to either P-A or P-B. P-A's historical use of the same username is a relevant lead but not evidence of continuous cross-platform control. P-B's current Z-17 affiliation and falcon-themed gear provide only weak circumstantial support and are non-unique. Independent livestream evidence strongly contradicts P-A's physical presence at K-4 at the Telegram upload time, while P-B's location is simply unknown. The K-4 image lacks original metadata and may predate the upload; therefore account control, image creation, physical presence and specific action must remain separate unresolved questions. The most useful discriminating evidence would be a verified account-continuity artefact tied to one candidate and/or independently timestamped original media establishing capture provenance.

## 6. What evidence would materially change the assessment

Examples:

- cryptographically or platform-verifiably linked account recovery/contact information, where lawfully available;
- cross-platform continuity with unique, non-public identifier;
- original media with reliable capture metadata and provenance;
- independently timestamped content showing the candidate and location;
- verified contemporaneous communication demonstrating account control;
- evidence of shared/admin access if relevant.

The point is not to teach students to chase invasive identifiers. They should first ask **which category of evidence would discriminate between hypotheses**.

## 7. Instructor red flags

Return for revision if a submission says:

- `P-A = @north_falcon77 because username match`;
- `P-B is more likely, therefore it is P-B`;
- `P-B could have been at K-4 because we don't know where he was`;
- `the post says "now", therefore the image was made then`;
- `Z-17 equipment proves Z-17 member took the photo`;
- `whoever runs the account committed the action`.

## 8. Pedagogical success condition

A successful student becomes **less certain** after analysing the dataset, but more precise about:

- which hypotheses remain;
- which are weakened;
- which claims are contradicted;
- what evidence is actually needed next.

That is the intended outcome.
