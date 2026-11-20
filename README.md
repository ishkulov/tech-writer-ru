# tech-writer-ru

Скилл для русскоязычных технических текстов в IT. Задаёт стиль, термины, жанры, локализацию и доступность.

## Состав

- `SKILL.md` — режимы, порядок работы и конституция стиля.
- `references/terminology.md` — универсальные термины, UI-действия и внутренний сленг.
- `references/glossary-template.md` — шаблон глоссария продукта.
- `references/localization.md` — перевод и локализация.
- `references/genres.md` — инструкции, UI-тексты, ошибки, релиз-ноты, API/CLI и README.
- `references/accessibility.md` — доступность и инклюзивность.
- `references/style.md` — примеры «Плохо → Хорошо».
- `references/checklist.md` — проверка перед выдачей.
- `references/lint.md` — быстрая проверка запрещённых синонимов.

## Установка

OpenCode ищет скиллы в `.opencode/skills` проекта и в глобальном каталоге: `~/.config/opencode/skills` или `~/.agents/skills`. Файл `SKILL.md` лежит в корне каталога скилла.

Для проекта:

```bash
mkdir -p /path/to/project/.opencode/skills
cp -r /path/to/tech-writer-ru /path/to/project/.opencode/skills/
```

Глобально:

```bash
mkdir -p ~/.config/opencode/skills
cp -r /path/to/tech-writer-ru ~/.config/opencode/skills/
```

Или симлинк вместо копирования:

```bash
ln -s /path/to/tech-writer-ru ~/.config/opencode/skills/tech-writer-ru
```

## Использование

Скилл вызывается автоматически по описанию. Явный вызов:

```text
@tech-writer-ru отредактируй этот текст
```

## Настройка

1. Скопируйте `references/glossary-template.md` и заполните его продуктовыми терминами.
2. Проверьте универсальные правила в `references/terminology.md`.
3. Обновите примеры в `references/style.md`.
4. Пройдите `references/checklist.md`.
5. Настройте проверки по `references/lint.md`.

## Лицензия

Проект распространяется по лицензии MIT. Подробности — в `LICENSE`.
