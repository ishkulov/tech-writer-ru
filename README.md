# tech-writer-ru

Навык помогает писать, редактировать и проверять техническую документацию на русском языке в IT. Он также переводит тексты с других языков. Навык опирается на принципы ASD-STE100, ГОСТ Р 58049-2017 (раздел 8.2, УТР) и ISO 24495-1. УТР расшифровывается как «упрощённый технический русский язык».

## Состав

- `SKILL.md` — режимы, порядок работы и восемь правил.
- `references/examples.md` — примеры «плохо → хорошо» и таблица запрещённых слов.

## Установка

OpenCode V2 ищет навыки в этих каталогах:

| Область | Каталоги |
| --- | --- |
| Проект | `.opencode/skills`, `.agents/skills`, `.claude/skills` |
| Глобально | `~/.config/opencode/skills`, `~/.agents/skills`, `~/.claude/skills` |

### Через npx skills

Для установки нужен Node.js 22.20 или новее.

В текущий проект:

```bash
npx skills add ishkulov/tech-writer-ru --skill tech-writer-ru -a opencode
```

Глобально, для всех проектов:

```bash
npx skills add ishkulov/tech-writer-ru --skill tech-writer-ru -a opencode -g
```

Обновление и удаление:

| Задача | Команда |
| --- | --- |
| Обновить навык | `npx skills update tech-writer-ru` |
| Удалить навык | `npx skills remove tech-writer-ru` |

### Установка вручную

1. Если каталога `~/.agents/skills` нет, создайте его:

   ```bash
   mkdir -p ~/.agents/skills
   ```

2. Создайте символьную ссылку:

   ```bash
   ln -s /path/to/tech-writer-ru ~/.agents/skills/tech-writer-ru
   ```

3. Убедитесь, что файл `~/.agents/skills/tech-writer-ru/SKILL.md` доступен.

Ссылка в глобальном каталоге делает навык доступным во всех проектах. Для проекта создайте такую же ссылку в `.opencode/skills` или `.agents/skills` проекта.

В Windows скопируйте каталог `tech-writer-ru` в `%USERPROFILE%\.agents\skills\tech-writer-ru`.

## Использование

Если задача совпадает с описанием из `SKILL.md`, OpenCode вызывает навык автоматически. Вызовите навык вручную:

```text
@tech-writer-ru отредактируй этот текст
```

Примеры для проверки и перевода:

```text
@tech-writer-ru проверь этот текст
@tech-writer-ru переведи этот текст с английского на русский
```

## Настройка

**ВНИМАНИЕ:** `npx skills update` может заменить файлы установленного навыка. Храните изменения в отдельной копии репозитория.

1. Склонируйте репозиторий или сделайте форк.
2. Замените примеры в `references/examples.md` на примеры из вашего продукта.
3. Добавьте термины продукта в таблицу запрещённых слов в `references/examples.md`.
4. Установите навык из локального каталога:

   ```bash
   npx skills add ./tech-writer-ru --skill tech-writer-ru -a opencode
   ```

   Замените `./tech-writer-ru` на путь к вашей копии.

## Лицензия

Проект распространяется по лицензии MIT. Подробности — в `LICENSE`.
