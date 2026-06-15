# Lakera (lakera-ai)

Lakera is an AI-native security platform that protects GenAI applications, agents, and workforces from prompt injection, data leakage, PII exposure, content violations, and malicious links. Lakera Guard exposes a single-endpoint runtime screening API (/v2/guard) that accepts OpenAI-style chat messages and returns a flagged decision in sub-50ms; a companion /v2/guard/results endpoint returns L1–L5 detector confidence levels for offline analysis. The Lakera Platform API lets Enterprise customers manage policies (detector sensitivity and action) and projects (per-application bindings) programmatically. Founded in Zurich and acquired by Check Point Software in 2025, Lakera also operates Gandalf, the 1M+ player prompt injection challenge that feeds its detector training pipeline, and publishes the open-source PINT benchmark for prompt injection detection evaluation.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/lakera-ai/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/lakera-ai/refs/heads/main/apis.yml)

## Scope

- **Position:** Consuming
- **Access:** 3rd-Party

## Tags

- AI Security
- Artificial Intelligence
- Generative AI
- LLM Security
- Prompt Injection
- AI Guardrails
- AI Red Teaming
- Data Loss Prevention
- Content Moderation
- Check Point

## Timestamps

- **Created:** 2026-05-25T00:00:00.000Z
- **Modified:** 2026-05-25

## APIs

### Lakera Guard API

Lakera Guard's runtime screening API. POST OpenAI-style chat messages to /v2/guard and receive a `flagged` decision based on the policy assigned to the project, with optional per-detector breakdown and payload-level PII/profanity match locations. Detectors cover prompt attacks, data leakage, PII, content violations, and unknown links across 100+ languages with sub-50ms latency. A second endpoint, /v2/guard/results, returns detector confidence levels (L1–L5) for offline analysis and threshold tuning without contributing to runtime screening logs.

- **Human URL:** [https://docs.lakera.ai/docs/api/guard](https://docs.lakera.ai/docs/api/guard)

#### Tags

- AI Security
- Artificial Intelligence
- Guard
- Prompt Injection
- PII
- Content Moderation

#### Properties

- [Documentation](https://docs.lakera.ai/docs/api/guard)
- [Getting Started](https://docs.lakera.ai/docs/quickstart)
- [Documentation](https://docs.lakera.ai/api-reference/lakera-api/guard/screen-content)
- [OpenAPI](openapi/lakera-guard-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/lakera-guard-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/lakera-guard-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/lakera-guard-request-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/lakera-guard-response-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Structure](json-structure/lakera-guard-request-structure.json)
- [JSON-LD](json-ld/lakera-ai-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [Example](examples/lakera-guard-screen-content-example.json)
- [Example](examples/lakera-guard-results-example.json)

### Lakera Platform API

The Lakera Platform API lets Enterprise SaaS customers programmatically manage Lakera Guard policies and projects. Policies select detectors and per-detector sensitivity (L1–L5); projects bind a protected application to a policy and an API key scope. Self-hosted deployments expose additional /policies/lint and /policies/health endpoints plus Kubernetes startupz/readyz/livez probes for in-cluster operation.

- **Human URL:** [https://platform.lakera.ai/docs/api](https://platform.lakera.ai/docs/api)

#### Tags

- AI Security
- Administration
- Policies
- Projects
- Enterprise

#### Properties

- [Documentation](https://platform.lakera.ai/docs/api)
- [OpenAPI](openapi/lakera-platform-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/lakera-platform-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/lakera-platform-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [LinkedIn](https://www.linkedin.com/company/lakeraai)
- [Portal](https://www.lakera.ai)
- [Documentation](https://docs.lakera.ai)
- [Documentation](https://docs.lakera.ai/docs/api)
- [Getting Started](https://docs.lakera.ai/docs/quickstart)
- [Documentation](https://docs.lakera.ai/guard)
- [Documentation](https://docs.lakera.ai/docs/integration)
- [Documentation](https://docs.lakera.ai/llms.txt)
- [M C P Server](https://docs.lakera.ai/_mcp/server)
- [Portal](https://platform.lakera.ai)
- [Pricing](https://platform.lakera.ai/pricing)
- [Support](https://www.lakera.ai/contact)
- [Blog](https://www.lakera.ai/blog)
- [Press](https://www.lakera.ai/news)
- [Case Study](https://www.lakera.ai/customers)
- [Terms of Service](https://www.lakera.ai/legal/terms)
- [Privacy Policy](https://www.lakera.ai/legal/privacy)
- [Trust Center](https://trust.lakera.ai)
- [Sandbox](https://gandalf.lakera.ai)
- [GitHub Organization](https://github.com/lakeraai)
- [Tool](https://github.com/lakeraai/pint-benchmark)
- [Code Examples](https://github.com/lakeraai/guard-demo-client)
- [Tool](https://github.com/lakeraai/chrome-extension)
- [Tool](https://github.com/lakeraai/canica)
- [Tool](https://github.com/lakeraai/dsec-gandalf)
- [Tool](https://github.com/lakeraai/intent-augmentation)
- [Integration](https://docs.litellm.ai/docs/proxy/guardrails/lakera_ai)
- [Plans](plans/lakera-ai-plans-pricing.yml)
- [Rate Limits](rate-limits/lakera-ai-rate-limits.yml)
- [Fin Ops](finops/lakera-ai-finops.yml)
- [Spectral Rules](rules/lakera-rules.yml)
- [Vocabulary](vocabulary/lakera-ai-vocabulary.yml)
- [Features](undefined)

## Maintainers

**FN:** Kin Lane
**Email:** info@apievangelist.com
**URL:** https://apievangelist.com
