# PWEB Group Help Bot

PWEB Group Help Bot is a modular Telegram group administration and community-management system. Its production runtime is a PHP Telegram bot backed by persistent storage, Telegram Bot API integrations, scheduled workers and an operational web/API workspace for authenticated administration.

This public repository is a **documentation and project-reference mirror**. It intentionally contains no production credentials, environment files, operational memory or deployment artifacts. The complete implementation is maintained separately in the controlled development repository.

## Current runtime

The current project loads **55 modules** and registers **86 public commands**. The PHP runtime is the source of truth for command registration, effective permissions, group context, configuration and operational behavior.

| Component | Current implementation |
|---|---|
| Telegram bot | PHP 8.4 with modular services, event listeners, repositories, migrations and scheduled processing |
| Persistence | SQLite and PostgreSQL-compatible database layer with incremental migrations |
| Web/API workspace | TypeScript, React/Vite, Express, OpenAPI, Drizzle and PostgreSQL integration |
| Telegram authentication | Real Telegram Web App/session validation with server-side authorization |
| Operations | systemd-managed bot and Watchtower services with controlled deployment and health validation |
| Configuration | Inline Telegram configuration hub, group-scoped settings and role-aware actions |

## Current user-facing behavior

The `/commands` interface is permission-aware. It displays only commands that the effective role of the current user can execute in the current chat context. The list is separated into shared, group-only and private-only contexts, sorted alphabetically within each section, numbered continuously and navigated through inline pagination. The role is shown once in the header. The main list expires after inactivity, while command details reuse one temporary message and renew its timeout when a new number is consulted.

The `/duelo` command uses a real turn-based challenge flow. The challenger starts the first round, turns alternate between the challenger and the challenged player, only the active player can answer, and the round message visibly identifies the player whose turn is active beside the question and inline answer buttons. The active turn is persisted with the round so callbacks and scheduled processing use the same state.

The system also includes role-aware administration, moderation and protection modules, staff and administrator views, notes and records, achievements, player statistics, media features, federation support, group configuration, the Telegram Mini App and the Watchtower operational interface. These capabilities are backed by project services and real Telegram API integrations rather than placeholder data.

## Development and deployment principles

The bot is developed on dedicated feature branches and validated before publication. Production deployments run an isolated PHP lint pass, apply pending database migrations through `php console.php migrate`, restart the managed services and verify that the bot and Watchtower are active. The `main` branch remains separate from feature work unless an explicit integration is requested.

> The code and the validated runtime behavior are the source of truth.

Historical notes, agent memory, obsolete roadmaps and planning files are not authoritative documentation for current behavior unless they have been revalidated and incorporated into the controlled project documentation. Secrets, production environment files and local operational directories must never be committed to this public repository.
