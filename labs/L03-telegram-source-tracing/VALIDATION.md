# L03 Validation Record

**Lab:** `L03-telegram-source-tracing`  
**Date:** 2026-08-10  
**Current status:** `DRAFT / internally testable`  
**Pilot-ready:** NO — independent human run still required.

## 1. Automated checks completed

### Dataset parsing

`input/messages.csv` was parsed successfully as structured CSV.

Checks passed:

- 8 records present;
- timestamps parse as timezone-aware ISO-8601 values;
- earliest record is `R1`;
- R4 explicit `forwarded_from = @front_watch`;
- R5 explicit `forwarded_from = @news_region`;
- R2a, R2b and R7 share message ID `4112`;
- R2a and R3 text is exactly identical, supporting an inference test without creating an explicit-forward fact.

Result:

```text
L03 dataset checks: OK
```

## 2. Media integrity check

Expected repository SHA-256 values:

```text
clip-A.svg
584d05ec2b575272d38d86c6ebe1cfc894e5c174bd383c03c7ab7a5b0a06b208

clip-A-crop.svg
fbc223ae7765d0272ee4a8c148d2e1f95d6243d6347c40c8fe83799d0181d7f4
```

Result:

```text
L03 expected SHA-256 values: OK
```

## 3. Internal logic checks

The synthetic case contains the intended reasoning traps:

- an earlier media publication than the viral alleged first source;
- earliest known publisher explicitly disclaims creator status (`subscriber-supplied`);
- identical later text without explicit forward metadata;
- explicit forward relationships later in the chain;
- material caption edit on the same message ID;
- later deletion event;
- derived/cropped media representation;
- repeated contextual claim that is not independent corroboration.

## 4. Gates not yet completed

Before changing status to `pilot-ready`, an independent tester MUST:

1. receive only `README.md`, `task.md`, `input/` and allowed templates;
2. complete the lab without oral hints;
3. record actual completion time;
4. identify ambiguous wording or missing fields;
5. compare submission against `rubric.md`;
6. confirm that `instructor-solution/solution.md` is sufficient to grade the work;
7. report any point where instructor explanation was needed.

Any required oral explanation is treated as a **course bug** and should be fixed in the written materials.

## 5. Status decision

`DRAFT / internally testable` retained.

Reason: technical/data consistency is verified, but independent human usability has not yet been demonstrated.
