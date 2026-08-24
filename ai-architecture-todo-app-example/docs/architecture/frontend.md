# Frontend Architecture

## Responsibilities

The React application renders the product, owns the current session state, applies
todo transitions, and coordinates persistence through a storage adapter.

## Conceptual directory structure

```text
src/
  app/                 application entry and shell
  features/todos/      todo components, state transitions, and selectors
  storage/             browser persistence boundary
  styles/              shared visual styles and tokens
  test/                shared test setup and helpers
```

This tree describes responsibility boundaries; it does not require a separate file
for every small function.

## State ownership

| State | Owner | Persistent? |
|---|---|---|
| Todo collection | Todo feature at the nearest shared application level | Yes |
| Selected filter | Todo feature | No |
| New-todo input | Todo editor | No |
| Edit input and validation message | Todo row or edit form | No |
| Visible todos | Derived selector | No; never stored separately |

## Component responsibilities

- The application shell provides page landmarks and does not contain todo rules.
- The editor owns temporary input and reports a validated add action.
- The list receives already selected visible todos and renders stable identities.
- A todo row reports complete, edit, and delete intentions without persisting data.
- Filter controls express the selected view and visible counts.
- Empty-state content depends on the current filter.

## Behavior rules

- Use stable todo identifiers for rendering and updates.
- Do not use array position as identity.
- Derive counts and filtered views instead of synchronizing duplicate state.
- Focus returns to a predictable control after editing or deleting.
- Validation appears near the relevant input and is announced accessibly.
- A storage failure leaves the current in-memory session usable when possible.

## Accessibility

- Use a real form for todo entry.
- Use native buttons and checkboxes for actions and completion state.
- Every control has an accessible name.
- Keyboard focus is visible.
- Completed state is communicated beyond color or strikethrough.
- Status messages use an appropriate live region without excessive announcements.
- Color contrast meets WCAG AA expectations.

## Responsive behavior

- The primary workflow fits narrow mobile-sized viewports without horizontal
  scrolling.
- Touch targets remain comfortably operable.
- Text can wrap without hiding actions or status.
