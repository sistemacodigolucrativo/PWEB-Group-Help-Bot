# PWEB Group Help Bot

PWEB Group Help Bot is a modular Telegram group administration and community-management system. Its production runtime is a PHP Telegram bot backed by persistent storage, a real Telegram Bot API integration, scheduled workers, and an operational web/API workspace for authenticated administration.

The project is organized around the following official documentation directory:

```text
documentation/
```

The recommended entry points are:

| Area | Documentation |
|---|---|
| Documentation index | [documentation/README.md](documentation/README.md) |
| Project overview | [documentation/overview/project.md](documentation/overview/project.md) |
| Runtime modules | [documentation/reference/modules.md](documentation/reference/modules.md) |
| Registered commands | [documentation/reference/commands.md](documentation/reference/commands.md) |
| Configuration | [documentation/bot/configuration.md](documentation/bot/configuration.md) |
| Telegram Mini App | [documentation/operations/telegram-mini-app.md](documentation/operations/telegram-mini-app.md) |
| Testing | [documentation/development/testing.md](documentation/development/testing.md) |
| Changelog | [documentation/changelog.md](documentation/changelog.md) |
| Features and releases | [documentation/news-features.md](documentation/news-features.md) |

## Current runtime

The current codebase loads **54 modules** and registers **80 public commands**. The main configuration gateway is `/menu`, while the PHP runtime remains the source of truth for command registration, effective permissions, group context, and operational behavior.

| Component | Current implementation |
|---|---|
| Telegram bot | PHP 8.4 with modular services, event listeners, repositories, migrations, and scheduled processing |
| Persistence | SQLite and PostgreSQL-compatible database layer with incremental migrations |
| Web/API workspace | TypeScript, React/Vite, Express, OpenAPI, Drizzle and PostgreSQL integration |
| Telegram authentication | Real Telegram Web App/session validation for the operational portal, with server-side authorization |
| Operations | systemd-managed bot and Watchtower services with controlled deployment and health validation |
| Configuration | Inline Telegram configuration hub, group-scoped settings and role-aware actions |

## Current user-facing behavior

The `/commands` interface is permission-aware. It displays only commands that the effective role of the current user can execute in the current chat context. The list is separated into shared, group-only and private-only contexts, sorted alphabetically within each section, numbered continuously and navigated through inline pagination. The role is shown once in the header rather than repeated for every command. The main list message expires after inactivity, while command details reuse one temporary message and renew its timeout when a new number is consulted.

The `/duelo` command is implemented as a real turn-based challenge flow. The challenger starts the first round, turns alternate between the challenger and the challenged player, only the player whose turn is active can submit an answer, and the round message visibly identifies the current player next to the question and inline answer buttons. The active turn is persisted with the round so that callbacks and scheduled processing use the same state.

The system also includes role-aware administration, moderation and protection modules, staff and administrator views, operational records, achievements, player statistics, media features, federation support, group configuration, the Telegram Mini App, and the Watchtower operational interface. These features use the project services and Telegram API integrations rather than placeholder data.

## Repository structure

| Path | Responsibility |
|---|---|
| `bot/` | PHP Telegram bot, core services, modules, migrations and runtime entry points |
| `artifacts/` | Built web/API and dashboard assets used by the operational workspace |
| `documentation/` | Validated project documentation and operational references |
| `tests/` | Module and integration-oriented validation scripts |
| `scripts/` | Installation, service and operational automation |

## Development and deployment

The bot is developed on dedicated feature branches and validated before publication. Production deployments run an isolated PHP lint pass, apply pending database migrations through `php console.php migrate`, restart the managed services, and verify that the bot and Watchtower are active. The `main` branch is kept separate from feature work unless an explicit integration is requested.

## Important rule

> The code and the validated runtime behavior are the source of truth.

Historical notes, agent memory, obsolete roadmaps and planning files are not authoritative documentation for current behavior unless the information has been revalidated and incorporated into `documentation/`. Secrets, production environment files and local operational directories must not be committed to the repository.
