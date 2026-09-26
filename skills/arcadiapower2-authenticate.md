---
name: arcadiapower2-authenticate
description: Obtain an access token and verify connectivity.
api: openapi/arcadiapower2-openapi.yaml
operations:
- createApiAccessToken
- ping
generated: '2026-09-25'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/arcadiapower2-openapi.yaml ; every operationId checked against the contract
---

# arcadiapower2-authenticate

Obtain an access token and verify connectivity.

## Steps

1. 1. Call `createApiAccessToken` with the required request body fields (as defined in the API contract).
2. 2. Use the returned access token in the `Authorization: Bearer <token>` header to call `ping` and confirm the token works.

## Rules

- Authentication: Include a `Authorization: Bearer <token>` header for protected endpoints.
- Rate limit: Maximum 100 requests per second; exceeding returns no specific HTTP status.
- Pagination: Not applicable for these operations.
