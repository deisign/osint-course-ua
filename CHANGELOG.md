# Changelog

## 2026-08-10 — M06 golden-module content build

- M06 promoted from curriculum skeleton/draft outline to `CONTENT-COMPLETE DRAFT` and designated golden-module candidate;
- added 9 substantive authored lessons:
  - why provenance matters;
  - source roles;
  - propagation models;
  - search strategy;
  - Telegram-specific provenance;
  - web/archives;
  - media provenance;
  - circular reporting;
  - confidence & limitations;
- added 12-case synthetic micro-casebook;
- added staged guided exercise with phase-1 model, later earlier-source discovery, and instructor solution;
- added 20-question knowledge check + answer key;
- added operational reference sheet;
- added 20 common errors with remediation guidance;
- added source dossier and freshness policy;
- added full instructor guide with learning sequence, provisional timing, diagnostic, grading philosophy, debrief and pilot protocol;
- official Telegram FAQ/API/TDLib checked 2026-08-10 for forward/edit/copy/delete provenance-relevant behaviour;
- official Internet Archive / Wayback Machine help checked 2026-08-10 for capture/save/coverage limitations;
- Bellingcat verification guide included as practitioner donor only;
- M06 README rebuilt as student/instructor navigation entrypoint;
- M06 still requires independent human run before `PILOT-READY`.

## 2026-08-10 — L01 + L12 + mini-pilot v0.1

- створено controlled synthetic lab `L01 Territory Map`;
- L01 містить task, synthetic scenario, 12 seed records, rubric, instructor solution, validation record і submission template;
- L01 формалізує `given / inferred / unknown`, source ecosystem, collection requirements, gaps, competing explanations і harm note;
- створено controlled synthetic lab `L12 Wrong Attribution`;
- L12 містить 2 synthetic candidate profiles, 15 observations, 10 claims, rubric, instructor solution, validation record і submission templates;
- L12 формалізує attribution ladder: `account control → identity → affiliation → physical presence → specific action / responsibility`;
- dataset L12 навмисно не містить прихованої позитивної атрибуції: P-A і P-B залишаються недоведеними кандидатами;
- зафіксовано правило `unknown location ≠ evidence of presence` і `upload time ≠ capture time`;
- внутрішні CSV checks пройдено: unique IDs / required columns / intended epistemic-status distributions → OK;
- створено `pilot/mini-pilot-v0.1.md` для послідовності L01 → L03 → L12;
- mini-pilot protocol вимірює completion time, clarification questions, rubric score, critical fails, confidence calibration і reviewer disagreement;
- усі три лабораторні залишаються `DRAFT / internally testable` до незалежного людського проходу.

## 2026-08-10 — M05/M06 draft modules

- додано `modules/M05-collection-preservation/README.md`;
- додано `modules/M06-source-tracing/README.md`;
- M05 формалізує preliminary assessment, collection, preservation, hash limits, reference/working copies і transformation logging;
- M06 первинно формалізував creator/uploader/publisher distinction, earliest-known-source logic, observed vs inferred propagation, circular reporting, edit/deletion history і provenance chains;
- обидва модулі використовують L03 як demonstration/assessment case.

## 2026-08-10 — methodology core + first working lab

- додано `docs/02-competency-map.md`;
- додано `docs/03-terminology.md`;
- проведено core-аудит Berkeley Protocol і додано `research/donors/berkeley-protocol.md`;
- оновлено source registry: Berkeley Protocol → `core-reviewed`; додано Berkeley imagery guide (2024) і Open-Source Practitioner’s Guide to the Murad Code (2025) у чергу;
- додано `standards/osint-investigation-standard-v0.1.md`;
- у стандарті формалізовано lifecycle `discovery → preliminary assessment → collection → preservation → verification → analysis → peer review → handoff/reporting`;
- verification стандартизовано як `SOURCE + ITEM + CONTENT`;
- додано attribution ladder і qualitative confidence scale;
- створено core templates для planning, digital landscape, threat/harm assessment, hypotheses, digital object provenance, collection logging, verification і peer review;
- Curriculum Blueprint оновлено до v0.2 з інтеграцією Berkeley;
- створено controlled synthetic lab `L03 Telegram Source Tracing`;
- L03 містить task, dataset, synthetic media, rubric, instructor solution і validation record;
- машинні перевірки L03 пройдено: CSV/chronology/forward logic → OK; expected SHA-256 values → OK;
- статус L03: `DRAFT / internally testable`, independent human run required before `pilot-ready`;
- Bradshaw donor audit розширено до `PARTIAL-REVIEWED` після file-level review network analysis, Kumu data model, OpenRefine cleaning, Python/scraping, company accounts і storytelling;
- network curriculum зафіксовано як entities + sourced relationships + observed/inferred + temporal validity + confidence, незалежно від конкретного graph UI.

## 2026-08-10 — curriculum architecture v0.1

- додано `docs/01-graduate-profile.md`;
- визначено 17 базових доменів компетентностей і 5 компетентностей спеціалізації «Україна — Росія — війна»;
- додано критичні компетентності та мінімальний стандарт випускної роботи;
- додано `curriculum/blueprint.md`;
- сформовано 20 core-модулів і 5 модулів спеціалізації;
- закладено 16 лабораторних, 3 наскрізні кейси, MVP/pilot curriculum і dependency map;
- інтегровано початкові висновки з Paul Bradshaw / MED7369: systems thinking, territory mapping, competing hypotheses, network analysis, statistics + cognitive bias, text-as-data, data cleaning і project-driven learning;
- зафіксовано Definition of Done для переходу модуля у статус `pilot-ready`.

## 2026-08-10 — bootstrap

- створено структуру репозиторію;
- додано `Концепцію курсу v0.1`;
- додано research layer і donor workflow;
- додано реєстр зовнішніх джерел;
- додано початковий аудит `paulbradshaw/MED7369-Specialist-Investigative-Journalism`;
- зафіксовано наступні артефакти: graduate profile, curriculum blueprint, terminology, investigation standard, Telegram lab.