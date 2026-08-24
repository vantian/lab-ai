# To-Do List: AI Architecture Example

This directory is a documentation-only example of the reusable AI project
structure. It intentionally contains no application source code.

The fictional product is a small React and TypeScript to-do application that
stores data in the browser. The documents demonstrate how an AI agent learns the
product, selects engineering rules, plans work, tracks progress, and updates the
correct source of truth.

## How the AI reads this project

```text
AGENTS.md
  -> docs/INDEX.md
  -> docs/product/overview.md
  -> docs/engineering/stack.md
  -> relevant architecture and engineering documents
  -> matching tasks/task-{name}.md
  -> perform and verify work
  -> update the same task and existing canonical docs
```

## What each Markdown file does

| File | Purpose | Typical reading time |
|---|---|---|
| `AGENTS.md` | Shared operating rules and context-loading sequence | Start of agent work |
| `CLAUDE.md` | Makes Claude Code consume the shared rules | Claude Code startup |
| `docs/INDEX.md` | Documentation map and single-source-of-truth registry | Before selecting or creating docs |
| `docs/product/overview.md` | Product purpose, users, scope, journeys, and rules | Before feature work |
| `docs/product/terminology.md` | Canonical domain language | When naming or behavior uses product terms |
| `docs/architecture/overview.md` | Whole-system components, boundaries, and flows | When system behavior is involved |
| `docs/architecture/frontend.md` | React structure, state ownership, UI behavior, and accessibility | Frontend tasks |
| `docs/architecture/backend.md` | Explicitly records that the MVP has no backend | Backend, API, auth, or sync proposals |
| `docs/architecture/database.md` | Browser persistence model and migration rules | Data model or storage tasks |
| `docs/engineering/stack.md` | Approved technologies and dependency policy | Every implementation task |
| `docs/engineering/coding-rules.md` | Repository-specific implementation standards | When changing code |
| `docs/engineering/testing.md` | Test levels, responsibilities, and commands | Before and after changing behavior |
| `docs/engineering/workflows.md` | Task and documentation lifecycle | Planning and delivery |
| `docs/engineering/skills.md` | Specialized workflows an agent may use | Only when a matching task needs one |
| `docs/decisions/README.md` | ADR policy and decision index | When architecture may change |
| `docs/decisions/ADR-0001-use-browser-storage.md` | Why the MVP uses browser storage | Storage or backend discussions |
| `tasks/README.md` | Task naming and status rules | Before creating or updating tasks |
| `tasks/task-build-todo-mvp.md` | Example feature breakdown and tracking file | While working on the MVP task |

## Anti-duplication mechanism

Before creating a document, the agent must check `docs/INDEX.md`. If the topic
already has an owner, that file is updated. The task file contains the plan,
progress, decisions, verification, and completion summary, so the agent does not
create separate plan or report documents.
