---
name: axway-delete-session
description: Delete a specific session after locating it.
api: openapi/axway-session-api-openapi.yml
operations:
- session_query
- session_find
- session_remove
generated: '2026-10-04'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/axway-session-api-openapi.yml ; every operationId checked against the contract
---

# axway-delete-session

Delete a specific session after locating it.

## Steps

1. 1. Use `session_query` to search for sessions (no specific fields or headers required beyond authentication).
2. 2. Use `session_find` to retrieve details of a session (no additional fields or headers required beyond authentication).
3. 3. Use `session_remove` with the `session_id` path parameter to delete the session (no additional fields or headers required beyond authentication).

## Rules

- Authentication: include the `x-auth-token` header (AuthToken scheme).
- Idempotency: the `session_remove` DELETE operation is idempotent; repeated calls with the same `session_id` have no additional effect.
