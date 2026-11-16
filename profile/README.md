# LifeSteward

**Smarter Home. Greener Life.**

A local-first home steward. One deployment serves one household: devices, documents, schedules, health, learning, and fitness, with room to add hardware and agents over time. The phone is the primary client. The software is a general product, not a one-off for a particular home, and is written so it can be open-sourced later.

## Repositories in This Organization

| Repository | Status | Description |
| --- | --- | --- |
| [docs](https://github.com/lifesteward/docs) | Active | Design, plans, protocols, decisions, and the brand kit |
| [steward](https://github.com/lifesteward/steward) | Active (M0 skeleton) | Server, web admin, and contracts. One modular process, not a set of microservices |
| [steward-app](https://github.com/lifesteward/steward-app) | Not started | Android app. The phone is the primary client |
| [steward-deploy](https://github.com/lifesteward/steward-deploy) | Active (M0 templates) | Deployment templates. Application data stays on the household's own hardware |

## Design Principles

1. **One domain model.** Household, member, space, device, document, record, and event each have a single definition used everywhere.
2. **Four protocols.** Terminals, device control, tools, and events. New hardware and new agents join by following the protocols.
3. **One server.** A modular monolith: one process, with clear module boundaries. Not microservices.
4. **Permissions are enforced in data and tools.** Not by asking the model to behave.
5. **Local-first.** Originals, the database, and indexes stay on the household's hardware. A cloud model receives only the fragment needed for the current turn.
6. **Use mature third-party systems behind adapters.** The device hub can be replaced without rewriting the rest of the system.
