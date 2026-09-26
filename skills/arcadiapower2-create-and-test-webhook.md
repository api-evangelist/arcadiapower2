---
name: arcadiapower2-create-and-test-webhook
description: Create a new webhook endpoint and trigger a test event to verify it.
api: openapi/arcadiapower2-openapi.yaml
operations:
- createWebhook
- requestWebookTestEvent
generated: '2026-09-25'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/arcadiapower2-openapi.yaml ; every operationId checked against the contract
---

# arcadiapower2-create-and-test-webhook

Create a new webhook endpoint and trigger a test event to verify it.

## Steps

1. 1. Use `createWebhook` with the request body fields required to define the webhook endpoint (e.g., `url`, `eventTypes`, etc.).
2. 2. Use `requestWebookTestEvent` with the path parameter `webhook_endpoint_id` returned from step 1 to trigger a test webhook event.

## Rules

- Auth: Include a Bearer token in the `Authorization` header (bearerAuth).
- Rate limit: Maximum 100 requests per second; exceeding this returns no specific HTTP error code.
