# Backend Architecture

## Current decision

The MVP has no backend.

All state is local to one browser profile and one device. No API, server process,
authentication service, or cloud database is part of the approved scope.

## Agent constraint

Do not create a backend to implement adding, editing, completing, deleting,
filtering, or locally preserving todos.

## When this document must change

A backend may be considered only when an approved product requirement introduces
one or more of these capabilities:

- Accounts or authentication
- Cross-device synchronization
- Sharing or collaboration
- Server-controlled authorization
- Remote backups
- Server-side integrations or notifications

Such a change requires:

1. An update to `../product/overview.md`.
2. A new task defining migration and compatibility expectations.
3. An ADR describing the service and data-ownership decision.
4. Updates to system, backend, data, security, and testing documentation before the
   task is considered complete.
