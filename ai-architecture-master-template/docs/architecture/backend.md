# Backend Architecture

## Stack

See `../engineering/stack.md`.

## Responsibilities

- {{RESPONSIBILITY}}

## Directory structure

```text
{{BACKEND_DIRECTORY_STRUCTURE}}
```

## Layers and boundaries

| Layer | Responsibility | Must not own |
|---|---|---|
| {{LAYER}} | {{RESPONSIBILITY}} | {{EXCLUDED_RESPONSIBILITY}} |

## API conventions

- Style: {{REST_GRAPHQL_RPC_OR_OTHER}}
- Versioning: {{APPROACH}}
- Validation: {{APPROACH}}
- Error format: {{APPROACH}}
- Pagination: {{APPROACH}}

## Security

- Authentication: {{APPROACH}}
- Authorization: {{APPROACH}}
- Sensitive-data handling: {{APPROACH}}

## Integrations and background work

- {{INTEGRATION_OR_JOB}}

## Backend testing

See `../engineering/testing.md`.
