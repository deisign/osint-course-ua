# elementalsouls / Claude-OSINT

**Repository:** `elementalsouls/Claude-OSINT`  
**Checked:** 2026-08-18  
**Audit status:** `PARTIAL-REVIEWED`  
**License:** code — MIT; textual/content material — CC BY 4.0 (`LICENSE-CONTENT`). Adaptation is possible with attribution.

## Executive decision

Useful donor, but **not** as a general OSINT curriculum and not for its offensive arsenal.

Its strongest value for our course is the architecture around professional reasoning and AI-assisted workflow:

- typed asset/entity graphs instead of loose notes;
- provenance on every discovered object;
- claim-specific confidence upgrades;
- separation of finding confidence from ownership/attribution confidence;
- human promotion gates for leads;
- connector/source resilience and explicit source-health tracking;
- stable output schemas for machine-assisted workflows;
- continuous baseline → re-run → diff logic;
- finding lifecycle and false-positive discipline;
- modular split between methodology and tool/reference layer;
- versioned AI skills + smoke-test prompts + expected behaviour;
- explicit hard boundaries and fail-closed behaviour.

The offensive probing, credential hunting, phishing, exploit-adjacent and evasion-oriented material is outside the core educational purpose of `osint-course-ua` and should not be imported.

---

## Reviewed

- `README.md`
- `docs/architecture.md`
- `skills/osint-methodology/SKILL.md` (methodological sections)
- `skills/org-attack-surface/SKILL.md` (attribution/ownership architecture)
- `skills/continuous-exposure-monitoring/SKILL.md` (monitoring/diff/lifecycle architecture)
- `tests/smoke-test-prompts.md`

Not reviewed as curriculum donor in detail:

- `skills/offensive-osint/SKILL.md` implementation arsenal;
- exploit-adjacent validators/probes;
- most vendor-specific offensive techniques.

---

# 1. What we take

## 1.1 Typed asset graph — `ADOPT + GENERALISE`

The repository insists that every discovery becomes a typed object rather than a free-floating string. Assets carry stable keys, sources, confidence, first/last seen and attributes.

For our course this should generalise beyond cyber assets:

```text
Person
Organisation
Unit
Account
Publication
DigitalObject
Location
Event
Document
Claim
Source
```

Every relationship should also be typed and sourced, for example:

```text
Person --AFFILIATED_WITH--> Unit
Publication --REPOSTS--> Publication
DigitalObject --DERIVED_FROM--> DigitalObject
Person --PRESENT_AT--> Location
Claim --SUPPORTED_BY--> DigitalObject
```

Each edge needs:

- source/evidence reference;
- observed vs inferred status;
- temporal validity;
- confidence;
- first_seen / last_seen where relevant.

**Targets:** M12, M13, M15, M18; future case-management/data model.

---

## 1.2 Separate existence confidence from attribution confidence — `ADOPT`

`org-attack-surface` keeps two axes separate:

1. Is the record/asset real and correctly observed?
2. Does it actually belong to the target organisation?

This is directly transferable to general OSINT.

Examples:

- a Telegram account definitely exists ≠ it belongs to Person A;
- a vehicle is definitely in the video ≠ it belongs to Unit X;
- a domain definitely exists ≠ Organisation Y controls it;
- a person is definitely identified ≠ they performed the alleged action.

This reinforces our attribution ladder and L12 Wrong Attribution.

**Targets:** M12, M13, M18, U02.

---

## 1.3 Discover-only / human promotion gate — `ADOPT`

One of the best patterns in the repository: newly associated assets are structurally treated as **leads**, not automatically promoted into the active workflow, even when their score looks strong.

For our course:

```text
candidate lead
→ attribution review
→ promote / reject / hold
→ only then enter substantive analysis
```

This prevents automation from converting correlation into fact.

Useful statuses:

- `candidate`
- `review_required`
- `promoted`
- `rejected`
- `unresolved`

**Targets:** M12, M13, M15, M18; AI-assisted workflow.

---

## 1.4 Confidence-upgrade workflow — `ADAPT`

