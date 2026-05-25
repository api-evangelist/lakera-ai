# Lakera (lakera-ai)

Lakera is an AI-native security platform that protects GenAI applications, agents, and workforces from prompt injection, data leakage, PII exposure, content violations, and malicious links. Lakera Guard exposes a single-endpoint runtime screening API (`/v2/guard`) that accepts OpenAI-style chat messages and returns a flagged decision in sub-50ms; a companion `/v2/guard/results` endpoint returns L1-L5 detector confidence levels for offline analysis. The Lakera Platform API lets Enterprise customers manage policies (detector sensitivity and action) and projects (per-application bindings) programmatically. Founded in Zurich and acquired by Check Point Software in 2025, Lakera also operates Gandalf, the 1M+ player prompt injection challenge that feeds its detector training pipeline, and publishes the open-source PINT benchmark for prompt injection detection evaluation.

**URL:** [Visit APIs.json](https://raw.githubusercontent.com/api-evangelist/lakera-ai/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Tags

 - AI Security, Artificial Intelligence, Generative AI, LLM Security, Prompt Injection, AI Guardrails, AI Red Teaming, Data Loss Prevention, Content Moderation, Check Point

## Timestamps

- **Created:** 2026-05-25
- **Modified:** 2026-05-25

## Products

| Product | Purpose |
|---|---|
| Lakera Guard | Runtime AI security screening for LLM applications (sub-50ms, 100+ languages) |
| Lakera Red | AI red-teaming with direct and indirect attack simulations and risk-based findings |
| AI Agent Security | Runtime protection for autonomous agents and tool use |
| Workforce AI Security | Monitors employee AI usage across applications and browsers |
| Gandalf | 1M+ player prompt injection challenge feeding detector training signal |
| PINT Benchmark | Open prompt injection detection benchmark on GitHub |

## APIs

### Lakera Guard API

Lakera Guard's runtime screening API. POST OpenAI-style chat messages to `/v2/guard` and receive a `flagged` decision based on the policy assigned to the project, with optional per-detector breakdown and payload-level PII/profanity match locations. Detectors cover prompt attacks, data leakage, PII, content violations, and unknown links across 100+ languages with sub-50ms latency. A second endpoint, `/v2/guard/results`, returns detector confidence levels (L1-L5) for offline analysis and threshold tuning without contributing to runtime screening logs.

**Human URL:** [https://docs.lakera.ai/docs/api/guard](https://docs.lakera.ai/docs/api/guard)

- [Documentation — Guard API](https://docs.lakera.ai/docs/api/guard)
- [Documentation — Results API](https://docs.lakera.ai/docs/api/results)
- [Documentation — Quickstart](https://docs.lakera.ai/docs/quickstart)
- [OpenAPI](openapi/lakera-guard-api-openapi.yml)
- [JSON Schema — Request](json-schema/lakera-guard-request-schema.json)
- [JSON Schema — Response](json-schema/lakera-guard-response-schema.json)
- [JSON Structure](json-structure/lakera-guard-request-structure.json)
- [JSON-LD](json-ld/lakera-ai-context.jsonld)
- [Example — Screen Content](examples/lakera-guard-screen-content-example.json)
- [Example — Results](examples/lakera-guard-results-example.json)
- [Naftiko Capability — Guard Screening](capabilities/guard-screening.yaml)

### Lakera Platform API

The Lakera Platform API lets Enterprise SaaS customers programmatically manage Lakera Guard policies and projects. Policies select detectors and per-detector sensitivity (L1-L5); projects bind a protected application to a policy and an API key scope. Self-hosted deployments expose additional `/policies/lint` and `/policies/health` endpoints plus Kubernetes `startupz`/`readyz`/`livez` probes for in-cluster operation.

**Human URL:** [https://platform.lakera.ai/docs/api](https://platform.lakera.ai/docs/api)

- [OpenAPI](openapi/lakera-platform-api-openapi.yml)
- [Naftiko Capability — Platform Policies](capabilities/platform-policies.yaml)

## Detectors

| Detector | Mapping | Notes |
|---|---|---|
| `prompt_attack` | OWASP LLM01 | Prompt injection, jailbreaks, instruction-override attempts |
| `pii` | OWASP LLM06 | Personally identifiable information in prompts and responses |
| `content_moderation` | — | Offensive, hateful, sexual, violent, vulgar content |
| `unknown_links` | — | URLs outside the configured allow-list |
| `custom` | — | Organization-defined detectors |

Confidence levels follow OWASP paranoia conventions: **L1 Confident**, **L2 Very Likely**, **L3 Likely**, **L4 Less Likely**, **L5 Unlikely**.

## Regional Endpoints

| Region | Base URL |
|---|---|
| Global | `https://api.lakera.ai/v2` |
| US East | `https://api.us-east.lakera.ai/v2` |
| US West | `https://api.us-west.lakera.ai/v2` |
| EU West | `https://api.eu-west.lakera.ai/v2` |
| Asia Pacific | `https://api.ap.lakera.ai/v2` |

## Plans, Rate Limits, and FinOps

- [Plans and Pricing (API Commons Plans 0.1)](plans/lakera-ai-plans-pricing.yml)
- [Rate Limits (API Commons Rate Limits 0.1)](rate-limits/lakera-ai-rate-limits.yml)
- [FinOps (FOCUS-aligned)](finops/lakera-ai-finops.yml)

## Governance

- [Spectral Rules](rules/lakera-rules.yml)
- [Vocabulary](vocabulary/lakera-ai-vocabulary.yml)

## Integrations and Tooling

- [LiteLLM Lakera Guardrail](https://docs.litellm.ai/docs/proxy/guardrails/lakera_ai)
- [PINT Benchmark](https://github.com/lakeraai/pint-benchmark)
- [Lakera Guard Demo Client (Python)](https://github.com/lakeraai/guard-demo-client)
- [Lakera Chrome Extension — ChatGPT Data Leak Protection](https://github.com/lakeraai/chrome-extension)
- [Canica — Text Embedding Viewer](https://github.com/lakeraai/canica)
- [Lakera Docs MCP Server](https://docs.lakera.ai/_mcp/server)
- [Gandalf — prompt injection sandbox](https://gandalf.lakera.ai)

## Common Resources

- [Lakera homepage](https://www.lakera.ai)
- [Lakera documentation](https://docs.lakera.ai)
- [Lakera platform](https://platform.lakera.ai)
- [Pricing](https://platform.lakera.ai/pricing)
- [Blog](https://www.lakera.ai/blog)
- [Customers](https://www.lakera.ai/customers)
- [Trust Center](https://trust.lakera.ai)
- [Terms of Service](https://www.lakera.ai/legal/terms)
- [Privacy Policy](https://www.lakera.ai/legal/privacy)
- [GitHub Organization](https://github.com/lakeraai)
- [LinkedIn](https://www.linkedin.com/company/lakeraai)

## Maintainer

- **Kin Lane** — [API Evangelist](https://apievangelist.com) — info@apievangelist.com
