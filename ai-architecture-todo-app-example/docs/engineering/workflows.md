# Engineering Workflows

## Starting work

1. Read `../INDEX.md`, the product overview, stack, and relevant architecture.
2. Search `../../tasks/` for an existing task with the same outcome.
3. Continue the existing task or create one `task-{name}.md`.
4. Confirm scope, acceptance criteria, and documentation impact.
5. Set the task to `ready` or `in-progress` as appropriate.

## Implementing

1. Inspect the existing behavior and tests.
2. Implement the smallest complete checklist item.
3. Add or update tests for changed behavior.
4. Update progress, decisions, and blockers in the same task file.
5. Avoid unrelated refactoring or documentation.

## Verifying

1. Run targeted tests during development.
2. Run relevant lint, type, test, and build checks before completion.
3. Record actual results in the task verification table.
4. Document skipped checks and why they could not run.

## Updating documentation

1. Consult `../INDEX.md` for the topic owner.
2. Update the existing owner to describe the resulting system.
3. Remove obsolete statements instead of keeping competing versions.
4. Create and register a new document only for a new responsibility.
5. Put implementation history in the task file, not the canonical document.

## Completing

1. Confirm every acceptance criterion.
2. Confirm canonical documentation is current.
3. Complete the verification table and remaining-risks section.
4. Set the original task status to `completed`.
5. Do not create a completion report.
