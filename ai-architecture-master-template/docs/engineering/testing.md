# Testing and Verification

## Test strategy

| Level | Tool | Location | Required for |
|---|---|---|---|
| Unit | {{TOOL}} | `{{PATH}}` | Business logic and utilities |
| Component | {{TOOL}} | `{{PATH}}` | Important UI behavior |
| Integration | {{TOOL}} | `{{PATH}}` | APIs, persistence, and integrations |
| End-to-end | {{TOOL}} | `{{PATH}}` | Critical user journeys |

## Commands

| Check | Command | Expected result |
|---|---|---|
| Format | `{{COMMAND}}` | No formatting changes required |
| Lint | `{{COMMAND}}` | No errors |
| Type check | `{{COMMAND}}` | No errors |
| Frontend tests | `{{COMMAND}}` | All relevant tests pass |
| Backend tests | `{{COMMAND}}` | All relevant tests pass |
| Build | `{{COMMAND}}` | Successful build |
| End-to-end tests | `{{COMMAND}}` | Relevant journeys pass |

Remove checks that do not apply; do not leave fake commands.

## Coverage expectations

- Test changed behavior, not implementation trivia.
- Cover the primary success path and meaningful failure or boundary cases.
- Reproduce bugs with a failing test when practical.
- Do not weaken or delete tests merely to make a change pass.
- Record every executed, failed, or skipped check in the task file.
