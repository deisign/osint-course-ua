# L03 Synthetic Case Manifest

**Case ID:** `L03-SYN-01`  
**Collection bundle assembled:** 2026-04-12 11:00 EEST (UTC+3)  
**All displayed times in `messages.csv`:** EEST (UTC+3)  
**Scenario:** entirely fictional / synthetic.

## Bundle purpose

This package simulates a Telegram propagation chain after one relevant post was edited and later deleted.

The bundle is intentionally incomplete in the same way real open-source investigations often are:

- it contains snapshots rather than access to live accounts;
- it does not contain device-original media;
- it does not establish who physically created the clip;
- it does not establish where or when the clip was recorded;
- it includes both explicit and non-explicit propagation relationships.

## Files

- `messages.csv` — normalized message snapshots and archive records;
- `media/clip-A.svg` — best available collected representation of the repeated media object;
- `media/clip-A-crop.svg` — later cropped/screenshot-derived representation.

## Collection notes

1. Record `R2` (`@sivernyi_signal`, message 4112) was observed before deletion via an archive snapshot.
2. The same message ID was later captured after an edit; both states are represented as separate records (`R2a`, `R2b`) for analytical clarity.
3. The live message was unavailable by the time the final bundle was assembled.
4. `messages.csv` has been normalized for the exercise. It is not a literal Telegram export format.
5. `forwarded_from` is populated only when the provided snapshot explicitly displayed a forward relationship.
6. A blank `forwarded_from` field does NOT prove that no copying occurred.
7. Text equality may support an inference of copying, but does not by itself prove direction when multiple plausible sources exist.

## Media note

`clip-A.svg` and `clip-A-crop.svg` are synthetic files created only for the laboratory.

Students may hash them and compare content, but should not infer real-world geolocation, weapon type, belligerent, casualty or incident facts from the illustration.

## Research target

The viral claim to be tested is:

> `@sivernyi_signal was the original creator and first publisher of the media, filmed on 12 April 2026 near Belgorod.`

The evidence bundle was designed so that a careful investigator should **separate several different claims instead of answering them with one binary verdict**.
