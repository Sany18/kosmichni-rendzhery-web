# Localization / Локалізація

Text data of the Space Rangers HD: A War Apart web port, in the game's own
language-file format. One file per top-level section.

Текстові дані веб-порту Space Rangers HD: A War Apart у форматі мовних файлів
самої гри. Один файл — один верхній розділ.

```
locales/
  en/   English (original game text) — base language of the port
  ru/   Russian (original game text)
  <code>/  your translation, same file names as en/
```

## Format / Формат

```
FormGameMenu ^{
    Exit=Exit (E)
    Help=Help (H)
    HelpFile=ManualEng.exe
    QExit=Do you want to quit the game?
    Resume=Continue (Esc)
}
```

- `Key=Text` — translate only the text after the first `=`; never change keys,
  section names or the `^{` / `~{` / `}` lines.
  Перекладайте лише текст після першого `=`; ключі, назви розділів і рядки
  `^{` / `~{` / `}` не змінюйте.
- Keep markup and placeholders as they are: `<br>`, `<clr>…<clrEnd>`,
  `<color=R,G,B>…</color>`, `<Player>`, `<Money>`, `<Number>` and other `<…>` tags.
  Розмітку й підстановки `<…>` лишайте як є.
- Some values are not text (file names like `HelpFile=ManualEng.exe`, numbers,
  image names) — keep them as in `en/`.
  Деякі значення — не текст (імена файлів, числа, картинки): лишайте як в `en/`.
- One line per value; line breaks inside a text are written as `<br>`.
  Одне значення — один рядок; перенос усередині тексту — `<br>`.
- Leading and trailing spaces of a value are ignored.
- Files are UTF-8.

## Adding a language / Нова мова

1. Copy `en/` to `locales/<code>/` (e.g. `uk/`) and translate the files.
2. The port is wired up for new languages by its maintainers (language list in
   the port's `lang.ts` and pack list in `tools/locales/lang_pack.py`); open a
   pull request with the translated files.

Not here yet: text quests and text drawn on images (menu buttons etc.) — they
will be added later with the rest of the port.
Поки що тут немає текстових квестів і написів на картинках (кнопки меню тощо) —
їх буде додано пізніше разом з рештою порту.

The original texts belong to their authors (Elemental Games, 1C, SNK-Games /
CHK-Games); this is a non-commercial fan project.
