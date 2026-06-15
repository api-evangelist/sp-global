# S&P Global (sp-global)

S&P Global (NYSE SPGI) is the parent of S&P Global Ratings, S&P Global Market Intelligence, S&P Dow Jones Indices, S&P Global Commodity Insights (Platts), S&P Global Mobility, and S&P Global Sustainable1. Its public developer surface is anchored by Kensho Technologies (a wholly-owned S&P Global AI subsidiary) which ships REST APIs for the S&P Global LLM-ready API (kFinance), Extract, NERD, Scribe, and the Grounding Agent, plus the S&P Capital IQ Pro and Marketplace data products distributed through the S&P Global Marketplace.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/sp-global/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/sp-global/refs/heads/main/apis.yml)

## Scope

- **Position:** Consuming
- **Access:** 3rd-Party

## Tags

- Capital IQ
- Commodity Insights
- Credit Ratings
- Document Extraction
- ESG
- Financial Data
- Index Data
- LLM
- MCP
- Market Intelligence
- Mobility
- Named Entity Recognition
- Speech to Text

## Timestamps

- **Created:** 2026-05-23
- **Modified:** 2026-05-29

## APIs

### S&P Global LLM-Ready API (kFinance)

REST API and Model Context Protocol server exposing S&P Capital IQ Financials, Market Data, Business Relationships, Earnings Call Transcripts, Company Intelligence, M&A Transactions, and Global Securities information to LLMs and agentic AI applications. Distributed via the kensho-kfinance Python library and an MCP server compatible with Claude, ChatGPT, Microsoft Copilot Studio, Amazon QuickSuite, Databricks, and Mistral. 60 documented REST endpoints across companies, securities, statements, estimates, transcripts, mergers, funding rounds, and identifier crosswalks.

