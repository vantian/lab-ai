# Coding Rules

## General

- Match existing naming, formatting, module, and error-handling conventions.
- Prefer clear, maintainable code over clever abstractions.
- Keep functions and modules focused on one responsibility.
- Remove duplication only when the shared concept is stable and meaningful.
- Avoid unrelated refactoring during feature or bug-fix tasks.
- Do not add dependencies without recorded justification.
- Do not expose secrets or sensitive information in code, logs, or errors.

## Frontend

- Separate presentation from business logic where practical.
- Avoid duplicated and unnecessarily synchronized state.
- Use the established design system and component library.
- Address relevant loading, empty, success, validation, and error states.
- Use semantic markup, keyboard support, labels, and visible focus behavior.
- Do not rely on client-side checks for authorization or data security.

## Backend

- Keep transport handlers thin.
- Separate transport, business, and persistence responsibilities.
- Validate and normalize input at boundaries.
- Enforce authorization server-side.
- Use safe parameterized persistence APIs.
- Define predictable errors and response contracts.
- Consider transactions, concurrency, idempotency, pagination, and rate limits
  when relevant.

## Data

- Preserve existing data unless removal is explicitly approved.
- Avoid unbounded queries and N+1 patterns.
- Define atomic transaction boundaries for related writes.
- Document rollout and rollback for risky migrations.

## Project-specific additions

- {{RULE}}
