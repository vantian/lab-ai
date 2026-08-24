# AI Project Master Template

Reusable repository structure for Codex, Claude Code, and human contributors.

## What this template provides

- One shared instruction source in `AGENTS.md`
- Claude Code compatibility through `CLAUDE.md`
- A documentation registry that prevents duplicate documents
- Separate product, architecture, engineering, and decision knowledge
- One-file task planning, progress tracking, verification, and completion
- Stack-neutral placeholders for frontend and backend projects

## Install in a project

1. Copy the contents of this directory into the repository root.
2. Replace every `{{PLACEHOLDER}}` value.
3. Complete `docs/product/overview.md` and `docs/engineering/stack.md`.
4. Adjust build and test commands in `docs/engineering/testing.md`.
5. Remove architecture documents that genuinely do not apply.
6. Keep `docs/INDEX.md` synchronized whenever documentation ownership changes.

If the repository already has documentation, register the existing files in
`docs/INDEX.md` instead of creating replacements.

## Operating model

```text
AGENTS.md
    -> docs/INDEX.md
    -> product overview
    -> relevant architecture and engineering rules
    -> one tasks/task-{name}.md
    -> implementation and verification
    -> update existing canonical documentation
```

The task file is the plan, tracker, decision log, verification record, and
completion summary. Do not create separate files for those purposes.
