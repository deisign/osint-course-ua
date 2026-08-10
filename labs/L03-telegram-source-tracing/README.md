# L03 — Відновлення та документування першоджерела Telegram-публікації

**Статус:** `DRAFT / internally testable`  
**Тип:** Controlled verification / synthetic case  
**Модулі:** M05 Provenance & Preservation + M06 Search Strategy & Source Tracing  
**Компетентності:** C04, C05, C13, C17  
**Приблизний час:** 90–150 хвилин

## Мета

Навчити студента не просто знайти «найстаріший пост», а:

1. відрізнити earliest known publication від original creator;
2. відновити observed та inferred propagation links;
3. зафіксувати provenance;
4. оцінити наслідки редагування й видалення повідомлення;
5. не перетворити часову послідовність на необґрунтовану причинність;
6. сформулювати claim із належним confidence;
7. оформити матеріал так, щоб інший дослідник міг повторити висновок.

## Чому кейс синтетичний

У першому пілоті ми не хочемо, щоб:

- live Telegram content зник під час лабораторної;
- різні студенти отримували різні набори даних;
- випадкова реальна людина або канал ставали навчальною мішенню;
- правильність роботи залежала від стороннього сервісу.

Усі канали, повідомлення й URL у пакеті вигадані. Структура задачі моделює реальну проблему source tracing.

## Файли

- `task.md` — завдання;
- `input/case-manifest.md` — опис отриманого пакета;
- `input/messages.csv` — нормалізовані snapshots повідомлень;
- `input/media/clip-A.svg` — synthetic media object;
- `input/media/clip-A-crop.svg` — derived screenshot/crop;
- `rubric.md` — критерії оцінювання;
- `instructor-solution/solution.md` — еталонна логіка для викладача.

## Required templates

Студент використовує:

- `templates/digital-object-card.md`;
- `templates/collection-log.csv`;
- `templates/verification-sheet.md`;
- за потреби `templates/hypothesis-matrix.md`.

## Pass condition

Студент може не вгадати кожен inferred edge, але MUST:

- правильно визначити earliest known publication у наданому пакеті;
- НЕ назвати її доведеним original creator;
- правильно відрізнити explicit forward від inferred manual copy;
- врахувати edit/deletion history;
- сформулювати обмежений висновок і limitations;
- залишити відтворюваний evidence trail.

---

**Standard:** `standards/osint-investigation-standard-v0.1.md`
