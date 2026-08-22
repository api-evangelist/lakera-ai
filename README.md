# Lakera (lakera-ai)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
