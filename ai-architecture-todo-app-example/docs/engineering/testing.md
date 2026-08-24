# Testing and Verification

## Test responsibilities

| Level | Covers | Examples |
|---|---|---|
| Unit | Pure todo transitions, validation, filters, and storage parsing | Empty description, completion transition, malformed stored data |
| Component | User-visible behavior and accessibility semantics | Add form, edit validation, filter selection, empty state |
| Integration | React feature working with the storage adapter | Load saved todos, persist changes, recover from storage failure |
| Browser journey | Critical end-to-end user outcomes | Add, reload, complete, filter, edit, and delete |

## Standard commands

| Check | Command | Expected result |
|---|---|---|
| Format | `npm run format:check` | No formatting differences |
| Lint | `npm run lint` | No lint errors |
| Type check | `npm run typecheck` | No TypeScript errors |
| Unit and component tests | `npm test` | Relevant tests pass |
| Production build | `npm run build` | Build succeeds |
| Browser tests | `npm run test:e2e` | Relevant journeys pass when Playwright is configured |

Commands are illustrative until the real project manifest defines them. Once the
project exists, this file must match the actual scripts rather than inventing them.

## Required cases for todo behavior

- Valid descriptions are trimmed and added.
- Empty and whitespace-only descriptions are rejected.
- The 200-character boundary is handled correctly.
- Completion can move in both directions.
- Filters display the correct subset without changing stored todos.
- Edits preserve identity and update the description.
- Deletion affects only the selected todo.
- Existing valid storage loads successfully.
- Missing, malformed, and unavailable storage fail safely.
- Keyboard and accessible names support primary actions.

## Reporting

Record the exact command, result, and any skipped checks in the active task file.
Never report a command as passing when it was not executed.
