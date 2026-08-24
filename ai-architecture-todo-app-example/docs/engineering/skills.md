# Specialized Skills Registry

Skills are optional workflows, not general project knowledge. An agent reads or
invokes one only when the task directly matches it.

| Task type | Appropriate workflow | Use for | Do not use for |
|---|---|---|---|
| Browser verification | Browser-control or web-testing skill | Keyboard flow, responsive layout, storage persistence, visible states | Pure domain validation |
| Accessibility review | Accessibility audit workflow | Semantics, labels, focus, contrast, and announcements | Replacing component tests |
| Visual design | Image or design workflow | Reference visuals or intentional UI exploration | Inventing product scope |
| Documentation artifact | Document workflow when a non-Markdown deliverable is requested | Exported formal documents | Routine repository Markdown |

## Rules

- Read a skill's own instructions before using it.
- Use only the minimum relevant workflow.
- Keep resulting task status and decisions in the existing task file.
- Do not copy entire external skill instructions into this repository.
- Tool availability depends on the agent environment; absence of a skill is not
  permission to fabricate results.
