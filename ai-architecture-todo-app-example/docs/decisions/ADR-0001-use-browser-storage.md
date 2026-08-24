# ADR-0001: Use Browser Storage for MVP Todos

**Status:** Accepted

**Date:** 2026-08-24

## Context

The MVP serves one person on one browser and does not include accounts,
collaboration, synchronization, or remote backup. Adding a backend would introduce
hosting, authentication, security, deployment, and operational work without serving
an approved product requirement.

## Decision

Store the todo collection in browser local storage through a dedicated adapter.
Keep UI components independent from the storage API and include a stored schema
version so future representations can be migrated.

## Positive consequences

- The application works without an account or network connection.
- The MVP has no server deployment or operational dependency.
- The architecture remains small enough to match the product scope.

## Negative consequences

- Todos are limited to one browser profile and device.
- Clearing site data removes todos.
- The product cannot provide collaboration, synchronization, or remote recovery.
- Storage capacity and availability are controlled by the browser.

## Alternatives considered

### Backend API and remote database

Rejected for the MVP because none of its benefits serve an approved requirement,
while it would substantially increase complexity and security responsibilities.

### In-memory state only

Rejected because preserving todos after reload is a product goal.

## Revisit when

Reconsider this decision if accounts, cross-device sync, sharing, or remote backup
becomes an approved product requirement.
