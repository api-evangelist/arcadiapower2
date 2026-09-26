---
name: arcadiapower2-enroll-and-create-utility-remittance
description: Enroll a utility credential in the Bundle Utility Remittance program, create a remittance item, and retrieve the created item.
api: openapi/arcadiapower2-openapi.yaml
operations:
- enrollUtilityRemittance
- createUtilityRemittanceItem
- getUtilityRemittanceItem
generated: '2026-09-25'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/arcadiapower2-openapi.yaml ; every operationId checked against the contract
---

# arcadiapower2-enroll-and-create-utility-remittance

Enroll a utility credential in the Bundle Utility Remittance program, create a remittance item, and retrieve the created item.

## Steps

1. 1. Call `enrollUtilityRemittance` with the path parameter `utility_credential_id` and required request body to enroll the utility credential.
2. 2. Call `createUtilityRemittanceItem` with the path parameter `utility_statement_id` and request body containing the remittance item details.
3. 3. Call `getUtilityRemittanceItem` with the path parameter `utility_remittance_item_id` returned from the previous step to retrieve the created item.

## Rules

- Auth: Include a `Authorization: Bearer <token>` header (bearerAuth).
- Rate limit: Maximum 100 requests per second; exceeding this returns no specific HTTP status code.
- Idempotency: Not defined for these endpoints; callers should avoid duplicate requests.
- Errors: Follow standard HTTP error responses as defined by the API (e.g., 4xx for client errors, 5xx for server errors).