- **Human URL:** [https://docs.kensho.com/llmreadyapi](https://docs.kensho.com/llmreadyapi)
- **Base URL:** `https://kfinance.kensho.com`

#### Tags

- Financial Data
- Capital IQ
- LLM
- MCP
- Agents
- Market Intelligence

#### Properties

- [OpenAPI](openapi/kensho-llmready-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/kensho-llmready.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/kensho-llmready.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Documentation](https://docs.kensho.com/llmreadyapi)
- [API Reference](https://docs.kensho.com/llmreadyapi/api)
- [Overview](https://docs.kensho.com/llmreadyapi/overview)
- [SDK](https://pypi.org/project/kensho-kfinance/)
- [SDK](https://github.com/kensho-technologies/kfinance)
- [Sandbox](https://github.com/kensho-technologies/llm-ready-api-examples)
- [M C P Server](https://docs.kensho.com/llmreadyapi/mcp)
- [SDK](https://github.com/kensho-technologies/spglobal-agent-skills)
- [Authentication](https://docs.kensho.com/authentication)
- [Sign Up](https://www.marketplace.spglobal.com/en/solutions/kensho-llm-ready-api-%28a156fe9f-5564-4f60-a624-95d8645dc98f%29)
- [JSON-LD](json-ld/sp-global-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)

### Kensho Extract API

Transforms unstructured PDF and image documents into machine-readable JSON, identifying titles, subtitles, paragraphs, tables, and footers in natural reading order. Optional OCR and Figure Extraction (FigEx). REST API at extract.kensho.com with asynchronous extractions and presigned upload/download URLs.

- **Human URL:** [https://docs.kensho.com/extract](https://docs.kensho.com/extract)
- **Base URL:** `https://extract.kensho.com`

#### Tags

- Document Extraction
- OCR
- PDF
- Tables
- Unstructured Data

#### Properties

- [OpenAPI](openapi/kensho-extract-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/kensho-extract.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/kensho-extract.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Documentation](https://docs.kensho.com/extract)
- [API Reference](https://docs.kensho.com/extract/api)
- [Quickstart](https://docs.kensho.com/extract/quickstart)
- [Tutorials](https://docs.kensho.com/extract/toolkit)
- [Authentication](https://docs.kensho.com/authentication)
- [Sign Up](https://kensho.com/extract)
- [JSON-LD](json-ld/sp-global-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)

### Kensho NERD API

Named-Entity Recognition and Disambiguation REST service linking text mentions to S&P Capital IQ company identifiers and to Wikimedia entities (people, places, events). Supports asynchronous batch annotation with optional person tagging and originating-entity context for financial documents.

- **Human URL:** [https://docs.kensho.com/nerd](https://docs.kensho.com/nerd)
- **Base URL:** `https://nerd.kensho.com`

#### Tags

- NER
- Entity Linking
- NLP
- Capital IQ
- Wikimedia

#### Properties

- [OpenAPI](openapi/kensho-nerd-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/kensho-nerd.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/kensho-nerd.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Documentation](https://docs.kensho.com/nerd)
- [API Reference](https://docs.kensho.com/nerd/api)
- [Overview](https://docs.kensho.com/nerd/overview)
- [Tutorials](https://docs.kensho.com/nerd/text-annotation)
- [Authentication](https://docs.kensho.com/authentication)
- [JSON-LD](json-ld/sp-global-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)

### Kensho Scribe Batch API v2

Asynchronous audio and video transcription REST API. POST a media file to start a transcription job, then poll the transcription ID for completion. Optimised for finance and business audio (earnings calls, conferences). Companion real-time WebSocket API and Human-in-the-Loop batch option are documented alongside.

- **Human URL:** [https://docs.kensho.com/scribe/v2/developer-guide](https://docs.kensho.com/scribe/v2/developer-guide)
- **Base URL:** `https://scribe.kensho.com`

#### Tags

- Speech to Text
- Transcription
- Audio
- Video
- Batch

#### Properties

- [OpenAPI](openapi/kensho-scribe-batch-v2-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/kensho-scribe-batch-v2.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/kensho-scribe-batch-v2.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Documentation](https://docs.kensho.com/scribe/v2/developer-guide)
- [API Reference](https://docs.kensho.com/scribe/v2/batch-api-specification)
- [Tutorials](https://docs.kensho.com/scribe/v2/batch-development)
- [Authentication](https://docs.kensho.com/authentication)
- [JSON-LD](json-ld/sp-global-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)

### Kensho Scribe Real Time API

Real-time streaming transcription over a WebSocket at wss://scribe.kensho.com/ws. Clients send an Authenticate message with a Kensho OIDC access token, then StartTranscription with an audio_format (RAW pcm_s16le, 16 kHz, mono), followed by base64-encoded AddData chunks of at most 15 seconds each carrying monotonically increasing sequence_numbers, and finally EndOfStream. The server streams TranscriptionStarted, DataAdded, AddTranscript, EndOfTranscript, and Error messages back over the same socket. This is the only public WebSocket surface S&P Global exposes — Capital IQ Pro, Marketplace, and other market-data feeds are delivered via REST, file/SFTP, Snowflake share, and Databricks share.

- **Human URL:** [https://docs.kensho.com/scribe/v2/developer-guide](https://docs.kensho.com/scribe/v2/developer-guide)
- **Base URL:** `wss://scribe.kensho.com/ws`

#### Tags

- Speech to Text
- Transcription
- WebSocket
- Streaming
- Real Time
- AsyncAPI

#### Properties

- [AsyncAPI](asyncapi/kensho-scribe-realtime-asyncapi.yml) — [AsyncAPI Specification](https://www.asyncapi.com/docs/reference/specification/latest)
- [Documentation](https://docs.kensho.com/scribe/v2/developer-guide)
- [API Reference](https://docs.kensho.com/scribe/v2/real-time-api-specification)
- [Authentication](https://docs.kensho.com/authentication)
- [JSON-LD](json-ld/sp-global-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [Postman Collection](collections/kensho-extract.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/kensho-extract.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/kensho-llmready.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/kensho-llmready.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/kensho-nerd.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/kensho-nerd.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/kensho-scribe-batch-v1.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/kensho-scribe-batch-v1.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/kensho-scribe-batch-v2.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/kensho-scribe-batch-v2.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Kensho Scribe Batch API v1

Legacy v1 batch transcription endpoint (POST /api/v1/transcription). Superseded by the v2 batch API which decouples submission from result retrieval. Documented here for customers on the v1 contract.

- **Human URL:** [https://docs.kensho.com/scribe/v1/overview](https://docs.kensho.com/scribe/v1/overview)
- **Base URL:** `https://scribe.kensho.com`

#### Tags

- Speech to Text
- Transcription
- Audio
- Legacy

#### Properties

- [OpenAPI](openapi/kensho-scribe-batch-v1-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/kensho-scribe-batch-v1.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/kensho-scribe-batch-v1.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Documentation](https://docs.kensho.com/scribe/v1/overview)
- [API Reference](https://docs.kensho.com/scribe/v1/batch-api-specification)
- [Authentication](https://docs.kensho.com/authentication)

### Kensho Grounding Agent (Alpha)

Data retrieval service that translates natural-language queries into structured retrieval tasks across S&P Global AI-ready datasets. Returns answers with source citations linking back to the underlying S&P Global data. Currently Alpha — access by request to commercial@kensho.com. No public OpenAPI yet.

- **Human URL:** [https://docs.kensho.com/grounding/overview](https://docs.kensho.com/grounding/overview)

#### Tags

- Grounding
- Agents
- Retrieval
- Citations
- Alpha

#### Properties

- [Documentation](https://docs.kensho.com/grounding/overview)
- [Getting Started](https://docs.kensho.com/grounding/api-guide)
- [Sign Up](https://kensho.com/grounding)
- [Postman Collection](collections/kensho-extract.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/kensho-extract.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/kensho-llmready.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/kensho-llmready.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/kensho-nerd.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/kensho-nerd.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/kensho-scribe-batch-v1.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/kensho-scribe-batch-v1.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/kensho-scribe-batch-v2.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/kensho-scribe-batch-v2.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### S&P Capital IQ Pro

Flagship desktop and API platform for S&P Global Market Intelligence — company fundamentals, ownership, transactions, estimates, news, screening, charting, and Office plug-ins. The Capital IQ Pro API is delivered as part of an enterprise subscription rather than as a self-serve developer signup; the LLM-ready API exposes a substantial subset of the same dataset.

- **Human URL:** [https://www.spglobal.com/market-intelligence/en/solutions/products/sp-capital-iq-pro](https://www.spglobal.com/market-intelligence/en/solutions/products/sp-capital-iq-pro)

#### Tags

- Capital IQ
- Market Intelligence
- Financial Data
- Enterprise

#### Properties

- [Documentation](https://www.spglobal.com/market-intelligence/en/solutions/products/sp-capital-iq-pro)
- [Sign Up](https://www.spglobal.com/market-intelligence/en/contact-us)
- [Postman Collection](collections/kensho-extract.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/kensho-extract.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/kensho-llmready.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/kensho-llmready.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/kensho-nerd.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/kensho-nerd.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/kensho-scribe-batch-v1.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/kensho-scribe-batch-v1.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/kensho-scribe-batch-v2.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/kensho-scribe-batch-v2.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### S&P Global Marketplace

Data and analytics catalog spanning S&P Global business units (Market Intelligence, Ratings, Commodity Insights/Platts, Mobility, Sustainable1, Indices, Dow Jones) plus third-party vendors. Distribution mechanisms include Snowflake shares, Databricks shares, file/SFTP delivery, API access, and packaged datasets. The Marketplace is the front door for discovering S&P Global APIs that are sold through enterprise channels.

- **Human URL:** [https://www.marketplace.spglobal.com](https://www.marketplace.spglobal.com)

#### Tags

- Marketplace
- Data Catalog
- Distribution
- Snowflake Share
- Databricks

#### Properties

- [Documentation](https://www.marketplace.spglobal.com)
- [Sign Up](https://www.marketplace.spglobal.com/en/sign-up)
- [Postman Collection](collections/kensho-extract.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/kensho-extract.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/kensho-llmready.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/kensho-llmready.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/kensho-nerd.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/kensho-nerd.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/kensho-scribe-batch-v1.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/kensho-scribe-batch-v1.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/kensho-scribe-batch-v2.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/kensho-scribe-batch-v2.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Portal](https://developer.spglobal.com)
- [Documentation](https://docs.kensho.com)
- [Marketplace](https://www.marketplace.spglobal.com)
- [Authentication](https://docs.kensho.com/authentication)
- [SDK](https://pypi.org/project/kensho-kfinance/)
- [SDK](https://github.com/kensho-technologies/kfinance)
- [SDK](https://github.com/kensho-technologies/spglobal-agent-skills)
- [Code Examples](https://github.com/kensho-technologies/llm-ready-api-examples)
- [Git Hub](https://github.com/kensho-technologies)
- [Git Hub](https://github.com/SP-Global)
- [Blog](https://www.spglobal.com/en/research-insights)
- [Blog](https://kensho.com/blog)
- [Plans](plans/sp-global-plans-pricing.yml)
- [Rate Limits](rate-limits/sp-global-rate-limits.yml)
- [Fin Ops](finops/sp-global-finops.yml)
- [JSON-LD](json-ld/sp-global-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [JSON Schema](json-schema/kensho-llmready-company-info-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/kensho-extract-extraction-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/kensho-nerd-annotation-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [Vocabulary](vocabulary/sp-global-vocabulary.yml)
- [Features](undefined)
- [Use Cases](undefined)
- [Integrations](undefined)
- [Subsidiaries](undefined)
- [L L Ms Txt](https://developer.spglobal.com/llms.txt)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
**Email:** commercial@kensho.com
**URL:** https://kensho.com
**Email:** market.intelligence@spglobal.com
**URL:** https://www.spglobal.com/market-intelligence
