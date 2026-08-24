---
title: "Build the To-Do List MVP"
status: ready
owner: "Product Engineering"
created: "2026-08-24"
updated: "2026-08-24"
---

# Task: Build the To-Do List MVP

## Outcome

An individual can add, review, complete, reactivate, filter, edit, and delete todos,
and the todos remain available after a normal browser reload.

## Background

This is the first implementation task for the product described in
`docs/product/overview.md`. The MVP is intentionally local-only and must not
introduce accounts, a backend, or cloud synchronization.

## Requirements

- Show a useful empty state when no todos exist.
- Add a todo using a trimmed description between 1 and 200 characters.
- Mark a todo completed or active.
- Filter todos by all, active, or completed.
- Edit an existing todo using the same description validation.
- Delete a selected todo.
- Preserve todos across reloads using the storage adapter.
- Recover safely when stored data is missing or malformed.
- Support keyboard operation and accessible names for all actions.

## Out of scope

- Accounts, authentication, and cloud synchronization
- Collaboration or sharing
- Due dates, reminders, tags, and projects
- Drag-and-drop sorting
- Undo history
- Backend services or remote databases

## Acceptance criteria

- [ ] A valid todo can be added and appears as active.
- [ ] Empty, whitespace-only, and over-limit descriptions show a clear error.
- [ ] A todo can be completed and reactivated.
- [ ] All, active, and completed filters show the correct todos.
- [ ] Editing preserves the todo's stable identity.
- [ ] Deleting affects only the selected todo.
- [ ] Todos remain after a normal page reload.
- [ ] Malformed stored data does not crash startup.
- [ ] Primary actions work with keyboard navigation.
- [ ] Relevant tests, type checks, linting, and production build pass.
- [ ] Canonical documentation describes the implemented behavior.

## Context to read

- `docs/product/overview.md`
- `docs/product/terminology.md`
- `docs/architecture/overview.md`
- `docs/architecture/frontend.md`
- `docs/architecture/database.md`
- `docs/engineering/stack.md`
- `docs/engineering/coding-rules.md`
- `docs/engineering/testing.md`
- `docs/decisions/ADR-0001-use-browser-storage.md`

The backend document is not required unless implementation appears to require a
server, which would indicate a scope conflict.

## Implementation plan

- [ ] Confirm project scripts and installed versions from manifests and lockfile.
- [ ] Establish the application shell and accessible page structure.
- [ ] Define the todo domain representation and validated state transitions.
- [ ] Define storage parsing, persistence, and failure behavior.
- [ ] Implement adding and validation.
- [ ] Implement completion and reactivation.
- [ ] Implement filtering and filter-specific empty states.
- [ ] Implement editing and focus behavior.
- [ ] Implement deletion.
- [ ] Add unit tests for domain and storage behavior.
- [ ] Add component tests for user interactions and accessibility semantics.
- [ ] Add the critical browser journey if Playwright is configured.
- [ ] Run required verification.
- [ ] Update affected canonical documentation.

## Progress log

### 2026-08-24

- Product and architecture documents reviewed.
- Scope confirmed as a client-only React application.
- Task broken into independently verifiable behavior slices.
- Status changed from `proposed` to `ready`.
- No implementation or verification has been performed in this documentation-only
  example.

## Decisions

### Keep filtering as derived state

**Decision:** Store the selected filter, but calculate visible todos and counts from
the canonical todo collection.

**Reason:** Storing filtered copies would duplicate data and create synchronization
bugs.

**Consequences:** Selectors must be tested, while persistence stores only todos and
not the current filtered view.

### Keep persistence behind an adapter

**Decision:** Components report actions through the feature boundary and never call
browser storage directly.

**Reason:** This keeps UI behavior testable and isolates validation and failure
handling at the storage boundary.

**Consequences:** The application needs one small persistence interface and an
in-memory substitute for tests.

## Blockers

- The actual project manifest does not exist in this documentation-only example, so
  command names and installed versions must be confirmed when implementation starts.

## Documentation impact

- [ ] Update `docs/architecture/frontend.md` if implemented component boundaries
  differ from the documented design.
- [ ] Update `docs/architecture/database.md` if the stored representation changes.
- [ ] Update `docs/engineering/testing.md` with actual project commands.
- [ ] Update `docs/product/overview.md` only if approved product behavior changes.
- [ ] Do not create an implementation summary; use this task's completion section.

## Verification

| Check | Command or method | Result |
|---|---|---|
| Unit and component tests | To be confirmed from project manifest | Not run; no application code exists in this example |
| Type checking | To be confirmed from project manifest | Not run; no application code exists in this example |
| Linting | To be confirmed from project manifest | Not run; no application code exists in this example |
| Production build | To be confirmed from project manifest | Not run; no application code exists in this example |
| Browser journey | Keyboard and reload workflow | Not performed; no application code exists in this example |

## Completion summary

**Final status:** Not completed; ready for implementation

**Implemented:**

- No application code. This file demonstrates planning and tracking only.

**Canonical documentation updated:**

- Initial product, architecture, engineering, and decision documents were prepared.

**Remaining risks or follow-up:**

- Confirm actual dependency versions and project commands after scaffolding.
- Validate local-storage failure behavior in supported browsers.
- Confirm focus behavior through component and browser testing.
