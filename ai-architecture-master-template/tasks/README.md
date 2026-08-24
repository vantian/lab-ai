# Tasks

Each feature, bug, or meaningful engineering outcome uses exactly one task file:

`task-{short-kebab-case-name}.md`

The same file contains requirements, planning, progress, decisions, documentation
impact, verification, and completion. Do not create separate tracking or summary
files.

## Status lifecycle

```text
proposed -> ready -> in-progress -> blocked -> completed
```

`blocked` may return to `in-progress` when the blocker is resolved.

## Starting a task

1. Search this directory for an existing task with the same outcome.
2. Continue it if found.
3. Otherwise copy `../templates/task-template.md`.
4. Rename it to `task-{name}.md`.
5. Replace placeholders and set its status.

Completed tasks remain here as an auditable record. Do not create duplicate archive
copies. If the directory becomes large, add a task index rather than duplicating or
renaming task files.
