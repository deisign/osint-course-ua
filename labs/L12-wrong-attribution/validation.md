# L12 — Internal validation record

**Дата:** 2026-08-10  
**Статус:** `DRAFT / internally testable`

## Structural checks

- `profiles.csv`: 2 synthetic candidates;
- `observations.csv`: 15 unique observations;
- `claims.csv`: 10 unique claims;
- all CSV structures parse correctly;
- provenance-strength distribution intentionally includes `strong`, `medium`, `weak` and `none`;
- no real person, unit, place or event is used.

## Bias / attribution checks

The dataset intentionally prevents a clean positive attribution.

### P-A

Relevant support:

- historical username continuity lead;
- weak linguistic similarity.

Material contradictions / limits:

- long cross-platform continuity gap;
- no unique identifier linking the Telegram account;
- current Z-17 affiliation contradicted by transfer record;
- strong independent livestream evidence contradicts physical presence at K-4 at the upload time.

### P-B

Relevant support:

- current Z-17 affiliation;
- non-unique falcon-themed visual similarity.

Limits:

- no direct account-control evidence;
- no verified K-4 location evidence;
- unknown location is explicitly not positive evidence.

### Third-person / shared-account hypotheses

Remain viable by design. The data does not contain a hidden observation that uniquely identifies P-A or P-B.

## Time/provenance checks

The lab forces separation of:

- upload time;
- capture time;
- account control;
- image creation;
- physical presence.

O15 deliberately creates a challenge to the caption `K-4 now` without becoming definitive capture-time proof because archive-label provenance is incomplete.

## Expected claims outcome

- C1: insufficient evidence;
- C2: insufficient evidence;
- C3: partially supported;
- C4: contradicted;
- C5: insufficient evidence;
- C6: insufficient evidence;
- C7: insufficient evidence;
- C8: insufficient evidence;
- C9: contradicted or insufficient evidence depending on treatment of unknown capture time, with explanation required;
- C10: insufficient evidence.

## Pedagogical success condition

The lab is successful if the student finishes with **lower attribution confidence but higher analytical precision**.

The intended lesson is not `P-A is wrong, therefore P-B is right`. It is:

> removing one hypothesis does not automatically prove another.

## Remaining gate before `pilot-ready`

- independent human run without oral hints;
- measured completion time;
- review for accidental ambiguity in claim wording;
- grading calibration using at least one independent submission.
