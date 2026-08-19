# PWEB Group Help Bot

PWEB Group Help Bot is a modular Telegram group administration and community-management system. Its validated production runtime is a PHP Telegram bot backed by persistent storage, real Telegram Bot API integrations, scheduled workers and an operational web/API workspace for authenticated administration.

## Purpose of this repository

This repository is a **public documentation and project-reference mirror**. It intentionally contains no production source code, credentials, environment files, deployment bundles, operational memory or private infrastructure artifacts. The complete implementation and its validated runtime are maintained in the private authoritative repository [PWEB-GroupHelpBot-TG](https://github.com/sistemacodigolucrativo/PWEB-GroupHelpBot-TG).

The public mirror is intended for project orientation and documentation access. It is not a deployment source and must not be used to operate the production bot.

## Current runtime

The current validated runtime loads **54 modules** and registers **80 public commands**. The official configuration gateway is `/menu`, while the PHP runtime remains the source of truth for command registration, effective permissions, group context, configuration and operational behavior.

| Component | Current implementation |
|---|---|
| Telegram bot | PHP 8.4 with modular services, event listeners, repositories, migrations and scheduled processing |
| Persistence | SQLite and PostgreSQL-compatible database layer with incremental migrations |
| Web/API workspace | TypeScript, React/Vite, Express, OpenAPI, Drizzle and PostgreSQL integration |
| Telegram authentication | Real Telegram Web App and session validation with server-side authorization |
| Operations | systemd-managed bot and Watchtower services with controlled deployment and health validation |
| Configuration | `/menu` as the official group gateway, private administrative delivery, group-scoped settings and role-aware actions |
| Administrative context | User-bound private-menu sessions, single-use access tokens and permission revalidation in the managed group |

## Documentation entry points

The validated project documentation is organized under the `documentation/` directory in the authoritative private implementation repository.

| Area | Documentation |
|---|---|
| Documentation index | [`documentation/README.md`](https://github.com/sistemacodigolucrativo/PWEB-GroupHelpBot-TG/tree/main/documentation) |
| Project overview | [`documentation/overview/project.md`](https://github.com/sistemacodigolucrativo/PWEB-GroupHelpBot-TG/blob/main/documentation/overview/project.md) |
| Runtime modules | [`documentation/reference/modules.md`](https://github.com/sistemacodigolucrativo/PWEB-GroupHelpBot-TG/blob/main/documentation/reference/modules.md) |
| Registered commands | [`documentation/reference/commands.md`](https://github.com/sistemacodigolucrativo/PWEB-GroupHelpBot-TG/blob/main/documentation/reference/commands.md) |
| Configuration | [`documentation/bot/configuration.md`](https://github.com/sistemacodigolucrativo/PWEB-GroupHelpBot-TG/blob/main/documentation/bot/configuration.md) |
| Telegram Mini App | [`documentation/operations/telegram-mini-app.md`](https://github.com/sistemacodigolucrativo/PWEB-GroupHelpBot-TG/blob/main/documentation/operations/telegram-mini-app.md) |
| Testing | [`documentation/development/testing.md`](https://github.com/sistemacodigolucrativo/PWEB-GroupHelpBot-TG/blob/main/documentation/development/testing.md) |
| Changelog | [`documentation/changelog.md`](https://github.com/sistemacodigolucrativo/PWEB-GroupHelpBot-TG/blob/main/documentation/changelog.md) |
| Features and releases | [`documentation/news-features.md`](https://github.com/sistemacodigolucrativo/PWEB-GroupHelpBot-TG/blob/main/documentation/news-features.md) |

## Current user-facing behavior

The `/commands` interface is permission-aware. It displays only commands that the effective role of the current user can execute in the current chat context. The list is separated into shared, group-only and private-only contexts, sorted alphabetically within each section, numbered continuously and navigated through inline pagination. The role is shown once in the header rather than repeated for every command. The main list message expires after inactivity, while command details reuse one temporary message and renew its timeout when a new number is consulted.

The `/start` menu includes a paginated **About** presentation. Its pages are rendered by editing the same Telegram message, provide explicit navigation boundaries and include a return action to the main menu. The presentation describes only capabilities confirmed in the current runtime.

The `/menu` command is the official textual gateway for group configuration. The administrative panel is delivered in the operator's private Telegram chat, while the group remains separate from the administrative output. The private context is bound to the user and managed group, and permissions are revalidated before administrative callbacks are processed.

The `/duelo` command uses a real turn-based challenge flow. The challenger starts the first round, turns alternate between the challenger and the challenged player, only the active player can answer, and the round message visibly identifies the player whose turn is active beside the question and inline answer buttons. The active turn is persisted with the round so callbacks and scheduled processing use the same state.

The system also includes role-aware administration, moderation and protection modules, staff and administrator views, achievements, player statistics, media features, federation support, group configuration, the Telegram Mini App and the Watchtower operational interface. These capabilities are backed by project services and real Telegram API integrations rather than placeholder data.

## Repository roles

The repositories have distinct responsibilities. The private operational repository is the authoritative source for the complete implementation, validated documentation and production-aligned changes. This public repository provides only a safe reference surface for the project.

| Repository | Role |
|---|---|
| [`PWEB-GroupHelpBot-TG`](https://github.com/sistemacodigolucrativo/PWEB-GroupHelpBot-TG) | Private authoritative implementation, validated runtime source and operational project history |
| [`PWEB-Group-Help-Bot`](https://github.com/sistemacodigolucrativo/PWEB-Group-Help-Bot) | Public documentation and project-reference mirror |

## Development and deployment principles

The bot is validated before publication. Production deployments run an isolated PHP lint pass, apply pending database migrations through `php console.php migrate`, restart the managed services and verify that the bot and Watchtower are active. The private repository's `main` branch is the authoritative integration point for the current implementation.

> The code and the validated runtime behavior are the source of truth.

Historical memories, planning files and obsolete roadmaps are not authoritative for current behavior unless they have been revalidated and incorporated into the controlled project documentation. Secrets, production environment files and local operational directories must never be committed to this public repository.

## Documentation status

This public mirror is aligned with the validated runtime inventory of **54 loaded modules** and **80 registered commands**. It documents the project without exposing production source, credentials or deployment-specific artifacts.
