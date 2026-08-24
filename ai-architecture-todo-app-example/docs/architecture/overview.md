# System Architecture

## Context

ClearDay To-Do is a client-only single-page web application. All application logic
runs in the browser. The browser's local storage is the persistence boundary.

## Components

| Component | Responsibility | Owns |
|---|---|---|
| Application shell | Page structure, heading, and main regions | Layout only |
| Todo feature | User interactions and todo state transitions | In-memory todo collection and active filter |
| Todo editor | Captures and validates new or edited descriptions | Temporary form state |
| Todo list | Presents visible todos | No independent business state |
| Filter controls | Selects all, active, or completed view | User filter selection through feature state |
| Storage adapter | Loads and saves persistent todo data | Browser storage access and stored-data validation |

## Startup flow

1. The application starts.
2. The storage adapter reads the stored document.
3. Stored data is validated and normalized.
4. Valid todos become the initial in-memory state.
5. Invalid or unavailable storage produces a recoverable empty state and a user-safe
   message when necessary.

## Interaction flow

1. A user action reaches the todo feature.
2. The feature validates the requested transition.
3. In-memory state is updated.
4. The storage adapter persists the new collection.
5. React renders the view derived from current state and filter.

## Boundaries

- UI components do not access browser storage directly.
- The storage adapter does not own product decisions or UI behavior.
- Filtering is derived from todos and the selected filter; filtered copies are not
  stored as separate state.
- There is no network or backend boundary in the MVP.

## Cross-cutting concerns

- Validation occurs before creating or updating a todo.
- Storage failures must not crash the page.
- User messages must not expose raw internal exceptions.
- Accessibility behavior is part of feature acceptance criteria.
- The application does not collect personal data or telemetry in the MVP.