The repository does not merely assign a confidence label; it specifies what additional evidence would move a claim upward.

We should adopt the pattern, not its cyber-specific thresholds.

Every important claim should support:

```text
current confidence
basis
missing evidence
upgrade path
possible downgrade trigger
```

This is stronger pedagogically than asking students only for `low/medium/high`.

**Targets:** M18, M19, all verification modules.

### Do not copy literally

The repository's simple `rule of three` is too mechanical for our purposes. Three dependent signals are still one evidentiary origin. Our version must prioritise **independence, relevance and claim-specific probative value**, not signal count.

---

## 1.5 Source/connector resilience — `ADOPT + EXPAND`

The methodology explicitly distinguishes:

```text
source failed / rate-limited
```

from:

```text
category returned no evidence
```

It recommends querying interchangeable sources as a union and recording per-source health.

This is extremely relevant to professional OSINT and monitoring.

For us each automated collection run should record:

- source/service;
- query parameters;
- run time;
- success / partial / failed;
- error/rate-limit state;
- result count;
- cache/freshness state;
- coverage caveat.

A broken Telegram indexer, search engine or archive must never silently become `no evidence exists`.

**Targets:** M06, M16, monitoring practicum.

---

## 1.6 Structured finding schema — `ADOPT + ADAPT`

The repository standardises findings with stable ID, module, typed asset key, category, confidence, evidence URL, timestamp, SHA-256 and references.

Our evidence-first equivalent should use separate records for object, claim and conclusion, but the machine-readable discipline is excellent.

Recommended general schema:

```yaml
ClaimRecord:
  id:
  claim:
  subject:
  predicate:
  object:
  status:
  confidence:
  evidence_supporting: []
  evidence_contradicting: []
  alternatives: []
  first_assessed:
  last_reviewed:
  reviewer:
  limitations: []
```

Object records remain separately preserved under Berkeley-style provenance rules.

**Targets:** M18, M20; future technical shell.

---

## 1.7 Continuous baseline → diff → lifecycle — `ADOPT + GENERALISE`

`continuous-exposure-monitoring` has several patterns useful well beyond cybersecurity:

- baseline snapshot;
- scheduled re-run;
- stable keys/fingerprints;
- new / removed / changed events;
- finding lifecycle;
- no repeated alert for already-triaged states;
- stored historical corpus for retroactive searches;
- delivery state separated from queue state (`queued ≠ delivered`).

For OSINT monitoring this maps cleanly to:

```text
baseline
→ collection run
→ normalize
→ diff
→ review
→ alert / suppress
→ lifecycle update
```

Possible finding lifecycle:

- `new`
- `under_review`
- `confirmed`
- `rejected_false_positive`
- `superseded`
- `resolved`
- `watching`

This is valuable both for the course and for our own monitoring architecture.

**Targets:** M16 advanced automation; future monitoring specialization/capstone.

---

## 1.8 AI-skill architecture: methodology vs arsenal — `ADOPT`

The project deliberately splits:

- **methodology / how to think**;
- **arsenal / what tool or technique to reach for**.

This is highly transferable to our course and to any AI assistant we build for OSINT.

An AI assistant should not have one giant prompt containing methodology, all tools and all case knowledge. Better separation:

```text
methodology layer
source/platform skill layer
case/domain layer
safety/legal layer
output/schema layer
```

This reduces tool-driven reasoning and makes updates/versioning easier.

**Targets:** safe-AI material; technical course shell; future OSINT assistant.

---

## 1.9 AI smoke tests and behavioural contracts — `ADOPT + EXPAND`

The repository ships a 56-prompt smoke-test suite with expected behaviour and explicit checks for:

- correct skill routing;
- no fabricated endpoints/sections;
- confidence/severity tagging;
- authorization boundaries;
- fail-closed behaviour.

This is one of the most useful donor ideas.

For our AI-assisted OSINT layer we should maintain regression prompts such as:

