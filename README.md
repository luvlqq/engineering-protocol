# Engineering Protocol

[English](#english) · [Русский](#русский)

## English

A skill for Claude Code and Codex that scales the engineering workflow to the risk of the task. It covers implementation, review, and verification, from small fixes to production changes.

### Install

Run this command to install the skill for both agents across your projects. The [skills CLI](https://github.com/vercel-labs/skills#install-a-skill) requires Node.js 22.20 or later.

```sh
npx skills add luvlqq/engineering-protocol --skill engineering-protocol -g -a claude-code -a codex
```

For a project-only install, run the command from the project directory and omit `-g`. To install for one agent, keep only its `-a` flag.

### Use

Type the appropriate invocation in your agent and follow it with the task.

| Agent | Example |
| --- | --- |
| Claude Code | `/engineering-protocol Review this release plan and identify stop conditions.` |
| Codex | `$engineering-protocol Review this release plan and identify stop conditions.` |

### Workflow

| Level | Typical task | Workflow |
| --- | --- | --- |
| L0 · Trivial | Typo, documentation, or mechanical edit | Inspect → Change → Verify |
| L1 · Standard | Bug fix or isolated feature | Research → Implement → Test → Review |
| L2 · Complex | Refactor or cross-service change | Research → Plan → Review plan → Implement → Independent review → Verify |
| L3 · Critical | Production, security-sensitive, or irreversible change | Research → Assess risk → Get approval → Back up → Plan → Execute → Verify → Recover if needed |

[SKILL.md](SKILL.md) defines the core workflow and tells the agent which references to load for the task. The eight references cover [development](references/development.md), [verification](references/verification.md), [production](references/production.md), [security](references/security.md), [Git](references/git.md), [CI/CD](references/ci-cd.md), the [local environment](references/local-environment.md), and [documentation](references/documentation.md).

## Русский

Скилл для Claude Code и Codex, который подбирает процесс работы по риску задачи. Он охватывает реализацию, ревью и проверку результата для задач от небольших правок до изменений в проде.

### Установка

Эта команда установит скилл для обоих агентов во всех твоих проектах. Для [CLI skills](https://github.com/vercel-labs/skills#install-a-skill) нужен Node.js 22.20 или новее.

```sh
npx skills add luvlqq/engineering-protocol --skill engineering-protocol -g -a claude-code -a codex
```

Чтобы установить скилл только для одного проекта, выполни команду из его каталога без `-g`. Для одного агента оставь только его флаг `-a`.

### Вызов

Укажи имя скилла в запросе к агенту и добавь задачу.

| Агент | Пример |
| --- | --- |
| Claude Code | `/engineering-protocol Проверь план релиза и укажи, когда нужно остановить выкатку.` |
| Codex | `$engineering-protocol Проверь план релиза и укажи, когда нужно остановить выкатку.` |

### Процесс работы

| Уровень | Типичная задача | Процесс |
| --- | --- | --- |
| L0 · Простая | Опечатка, документация или механическая правка | Изучить → Изменить → Проверить |
| L1 · Обычная | Исправление бага или изолированная фича | Изучить → Реализовать → Протестировать → Провести ревью |
| L2 · Сложная | Рефакторинг или изменение в нескольких сервисах | Изучить → Составить и проверить план → Реализовать → Провести независимое ревью → Проверить |
| L3 · Критичная | Изменение в проде, операция с риском для безопасности или необратимое действие | Изучить → Оценить риск → Получить одобрение → Сделать бэкап → Подготовить план → Выполнить → Проверить → Восстановить при необходимости |

[SKILL.md](SKILL.md) описывает общий процесс и подсказывает агенту, какие справки загрузить для задачи. Восемь англоязычных справок охватывают [разработку](references/development.md), [проверку](references/verification.md), [работу в проде](references/production.md), [безопасность](references/security.md), [Git](references/git.md), [CI/CD](references/ci-cd.md), [локальное окружение](references/local-environment.md) и [документацию](references/documentation.md).
