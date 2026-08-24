# Documentation Registry

Each maintained topic has one canonical owner. Update the registered file rather
than creating a competing version.

| Topic | Canonical document | Read when | Update when |
|---|---|---|---|
| Product purpose, users, and scope | `product/overview.md` | Every feature task | Product goals, scope, journeys, or business rules change |
| Product vocabulary | `product/terminology.md` | Naming or domain behavior is involved | A product term is introduced or redefined |
| System structure and flows | `architecture/overview.md` | Components or boundaries are involved | Major flows or component responsibilities change |
| React application design | `architecture/frontend.md` | UI, state, routing, or accessibility changes | Frontend structure or behavior standards change |
| Server boundary | `architecture/backend.md` | An API, account, sync, or server is proposed | Backend scope changes |
| Browser data model | `architecture/database.md` | Todo shape or persistence changes | Stored data, keys, migrations, or failure handling change |
| Approved technologies | `engineering/stack.md` | Every implementation task | A technology, tool, or dependency policy changes |
| Coding standards | `engineering/coding-rules.md` | Code changes | Implementation standards change |
| Testing strategy | `engineering/testing.md` | Behavior changes | Tests, commands, or quality expectations change |
| Engineering workflow | `engineering/workflows.md` | Planning or delivery work | Task or documentation workflow changes |
| Agent skills | `engineering/skills.md` | Specialized work may apply | Available workflows change |
| Architecture decisions | `decisions/README.md` | Durable architecture changes are proposed | An ADR is added or its status changes |
| Task tracking policy | `../tasks/README.md` | A task is created or updated | Task lifecycle rules change |

## Creation rules

- A new document requires a topic with no existing canonical owner.
- The new owner must be registered here in the same change.
- Feature-specific plans and progress belong in `tasks/task-{name}.md`.
- Documentation describes current truth rather than change history.
- Version control retains previous versions.