- `earliest publication = creator?` → must reject overclaim;
- `three reposts = three independent confirmations?` → must reject;
- `same name + same city = same person?` → must require more evidence;
- `archive has no capture = page did not exist?` → must reject;
- `unit was present = named soldier committed event?` → must reject;
- `source connector failed = no result exists?` → must distinguish failure from absence;
- `give legal guilt conclusion from OSINT package` → must preserve competence boundary.

Every course AI helper/version should be tested against these before release.

**Targets:** cross-cutting AI policy; instructor QA; future toolchain CI.

---

# 2. What we explicitly do NOT take

## 2.1 Offensive recon arsenal — `REJECT for core`

Most of the large tactical arsenal is oriented toward authorized red-team/bug-bounty work: active probing, credential exposure, phishing feasibility, attack-path construction and exploit-adjacent validation.

That is a different course. It should not leak into the core OSINT curriculum merely because the repository calls itself OSINT.

## 2.2 Cyber severity rubric — `REJECT`

`CRITICAL/HIGH/MEDIUM/...` thresholds are engagement-specific and sometimes deliberately aggressive. They are not transferable to factual confidence, evidentiary strength or legal significance.

Keep separate axes:

```text
confidence
source quality
evidence strength
harm/risk
priority
legal significance (only where professionally assessed)
```

## 2.3 Self-evaluation claims — `DO NOT TREAT AS VALIDATION`

The repository reports 56/56 PASS on its own smoke tests. Useful engineering evidence, but it is a **self-grade**, not independent validation.

What we take is the regression-testing pattern, not the marketing claim.

## 2.4 Engagement-grade evidence ≠ Berkeley-grade evidence

Its generic finding schema includes truncated raw captures and engagement reporting discipline. For our high-stakes documentation path, this is insufficient as the preservation model.

Berkeley/Mnemonic/WITNESS remain authoritative for preservation, source context, full original/reference copies and transfer packages.

---

# 3. Curriculum impact

High-value adaptations:

### M13 Organisations, Domains, Documents & Accountability Systems

Add:

- organisation-first vs domain-first mapping;
- ownership/association evidence classes;
- candidate lead vs attributed asset;
- namesake and shared-infrastructure false attribution;
- explicit ownership/relationship assessment.

### M15 Timelines & Network Analysis

Add:

- typed nodes and typed edges;
- stable IDs;
- `sources[]` on every substantive edge;
- first_seen / last_seen;
- temporal edge validity;
- machine-readable graph export.

### M16 APIs, Scraping, Regex & Text-as-Data

Add:

- connector health;
- category union/fallback strategy;
- `failed source ≠ empty evidence`;
- run IDs and collection manifests;
- baseline/diff patterns;
- machine-checkable outputs;
- optional AI-agent orchestration.

### M18 Investigative Analysis

Add:

- explicit confidence-upgrade path;
- separation of existence/identity/ownership/action confidence;
- structural lead-promotion gate.

### M19 Peer Review

Add AI/system regression tests as a form of methodological QA.

### M20 Evidence/Research Package

Add machine-readable claim/finding export alongside the human analytical package.

---

# 4. Possible new cross-cutting block: AI-assisted OSINT

Do **not** make "prompt engineering" a standalone toy module.

Instead teach a cross-cutting professional rule:

> AI may assist collection planning, search expansion, extraction, normalization, comparison, contradiction-finding and drafting, but every factual assertion must remain traceable to non-AI evidence.

Suggested topics:

- modular agent skills;
- grounded context vs model memory;
- source/tool provenance;
- hallucination regression tests;
- structured outputs;
- human promotion gates;
- safe handling of sensitive material;
- deterministic checks where possible;
- versioning/changelog of prompts/skills;
- model/tool freshness;
- AI never counts as independent corroboration.

---

# 5. Overall assessment

**Value for general OSINT methodology:** medium.  
**Value for cyber reconnaissance specialization:** high, but outside current core.  
**Value for OSINT data architecture / monitoring:** very high.  
**Value for AI-assisted OSINT engineering:** very high.  
**Value for evidence preservation:** secondary; Berkeley remains primary.

The repository is therefore worth keeping as a **systems/AI/automation donor**, not as a primary OSINT authority.