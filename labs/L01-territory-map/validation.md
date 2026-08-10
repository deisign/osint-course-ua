# L01 — Internal validation record

**Дата:** 2026-08-10  
**Статус:** `DRAFT / internally testable`

## Structural checks

- `seeds.csv` parses as CSV;
- 12 unique seed records;
- required columns present;
- epistemic status is mixed by design: 9 `given`, 3 `inferred`;
- scenario explicitly marks all entities and events as synthetic;
- task, rubric and instructor solution use the same research question and scope;
- no task requires identification of a real private person.

## Pedagogical checks

The lab contains deliberate traps:

1. treating co-appearance as a formal relationship;
2. treating budget allocation as actual spending;
3. treating procurement title as proof of final use;
4. treating official percentage as verified outcome without denominator/methodology;
5. turning an `inferred` source/system relationship into a fact;
6. drifting from institutional mapping into unnecessary personal-data collection.

The instructor solution preserves unresolved nodes and relationships instead of completing the system artificially.

## Expected learning signal

A strong student should produce **more structured uncertainty**, not merely more nodes.

Success is demonstrated when the student can state:

- what is known;
- what is inferred;
- what remains unknown;
- where a relevant trace would likely appear;
- what type of evidence would change a relationship status.

## Remaining gate before `pilot-ready`

- independent human run without oral hints;
- measured completion time;
- usability review of tables / deliverables;
- instructor grading test on at least one real student submission.
