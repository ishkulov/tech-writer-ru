# tech-writer-ru

Скилл для русскоязычных технических текстов в IT. Задаёт стиль, термины и оформление.

## Состав

- `SKILL.md` — режимы, порядок работы и конституция стиля.
- `references/style.md` — примеры «Плохо → Хорошо».
- `references/terminology.md` — термины, продукты, код и лексика.
- `references/checklist.md` — проверка перед выдачей.

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

Замените таблицу в `references/terminology.md` на глоссарий продукта и обновите примеры в `references/style.md`.
