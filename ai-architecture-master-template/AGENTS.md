# Repository Agent Instructions

## Mission

Work as a senior software engineer within the existing product, architecture,
and engineering standards. Make the smallest complete change that satisfies the
task, verify it, and leave canonical documentation accurate.

## Context loading

Before planning or changing code, read in this order:

1. `docs/INDEX.md`
2. `docs/product/overview.md`
3. `docs/engineering/stack.md`
4. The architecture and engineering documents relevant to the request
5. The matching `tasks/task-{name}.md`, if it exists

Do not load every document. Use `docs/INDEX.md` to select only relevant sources.

## Sources of truth

- `docs/INDEX.md` owns the documentation registry.
- `docs/product/overview.md` owns product purpose, users, and boundaries.
- Files under `docs/architecture/` own current system design.
- Files under `docs/engineering/` own development standards and workflows.
- Files under `tasks/` own task-specific plans, progress, and verification.
- Version control owns historical versions of documentation.

When sources conflict, stop and identify the conflict. Do not silently choose or
create another document.

## Task workflow

Task filenames must use `tasks/task-{short-kebab-case-name}.md`.

Before implementation:

1. Search for an existing task covering the same outcome.
2. Continue the existing file when found.
3. Otherwise copy `templates/task-template.md` to the required task filename.
4. Set its status and break the work into verifiable checklist items.
5. Identify affected canonical documentation.

During implementation:

1. Inspect relevant existing code before editing.
2. Update the task checklist and progress log in the same task file.
3. Record material decisions, scope changes, and blockers there.
4. Keep the change focused; avoid unrelated refactoring.
5. Add or update tests for changed behavior.

After implementation:

1. Run relevant tests, linting, type checking, and builds.
2. Record commands and actual results in the task file.
3. Update affected canonical documentation.
4. Mark acceptance criteria and documentation checks accurately.
5. Set the task status to `completed` only when required work is finished.
6. Write the completion summary in the same task file.

Do not create separate plan, progress, implementation-summary, final-report, or
completion files.

## Documentation control

Before creating any documentation file:

1. Read `docs/INDEX.md`.
2. Search the repository for the topic and related terminology.
3. Update the registered canonical document when it owns the topic.
4. Create a new file only when the topic has no canonical owner and cannot fit an
   existing document without mixing unrelated concerns.
5. Register the new document in `docs/INDEX.md` in the same change.

Never create versioned alternatives such as:

- `architecture-new.md`
- `architecture-updated.md`
- `architecture-v2.md`
- `feature-summary.md`
- `implementation-summary.md`
- `final-report.md`

Documentation describes the current system. Task files and version control
preserve implementation history. Replace obsolete statements rather than keeping
old and new descriptions together.

## Architecture and coding rules

- Follow existing patterns and boundaries unless the task authorizes a change.
- Reuse existing components, services, utilities, and dependencies where suitable.
- Keep presentation, business, and persistence concerns separated.
- Validate untrusted input at system boundaries.
- Enforce authentication and authorization on the server.
- Never expose secrets, credentials, or sensitive data.
- Preserve compatibility unless a breaking change is explicitly approved.
- Do not invent APIs, packages, schemas, commands, or project conventions.
- Do not introduce dependencies without a clear, recorded justification.
- Do not leave placeholders, incomplete branches, or silent failures.

Detailed rules live in `docs/engineering/coding-rules.md`.

## Testing and verification

- Follow `docs/engineering/testing.md`.
- Cover the primary success path and meaningful failure or edge cases.
- Prefer the testing style and tools already established by the repository.
- Never claim a check passed unless it was executed successfully.
- Record failed or skipped checks and their reason.

## Architecture decisions

Create an ADR under `docs/decisions/` only for a durable decision that changes
system structure, boundaries, data ownership, public interfaces, security posture,
or an important technology choice. Routine implementation decisions stay in the
task file.

## Skills

Read `docs/engineering/skills.md` when a task may require a specialized workflow.
Use only skills relevant to the request and follow their instructions before acting.

## Completion standard

A task is complete only when:

- Acceptance criteria are satisfied.
- Required implementation and tests are present.
- Relevant verification has been run or limitations are documented.
- Canonical documentation reflects the resulting system.
- The original task file contains final status and results.
- No redundant documentation was created.
