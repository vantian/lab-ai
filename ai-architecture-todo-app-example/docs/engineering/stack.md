# Technology Stack

Exact installed versions are determined by project manifests and the lockfile.
Agents must not assume or upgrade versions during unrelated tasks.

## Application

| Concern | Approved technology | Reason |
|---|---|---|
| Language | TypeScript in strict mode | Explicit contracts and safer refactoring |
| UI framework | React | Component-based UI and established testing support |
| Build tooling | Vite | Small, fast client application workflow |
| Styling | Plain CSS with a small shared token layer | The product does not require a component framework |
| Persistence | Browser local storage behind an adapter | Meets offline, single-device MVP scope |

## Quality tooling

| Concern | Approved technology |
|---|---|
| Unit and component tests | Vitest and React Testing Library |
| Browser journey tests | Playwright when configured |
| Static analysis | TypeScript and ESLint |
| Formatting | Prettier |

## Explicit exclusions for the MVP

- No backend framework
- No remote database
- No global state-management package
- No UI component framework
- No data-fetching library
- No authentication library

A new dependency requires a concrete problem that the existing stack cannot solve
cleanly, plus justification in the task file.
