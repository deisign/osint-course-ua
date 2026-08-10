# L01 — Instructor solution

Це **не єдина правильна карта**. Еталон задає мінімальну повноту, правильний епістемічний статус і типи collection requirements, які очікуються від сильної роботи.

## 1. Межі системи

### У межах дослідження

- регіональні й муніципальні рішення про виплати;
- адміністративна та інформаційна інфраструктура набору;
- публічні закупівлі й рекламні контракти;
- офіційні й напівофіційні комунікаційні канали;
- освітні, соціальні та ветеранські інституції як потенційні точки публічного залучення;
- методика обліку й звітності результатів;
- контрольні / аудитні системи.

### Поза межами без додаткового мандата

- встановлення конкретних кандидатів на службу;
- оцінка законності індивідуальних дій;
- непублічні військові процедури;
- HUMINT / приховані контакти;
- збір зайвих персональних даних.

## 2. Мінімальний territory map

Сильна карта має містити щонайменше такі групи вузлів.

### A. Policy / command layer

- Government of Northern Krai — `given`;
- профільний регіональний орган, відповідальний за соціальну / кадрову / військово-адміністративну координацію — `unknown/inferred` до виявлення нормативного акта;
- municipal administrations — `given`.

### B. Public-facing recruitment layer

- contract consultation points — `given`;
- employment centres — `given`;
- можливий окремий recruitment operator / military-facing institution — `unknown`.

### C. Money / procurement layer

- regional budget system — `inferred`;
- municipal budgets — `inferred`;
- procurement portal — `inferred`;
- advertising contractors — `given as class`, конкретні юридичні особи — `unknown`;
- treasury / execution reporting — `inferred`.

### D. Communication layer

- regional government press service;
- municipal media;
- regional media;
- social channels of administrations;
- paid advertising inventory;
- contractors producing or placing creative assets.

Статус конкретних зв’язків між бюджетом, медіа й contractors має бути `unknown` до документального підтвердження.

### E. Social / institutional layer

- Northern Veterans Association — `given`;
- colleges — `given as participating institutions`;
- employment centres — `given`;
- houses of culture / venues — `given from scenario`;
- enterprises mentioned in meetings — `given as class`, конкретні підприємства — `unknown`.

### F. Measurement / accountability layer

- monthly plan-performance reports — `given`;
- counting methodology — `unknown`;
- audit/control body — `inferred`;
- budget execution reports — `inferred`;
- procurement oversight / complaints / audit trail — `inferred`;
- external statistics that could act as denominator/check — `unknown but desirable`.

## 3. Source ecosystem — examples

| Source class | Expected artefact | Can support | Cannot establish alone |
|---|---|---|---|
| regional legal portal | decree / resolution | existence and formal terms of payment | actual number of recipients |
| budget portal | appropriations / amendments | planned financing | actual execution unless execution data present |
| treasury/execution report | actual spending | expenditure under identified code | purpose if code is ambiguous |
| procurement portal | contract, supplier, amount | procurement relationship | final use or impact |
| municipal sites | local resolutions, event reports | local implementation / messaging | complete regional picture |
| college sites | event pages / photos | event occurred / institution participated | recruitment outcome |
| veteran organisation | event report | organisation publicly participated | formal authority or financing |
| official performance report | claimed output | official claim and methodology if stated | independent verification of count |
| audit/control body | audit report | reviewed findings / deficiencies | everything outside audit scope |
| media archive | campaign narrative / chronology | what was publicly communicated | underlying administrative truth |

## 4. Strong collection requirements — examples

1. Identify the formal legal act establishing `Служба поруч` and list responsible institutions.
2. Determine whether regional one-time payments have a distinct budget programme/code.
3. Compare planned appropriations with actual execution for that code by month/quarter.
4. Identify municipalities that adopted additional payments and dates/amounts of amendments.
5. Identify procurement records whose subject explicitly concerns campaign advertising or recruitment information.
6. For each identified contractor, determine contract value, contracting authority, period and deliverables.
7. Determine whether monthly recruitment figures come from one data owner or are compiled from municipalities.
8. Find methodology/definitions used for `contract signed`, `candidate`, `referred`, and `plan completed`.
9. Compare figures published by regional government, municipalities and recruitment-facing institutions for the same period.
10. Determine whether employment centres have formal agreements/instructions to host consultation points.
11. Determine whether colleges received formal guidance, funding or only invitations to host informational events.
12. Check whether the regional audit/control body reviewed programme expenditure or related procurement.
13. Determine whether media placements were editorial, state-funded informational contracts, or commercial advertising.
14. Identify any public denominator needed to interpret `plan completion` rather than relying on percentages alone.

## 5. Competing explanations — expected examples

### Observation: advertising volume increased when reported recruitment increased

Possible explanations:

- advertising contributed to recruitment;
- recruitment increased for unrelated economic/administrative reasons;
- both were responses to a third factor such as increased regional target or increased payments;
- reporting intensity increased without a proportional change in actual recruitment.

### Observation: veterans association appears repeatedly at official events

Possible explanations:

- formal programme partner;
- informal invited participant;
- media-friendly symbolic presence;
- independent organisation supporting the same policy without a formal administrative role.

### Observation: a private contractor appears in procurement records

Possible explanations:

- contractor produced recruitment advertising;
- contract covered a broader information campaign;
- contractor performed unrelated services under a similarly worded procurement item;
- subcontracting or actual delivery differed from contract title.

## 6. Expected gaps

A strong student should leave unresolved at least some of these questions:

- who owns the master dataset for recruitment outcomes;
- how duplicates / failed candidates / transfers are counted;
- whether all relevant spending is visible under one programme;
- whether municipal and regional payments overlap;
- whether media coverage is paid, editorial or mixed;
- whether institutional participation implies formal responsibility.

## 7. Harm note — expected reasoning

The lab does not require names of candidates, students, rank-and-file employees or private individuals. Strong work should prefer institutional/documentary sources and use data minimisation.

Images from colleges or events may contain minors or uninvolved people; identification is unnecessary for the research question.

## 8. Model conclusion

> The available seed information is sufficient to identify a multi-layer system of policy, municipal implementation, public communication, social institutions, procurement and performance reporting. It is **not** sufficient to establish the formal role of every actor or a causal chain between spending, messaging and recruitment results. The next stage should prioritise legal acts, budget/execution data, procurement records and the methodology behind performance reporting before individual organisations are assigned a stronger role in the system.

## 9. Instructor red flags

Reject or return for revision if the submission:

- draws direct arrows between all co-mentioned actors without source status;
- equates participation in an event with organisational responsibility;
- treats budget allocation as proof of actual spending;
- treats procurement title as proof of final use;
- treats official recruitment percentage as verified outcome without denominator/methodology;
- starts identifying private individuals even though the research question does not require it.
