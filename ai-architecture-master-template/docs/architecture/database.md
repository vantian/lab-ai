# Data Architecture

## Storage technologies

See `../engineering/stack.md`.

## Data ownership

| Data or aggregate | Owner | Source of truth | Consumers |
|---|---|---|---|
| {{DATA}} | {{OWNER}} | {{SOURCE}} | {{CONSUMERS}} |

## Schema and naming rules

- {{RULE}}

## Migration rules

- Migrations must preserve existing data unless data removal is explicitly approved.
- Risky migrations require rollout and rollback notes in the task file.
- {{PROJECT_SPECIFIC_RULE}}

## Transaction and consistency rules

- {{RULE}}

## Query and indexing rules

- Avoid unbounded reads and N+1 query patterns.
- Add indexes based on documented access patterns.
- {{PROJECT_SPECIFIC_RULE}}

## Sensitive data and retention

- {{RULE}}
