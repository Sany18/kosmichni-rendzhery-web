# Localization / Локалізація

Compare languages by key, search, copy a key or suggest an edit:
порівняння мов за ключами, пошук, копіювання ключа чи пропозиція правки —
https://sany18.github.io/kosmichni-rendzhery-web/locales/

Text data of the Космічні Ренджери HD: A War Apart web port. One JSON file per
section of the game's language data.

Текстові дані веб-порту Космічні Ренджери HD: A War Apart. Один JSON-файл — один
розділ мовних даних гри.

```
locales/
  en/   English (original game text) — base language of the port
  ru/   Russian (original game text)
  uk/   Ukrainian — complete, manual review in progress / українська — перекладено, триває ручне уточнення
  <code>/  your translation, same file names as en/
  quests/<code>/<QUEST>.json   text quests (one file per quest; keys = parts of the quest) / текстові квести
  uk-glossary.md   Ukrainian terminology / глосарій українських термінів
```

Example / приклад — `en/FormGameMenu.json`:

```json
{
  "Exit": "Exit (E)",
  "Help": "Help (H)",
  "HelpFile": "ManualEng.exe",
  "QExit": "Do you want to quit the game?",
  "Resume": "Continue (Esc)"
}
```

- Translate the values, never the keys. / Перекладайте значення, ключі не змінюйте.
- Keep markup and placeholders as they are: `<br>`, `<clr>…<clrEnd>`,
  `<color=R,G,B>…</color>`, `<Player>`, `<Money>`, `<Number>` and other `<…>` tags.
  Розмітку й підстановки `<…>` лишайте як є.
- Only texts are here: file names, numbers and resource references are kept out of this repository, there is
  nothing else to translate. / Тут лише тексти: імена файлів, числа й посилання на ресурси в цьому
  репозиторії не лежать, більше нічого перекладати не треба.
- Arrays keep their length and order. / Масиви — тієї ж довжини й у тому ж порядку.

## Adding a language / Нова мова

1. Copy `en/` to `locales/<code>/` (e.g. `uk/`) and translate the files.
2. Open a pull request. The port's maintainers connect the new language to the game.

Not here yet: text quests and text drawn on images (menu buttons etc.) — they
will be added later with the rest of the port.
Поки що тут немає текстових квестів і написів на картинках (кнопки меню тощо) —
їх буде додано пізніше разом з рештою порту.

The original texts belong to their authors (Elemental Games, 1C, SNK-Games /
CHK-Games); this is a non-commercial fan project.

**Text quests / Текстові квести.** In many original quests the `en` file is Russian or partly Russian: the game
ships no English version of them. Translate `uk` from `ru` there. /
У багатьох оригінальних квестах `en` російською чи частково російською: англійської версії в грі немає.
Там перекладайте `uk` з `ru`.
