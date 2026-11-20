# tech-writer-ru

Скилл для русскоязычной технической документации в IT. Задаёт правила упрощённого технического языка по ASD-STE100, ГОСТ Р 58049-2017 (раздел 8.2, УТР) и ISO 24495-1.

## Состав

- `SKILL.md` — режимы, порядок работы, восемь правил, границы.
- `references/examples.md` — примеры «плохо → хорошо» и запрещённые синонимы.

## Установка

OpenCode ищет скиллы в `.opencode/skills` проекта и в глобальном каталоге: `~/.config/opencode/skills` или `~/.agents/skills`. Файл `SKILL.md` лежит в корне каталога скилла.

### Через npx skills

CLI `skills` устанавливает скилл из GitHub или локальной папки. Нужен Node.js 22.20 или новее.

В текущий проект:

```bash
npx skills add ishkulov/tech-writer-ru --skill tech-writer-ru -a opencode
```

Глобально, для всех проектов:

```bash
npx skills add ishkulov/tech-writer-ru --skill tech-writer-ru -a opencode -g
```

Флаг `-y` отключает вопросы. Скилл устанавливается в `.agents/skills/tech-writer-ru` проекта или в `~/.agents/skills/tech-writer-ru` при `-g`. OpenCode читает оба каталога.

Проверка, обновление и удаление:

```bash
npx skills list
npx skills update tech-writer-ru
npx skills remove tech-writer-ru
```

### Вручную

```bash
ln -s /path/to/tech-writer-ru ~/.config/opencode/skills/tech-writer-ru
```

## Использование

Скилл вызывается автоматически по описанию. Явный вызов:

```text
@tech-writer-ru отредактируй этот текст
```

## Настройка

1. Замените примеры в `references/examples.md` на примеры из вашего продукта.
2. Добавьте продуктовые термины в таблицу запрещённых слов.

## Лицензия

Проект распространяется по лицензии MIT. Подробности — в `LICENSE`.
