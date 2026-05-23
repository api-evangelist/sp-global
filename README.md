# S&P Global

S&P Global (NYSE: SPGI) is the parent of S&P Global Ratings, S&P Global Market Intelligence, S&P Dow Jones Indices, S&P Global Commodity Insights (Platts), S&P Global Mobility, and S&P Global Sustainable1. Its public developer surface is anchored by [Kensho Technologies](https://kensho.com) — S&P Global's wholly-owned AI subsidiary — which ships REST APIs for the **S&P Global LLM-Ready API (kFinance)**, **Extract**, **NERD**, **Scribe**, and the **Grounding Agent** (Alpha), plus the **S&P Capital IQ Pro** and **S&P Global Marketplace** data products distributed through the [S&P Global Marketplace](https://www.marketplace.spglobal.com).

This repository is the API Evangelist profile for S&P Global. It indexes the public API surface, captures the OpenAPI specs that back each Kensho product, and generates the supporting Naftiko capabilities, JSON Schemas, examples, plans, rate-limits, and FinOps mapping.

- Index file: [`apis.yml`](apis.yml)
- Master registry entry: [`api-evangelist-network/apis.yml` → `sp-global`](https://github.com/api-evangelist/api-evangelist-network)

## APIs

| API | OpenAPI | Capability | Docs |
|---|---|---|---|
| S&P Global LLM-Ready API (kFinance) — 60 endpoints | [openapi/kensho-llmready-openapi.yml](openapi/kensho-llmready-openapi.yml) | [capabilities/kensho-llm-ready-api.yaml](capabilities/kensho-llm-ready-api.yaml) | [docs.kensho.com/llmreadyapi](https://docs.kensho.com/llmreadyapi) |
| Kensho Extract — 5 endpoints | [openapi/kensho-extract-openapi.yml](openapi/kensho-extract-openapi.yml) | [capabilities/kensho-extract-api.yaml](capabilities/kensho-extract-api.yaml) | [docs.kensho.com/extract](https://docs.kensho.com/extract) |
| Kensho NERD — 3 endpoints | [openapi/kensho-nerd-openapi.yml](openapi/kensho-nerd-openapi.yml) | [capabilities/kensho-nerd-api.yaml](capabilities/kensho-nerd-api.yaml) | [docs.kensho.com/nerd](https://docs.kensho.com/nerd) |
| Kensho Scribe Batch v2 — 2 endpoints | [openapi/kensho-scribe-batch-v2-openapi.yml](openapi/kensho-scribe-batch-v2-openapi.yml) | [capabilities/kensho-scribe-api.yaml](capabilities/kensho-scribe-api.yaml) | [docs.kensho.com/scribe/v2](https://docs.kensho.com/scribe/v2/developer-guide) |
| Kensho Scribe Batch v1 — 1 endpoint (legacy) | [openapi/kensho-scribe-batch-v1-openapi.yml](openapi/kensho-scribe-batch-v1-openapi.yml) | _shared with v2 capability_ | [docs.kensho.com/scribe/v1](https://docs.kensho.com/scribe/v1/overview) |
| Kensho Grounding Agent (Alpha) | _no public OpenAPI yet_ | _pending_ | [docs.kensho.com/grounding](https://docs.kensho.com/grounding/overview) |
| S&P Capital IQ Pro | _enterprise data API_ | _via LLM-ready API_ | [spglobal.com/market-intelligence/.../sp-capital-iq-pro](https://www.spglobal.com/market-intelligence/en/solutions/products/sp-capital-iq-pro) |
| S&P Global Marketplace | _data catalog_ | _per dataset_ | [marketplace.spglobal.com](https://www.marketplace.spglobal.com) |

**Totals: 5 OpenAPI specs, 71 documented REST paths, 78 operations.**

## Artifacts

| Folder | Count | Description |
|---|---|---|
| `openapi/` | 5 | OpenAPI 3.x specs lifted from `docs.kensho.com` Next.js SSG data |
| `capabilities/` | 4 | Naftiko capability definitions with REST and MCP adapters |
| `json-schema/` | 9 | JSON Schemas for key Kensho entities (company, auditor, earnings, estimate, recommendation, CUSIP, extraction, annotation, transcription) |
| `json-structure/` | 9 | Field-level summaries of each schema |
| `json-ld/` | 1 | `sp-global-context.jsonld` — vocabulary bridge to schema.org / Wikidata |
| `examples/` | 75 | Per-operation request/response examples |
| `rules/` | 1 | Spectral ruleset enforcing S&P Global / Kensho conventions |
| `vocabulary/` | 1 | Domain vocabulary spanning business units, data domains, identifiers, capabilities |
| `plans/` | 1 | API Commons Plans 0.1 (trial + per-product subscriptions; pricing not publicly disclosed) |
| `rate-limits/` | 1 | API Commons Rate Limits 0.1 (limits negotiated per subscription; structure captured) |
| `finops/` | 1 | FOCUS-aligned billing mapping for Kensho + Capital IQ Pro |

## SDKs and Tooling

- **`kensho-kfinance`** — Python SDK on PyPI (`pip install kensho-kfinance`); see [github.com/kensho-technologies/kfinance](https://github.com/kensho-technologies/kfinance).
- **MCP server** — Ships in the `kfinance` package: `python -m kfinance.mcp` with stdio / SSE / streamable-http transports.
- **S&P Global Plugin (Claude Cowork)** — Skills for tearsheets, funding digests, earnings previews. See [github.com/kensho-technologies/spglobal-agent-skills](https://github.com/kensho-technologies/spglobal-agent-skills).
- **LLM-ready API examples** — Notebooks for OpenAI, Anthropic, Google Gemini (function calling, code generation, LangChain). See [github.com/kensho-technologies/llm-ready-api-examples](https://github.com/kensho-technologies/llm-ready-api-examples).

## Authentication

Per [docs.kensho.com/authentication](https://docs.kensho.com/authentication): OpenID Connect (OIDC) over OAuth 2.0. Two flows:

1. **Public-private keypair** — recommended for production / long-running unattended workloads.
2. **Refresh token** — suitable for development and testing.

## Notable Findings

- The `developer.spglobal.com` portal exists but does not host self-serve API references — the canonical developer documentation is `docs.kensho.com`, owned by S&P Global's AI subsidiary.
- The `SP-Global` GitHub org currently has **0 public repositories**; all open-source artifacts ship under [`kensho-technologies`](https://github.com/kensho-technologies).
- All five public Kensho REST APIs are documented with OpenAPI 3.x but served via Redocly inside Next.js — the specs are embedded in `_next/data/{buildId}/{slug}.json` rather than at standalone `openapi.json` URLs.
- The LLM-ready API (`kfinance.kensho.com`) is the broadest surface (60 paths) and is the AI-native re-projection of S&P Capital IQ.
- Pricing is **not** published publicly for any Kensho product or for Capital IQ Pro; access is gated through commercial@kensho.com and market.intelligence@spglobal.com.

## Notable Absences

- No public **Platts / Commodity Insights** OpenAPI on `docs.kensho.com`.
- No public **Sustainable1 / ESG** OpenAPI.
- No public **S&P Global Ratings** REST API.
- No public **S&P Dow Jones Indices** REST API on the developer portal.
- No published rate-limit numbers, no public price card, no RSS/changelog at `developer.spglobal.com`.
- `marketplace.spglobal.com` endpoints frequently return 403 to unauthenticated WebFetch — listings appear gated behind a JS client.

## Maintainers

- Kin Lane — `kin@apievangelist.com`
- Kensho Technologies (S&P Global) — `commercial@kensho.com`
- S&P Global Market Intelligence — `market.intelligence@spglobal.com`
