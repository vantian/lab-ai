# Documentation Registry

This file is the table of contents and ownership registry for maintained project
knowledge. Each topic has one canonical owner.

## Canonical documents

| Topic | Canonical document | Read when | Update when |
|---|---|---|---|
| Product purpose and users | `product/overview.md` | Every feature task | Product goals, users, scope, or key journeys change |
| Product terminology | `product/terminology.md` | Business language is involved | A domain term is introduced or redefined |
| System architecture | `architecture/overview.md` | System boundaries or flows are involved | Components, boundaries, or major flows change |
| Frontend architecture | `architecture/frontend.md` | Frontend code or UX behavior changes | Frontend structure, state, routing, or UI standards change |
| Backend architecture | `architecture/backend.md` | Backend or API behavior changes | Services, APIs, integrations, or backend boundaries change |
| Data architecture | `architecture/database.md` | Persistence or data contracts change | Schemas, ownership, migrations, or access patterns change |
| Technology stack | `engineering/stack.md` | Every implementation task | Languages, frameworks, versions, or tooling change |
| Coding rules | `engineering/coding-rules.md` | Code is created or changed | Repository-wide coding standards change |
| Testing strategy | `engineering/testing.md` | Behavior is created or changed | Test tools, commands, or coverage expectations change |
| Development workflow | `engineering/workflows.md` | Build, release, or collaboration is involved | Team workflows or delivery processes change |
| Specialized skills | `engineering/skills.md` | A specialized workflow may apply | Skills are added, removed, or retargeted |
| Architecture decisions | `decisions/README.md` | A durable architecture choice is proposed | ADR policy or index changes |
| Task workflow | `../tasks/README.md` | Planning or tracking work | Task lifecycle or naming rules change |

## Rules

- Update the canonical owner instead of creating a competing document.
- A new document requires a genuinely new topic and a new registry row.
- Task-specific facts belong in `tasks/task-{name}.md`.
- Documentation describes current behavior, not a chronological change log.
- Version control preserves prior versions.
- Links must point to canonical files.
