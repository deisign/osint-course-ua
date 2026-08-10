# M06 Guided Exercise — Instructor solution

## Phase 1 expected reasoning

### Earliest known publication

A at 08:12.

### Creator

Unknown.

A explicitly says subscriber-supplied, so A should not be treated as creator.

### Propagation relationships

#### C → B

`OBSERVED`, high confidence.

Basis: explicit forwarded-from metadata.

#### D → C

`OBSERVED`, high confidence.

Basis: article links to C and embeds C.

#### A ↔ B

Relationship exists at content level, but direct direction is not observed.

Reasonable phase-1 model:

- `A→B: INFERRED, medium`, because A is earlier and B repeats identical distinctive wording;
- strongest alternative: common upstream source supplying A and B.

A cautious student may rate `A→B` low/medium. Both can pass if reasoning is explicit.

### Strong phase-1 conclusion

> A is the earliest known publication in the phase-1 dataset at 08:12 and states the media was subscriber-supplied, so creator remains unknown. C is an observed forward of B, and D explicitly derives from C. B likely derives from A or from a common upstream source, but direct A→B transmission is not observed.

---

# Phase 2 expected reasoning

## New earliest known publication

E at 07:51.

The label `earliest known` must move from A to E.

## What must change

A student must not simply prepend E to the graph while leaving `A→B` unchanged.

The new E demonstrates that the distinctive wording existed before both A and B.

Therefore:

- chronology no longer makes A the strongest obvious upstream candidate for B;
- `A→B` confidence should decrease;
- common upstream / E-related path becomes stronger;
- direction E→A or E→B is still **not observed**, because E is a mirror and its own upstream is unknown.

## Correct graph logic

Observed edges remain:

- B → C in the sense `C forwarded from B`;
- C → D in the sense `D cites/embeds C`.

For early records:

```text
E earliest-known publication
 ?
 ├── A
 └── B
      ↓ observed forward
      C
      ↓ observed citation/embed
      D
```

The question marks are analytically meaningful.

## Strong phase-2 conclusion

> E is now the earliest known available publication at 07:51, but because E is itself a mirror with unknown upstream provenance, creator remains unknown. The discovery weakens the phase-1 inference that B copied A: both may derive from E or another common source. C→B and D→C remain directly observed provenance relationships. No evidence establishes a complete chain from creator to E/A/B.

---

# What the exercise tests

The main competency is not finding E.

It is whether the student:

1. preserves the original phase-1 reasoning;
2. notices that new evidence changes old confidence;
3. distinguishes earliest known publication from creator;
4. leaves unsupported edges unknown;
5. does not protect the initial hypothesis after it becomes weaker.

---

# Critical fail

A critical fail occurs if after phase 2 the student writes any equivalent of:

> «E is the original creator/source because it is earliest.»

or keeps:

> `A→B: proven/high confidence`

without new independent evidence.