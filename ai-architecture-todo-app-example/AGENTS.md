# To-Do List Repository Instructions

## Mission

Maintain a small, accessible, reliable to-do application without adding complexity
outside the approved product scope.

## Required startup context

Before planning or changing behavior, read:

1. `docs/INDEX.md`
2. `docs/product/overview.md`
3. `docs/engineering/stack.md`
4. Documents relevant to the requested area
5. The matching file under `tasks/`, if one exists

Do not load every document or task file.

## Product boundaries

- The MVP is a single-user browser application.
- Todos are stored locally in the browser.
- The MVP has no account, server, cloud database, collaboration, or synchronization.
- Do not introduce a backend merely to implement an existing MVP requirement.
- A task that changes these boundaries must update product documentation and
  propose an architecture decision before implementation.

## Task workflow

- Use one file named `tasks/task-{short-kebab-case-name}.md` per outcome.
- Search for an existing matching task before creating one.
- Keep requirements, plan, progress, decisions, blockers, verification, and
  completion in that file.
- Do not create separate plan, progress, summary, or final-report documents.
- Set a task to `completed` only after acceptance criteria, verification, and
  documentation work are finished.

## Documentation control

Before creating documentation:

1. Read `docs/INDEX.md`.
2. Search for an existing document that owns the topic.
3. Update the canonical owner when it exists.
4. Create a new document only for a genuinely new topic.
5. Register a new canonical document in `docs/INDEX.md` immediately.

Never create names such as `frontend-v2.md`, `updated-architecture.md`,
`feature-summary.md`, or `final-report.md`. Documentation describes the current
system; task files and version control preserve history.

## Engineering rules

- Follow `docs/engineering/coding-rules.md`.
- Follow the component and state boundaries in `docs/architecture/frontend.md`.
- Use only technologies registered in `docs/engineering/stack.md` unless a task
  explicitly approves a change.
- Keep domain behavior testable without depending directly on browser APIs.
- Treat browser storage as an external boundary with predictable failure handling.
- Preserve keyboard access, semantic controls, visible focus, and readable status
  announcements.
- Avoid unrelated refactoring and unnecessary dependencies.

## Testing and completion

- Follow `docs/engineering/testing.md`.
- Test changed behavior and meaningful edge cases.
- Record every executed, failed, or skipped check in the task file.
- Never claim a check passed unless it was actually executed.
- Update canonical documentation when product behavior, architecture, storage, or
  workflow changes.
