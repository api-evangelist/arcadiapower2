---
name: arcadiapower2-retrieve-utility-credentials
description: Retrieve utility credentials by listing them and then fetching a specific credential.
api: openapi/arcadiapower2-openapi.yaml
operations:
- getUtilityCredentials
- getUtilityCredential
generated: '2026-09-25'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/arcadiapower2-openapi.yaml ; every operationId checked against the contract
---

# arcadiapower2-retrieve-utility-credentials

Retrieve utility credentials by listing them and then fetching a specific credential.

## Steps

1. 1. Call `getUtilityCredentials` with optional pagination query parameters `page`, `size`, and `sort`.
2. 2. From the list response, obtain the `utility_credential_id` of the desired credential.
3. 3. Call `getUtilityCredential` with the path parameter `utility_credential_id` to retrieve the full credential details.

## Rules

- Authentication: Include a Bearer token in the `Authorization` header (bearerAuth).
- Pagination: Use `page` (0‑indexed, default 0), `size` (default 20, max 100 for most resources), and optional `sort` query parameters when listing.
- Rate limit: Maximum 100 requests per second; exceeding the limit returns no specific HTTP status code.
