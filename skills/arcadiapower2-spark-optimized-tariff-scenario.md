---
name: arcadiapower2-spark-optimized-tariff-scenario
description: Find applicable tariffs and calculate the cost of a tariff‑scenario for Spark resources.
api: openapi/arcadiapower2-openapi.yaml
operations:
- searchLoadServingEntities
- getOptimizedTariffsApplicabilities
- searchOptimizedTariffsByApplicabilities
- calculateOptimizedTariffsScenarioCost
generated: '2026-09-25'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/arcadiapower2-openapi.yaml ; every operationId checked against the contract
---

# arcadiapower2-spark-optimized-tariff-scenario

Find applicable tariffs and calculate the cost of a tariff‑scenario for Spark resources.

## Steps

1. 1. `searchLoadServingEntities` – no request body; use query parameters if needed.
2. 2. `getOptimizedTariffsApplicabilities` – no request body; use query parameters if needed.
3. 3. `searchOptimizedTariffsByApplicabilities` – provide the applicability answers in the request body.
4. 4. `calculateOptimizedTariffsScenarioCost` – submit the selected tariff and scenario details in the request body.

## Rules

- Auth: Include a Bearer token in the `Authorization` header (bearerAuth).
- Rate limit: 100 requests per second; exceeding returns no specific HTTP error code.
- Pagination: When applicable, use `page`, `size`, and `sort` query parameters.
