# Coding Rules

## General

- Use TypeScript strictness rather than bypassing uncertain values.
- Name concepts using `docs/product/terminology.md`.
- Prefer small, cohesive modules with explicit responsibilities.
- Keep product transitions independent from React rendering and browser storage when
  practical.
- Reuse established patterns before creating abstractions.
- Do not refactor unrelated code during feature work.
- Do not add a package for behavior that is small and clear with the current stack.

## React

- Use function components and hooks.
- Keep state at the nearest level shared by its consumers.
- Derive visible todos and counts; do not synchronize duplicate state.
- Avoid effects for values that can be calculated during rendering.
- Keep browser APIs behind adapters.
- Use stable identifiers for rendered collections.
- Keep components focused on either coordination or presentation when that separation
  improves clarity.

## Validation and errors

- Trim a description before validating or storing it.
- Reject empty or over-limit descriptions with a specific user-facing message.
- Treat data read from browser storage as unknown input.
- Recover from malformed storage without exposing raw exceptions.
- Do not discard an in-memory user action silently when persistence fails.

## Accessibility

- Prefer native semantic elements before custom roles.
- Support keyboard operation for every action.
- Preserve a logical heading structure and page landmarks.
- Do not communicate completion, errors, or selection using color alone.

## Documentation

- Update existing canonical documents instead of creating new summaries.
- Record task-specific reasoning and verification in the original task file.
