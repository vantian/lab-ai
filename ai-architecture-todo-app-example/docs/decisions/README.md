# Architecture Decision Records

ADRs record durable choices that materially affect system boundaries, data
ownership, public interfaces, security, or core technology.

Routine component, naming, and implementation decisions stay in task files.

## Index

| ADR | Status | Decision |
|---|---|---|
| `ADR-0001-use-browser-storage.md` | Accepted | Store MVP todos locally rather than introducing a backend |

## Naming

Use `ADR-{four-digit-number}-{short-kebab-case-title}.md`.

When a decision changes, add a new ADR that supersedes the old one. Do not rewrite
an accepted ADR to pretend the original context never existed.
