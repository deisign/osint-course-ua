# M06 Guided Exercise — Instructor solution

## Phase 1 expected reasoning

### Earliest known publication

A at 08:12 based on the platform timestamp in the phase-1 dataset.

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

## New earlier web object discovered through archive

E is a web-mirror page whose own page timestamp claims **07:51**.

The archive capture establishes that this state of E existed **by 08:02**.

These are two separate time claims and must not be collapsed.

Because the archive proves E existed by 08:02, E is now the earliest **documented available object in the exercise** before A at 08:12.

A careful student may phrase this as:

> «E is documented by archive capture as existing by 08:02; the page itself claims publication at 07:51.»

They should not say:

> «The archive proves E was published at 07:51.»

## What must change

A student must not simply prepend E to the graph while leaving `A→B` unchanged.

The newly discovered E shows that the distinctive wording was publicly present no later than the 08:02 archive capture, before A and B.

Therefore:

- chronology no longer makes A the strongest obvious upstream candidate for B;
- `A→B` confidence should decrease;
- common upstream / E-related path becomes stronger;
- direction E→A or E→B is still **not observed**, because E’s upstream provenance is unknown;
- the page’s claimed 07:51 publication time remains distinct from the archive’s 08:02 capture proof.

## Correct graph logic

Observed edges remain:

- B → C in the sense `C forwarded from B`;
- C → D in the sense `D cites/embeds C`.

For early records:

```text
E — documented available by 08:02
 ?
 ├── A 08:12
 └── B 08:19
      ↓ observed forward
      C
      ↓ observed citation/embed
      D
```

The question marks are analytically meaningful.

## Strong phase-2 conclusion

> E is the earliest newly documented available object in the exercise: an archive capture proves the mirror page existed by 08:02, while the page itself claims a 07:51 publication time. E’s upstream provenance remains unknown, so creator remains unknown. The discovery weakens the phase-1 inference that B copied A: both may derive from E or another common source. C→B and D→C remain directly observed provenance relationships. No evidence establishes a complete chain from creator to E/A/B.

---

# What the exercise tests

The main competency is not finding E.

It is whether the student:

1. preserves the original phase-1 reasoning;
2. notices that new evidence changes old confidence;
3. distinguishes earliest documented availability from creator;
4. distinguishes page publication claim from archive capture time;
5. leaves unsupported edges unknown;
6. does not protect the initial hypothesis after it becomes weaker.

---

# Critical fail

A critical fail occurs if after phase 2 the student writes any equivalent of:

> «E is the original creator/source because it is earliest.»

or:

> «The archive proves E was published at 07:51.»

or keeps:

> `A→B: proven/high confidence`

without new independent evidence.