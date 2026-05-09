# Design Agent Template

Русский | [English](README.en.md)

Текущая версия: `v0.2.0`

Стартовый Cursor workspace для дизайн-задач: UI research, Figma implementation, Lazyweb references, design review и переиспользуемые правила для агента.

## Быстрый старт

1. Склонируй или скачай эту папку для нового дизайн-проекта.
2. Получи бесплатный Lazyweb MCP token на https://www.lazyweb.com/mcp-install.
3. Скопируй `.cursor/mcp.example.json` в `.cursor/mcp.json`.
4. Вставь локальный Lazyweb bearer token в `.cursor/mcp.json`.
5. Перезагрузи Cursor, чтобы MCP servers и локальные slash skills появились в агенте.
6. Начинай работу с правилами и skills из `.cursor/`.

## Что внутри

- `.cursor/skills/lazyweb/SKILL.md`: локальный `/lazyweb` skill для UI references, screenshots, onboarding patterns, pricing pages и design comparisons.
- `.cursor/skills/manifest.json`: понятное описание skills для визуального каталога.
- `docs/skills/index.html`: bento-каталог skills с темной темой по умолчанию, RU/EN переключателем и preview-видео.
- `.cursor/rules/design-workflow.mdc`: постоянные правила для дизайн-задач.
- `.cursor/rules/security-and-secrets.mdc`: правила, чтобы токены и локальные конфиги не попали в Git.
- `.cursor/mcp.example.json`: безопасный пример Lazyweb MCP setup.
- `docs/`: инструкции по subagents, GitHub, каталогу skills и добавлению новых правил.

## Визуальный каталог skills

Открой `docs/skills/index.html`, чтобы увидеть skills как bento-карточки. Каталог стартует на русском и в темной теме, умеет переключаться на английский и использует официальное Lazyweb preview-видео.

## Локальные файлы и публичный шаблон

`.cursor/mcp.json` специально игнорируется, потому что там могут быть локальные bearer tokens. Храни настоящие credentials только у себя на машине. В репозиторий коммить только `.cursor/mcp.example.json`.

## Lazyweb token

Lazyweb выдает бесплатный no-billing MCP token через one-click installer:

```text
https://www.lazyweb.com/mcp-install
```

Агент может открыть эту страницу при старте проекта, вставить token в ignored local config и проверить `lazyweb_health` плюс `lazyweb_search`.

## README на двух языках

GitHub и GitLab не дают надежного автоматического переключателя языка README. Практичный вариант для RU-аудитории: держать `README.md` на русском, рядом вести `README.en.md` и давать языковые ссылки сверху.

## Безопасность перед публикацией

Перед push проверяй:

```bash
git status --ignored
git diff -- . ":(exclude).cursor/mcp.json"
```

Не коммить `.cursor/mcp.json`, `.env`, токены, приватные screenshots, customer data и приватные Figma exports.
