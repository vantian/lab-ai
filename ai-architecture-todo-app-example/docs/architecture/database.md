# Data Architecture

## Persistence technology

The MVP uses the browser's local storage through a dedicated storage adapter.
This is local persistence, not a relational or server database.

## Stored document

| Field | Meaning | Rules |
|---|---|---|
| Schema version | Version of the stored representation | Required positive integer |
| Todos | Ordered collection of todo records | Defaults to an empty collection |

## Todo record

| Field | Meaning | Rules |
|---|---|---|
| ID | Stable identity | Unique, generated once, never based on array position |
| Description | User-visible todo text | Trimmed, 1–200 characters |
| Completed | Completion state | Boolean; defaults to false |
| Created at | Creation timestamp | Stored in a consistent machine-readable format |
| Updated at | Last meaningful modification timestamp | Changes after edits or completion transitions |

## Storage rules

- Use one application-owned storage key.
- UI components never access local storage directly.
- Every load validates unknown stored data before using it.
- Missing data produces an empty collection.
- Malformed data is ignored safely rather than crashing application startup.
- Write failures preserve the current in-memory session and produce a user-safe
  notification when continued persistence cannot be guaranteed.

## Migration rules

- The stored document includes a schema version from the first release.
- Compatible additions use defaults when older data lacks a field.
- A breaking representation change requires a migration and tests using the prior
  stored format.
- Destructive migration requires explicit product approval.

## Privacy and retention

- Data remains in the user's browser profile.
- The application does not transmit todos in the MVP.
- Clearing site data removes stored todos.
- The UI should not imply cloud backup or recovery.
