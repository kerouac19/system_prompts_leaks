# External Integrations

**Analysis Date:** 2026-03-30

## APIs & External Services

**AI Model Providers:**
- OpenAI - Various GPT models (4o, 4.1, 4.5, 5.x series)
  - SDK/Client: Documentation of system prompts for ChatGPT, API endpoints
  - Auth: Not documented in repository (likely via API keys not stored here)

- Anthropic - Claude models (Sonnet, Opus, Haiku 4.x series)
  - SDK/Client: Claude API, Anthropic SDK documentation
  - Auth: Not documented in repository (likely via API keys not stored here)

- Google - Gemini models (Flash, Pro)
  - SDK/Client: Gemini API, Google AI SDK
  - Auth: Not documented in repository (likely via API keys not stored here)

- xAI - Grok models (3, 4, 4.x series)
  - SDK/Client: Grok API and platform
  - Auth: Not documented in repository (likely via API keys not stored here)

- Perplexity - Various assistants (Comet, Voice)
  - SDK/Client: Perplexity API and tools
  - Auth: Not documented in repository (likely via API keys not stored here)

**Tools & Capabilities:**
- Web search functionality integrated into Claude
- Code execution capabilities
- File handling (creation/processing)
- Gmail integration
- Google Calendar integration
- Google Drive search and access
- Slack integration (Canvas, messages, threads, profiles)

## Data Storage

**Databases:**
- Local filesystem - All system prompts appear to be stored as individual markdown files

**File Storage:**
- GitHub repository storage for markdown files

**Caching:**
- None explicitly documented

## Authentication & Identity

**Auth Provider:**
- External providers (OpenAI, Anthropic, Google, etc.) - Each AI provider handles authentication separately
  - Implementation: API key-based authentication (not documented in this repository)

## Monitoring & Observability

**Error Tracking:**
- Not documented

**Logs:**
- Not applicable - This is a static documentation repository

## CI/CD & Deployment

**Hosting:**
- GitHub repository
- May be served via GitHub Pages (HTML/CSS/JS present in Anthropic section)

**CI Pipeline:**
- Not documented - This is a documentation repository

## Environment Configuration

**Required env vars:**
- Not applicable - This is a static documentation repository

**Secrets location:**
- Not applicable - No runtime configuration in this repository

## Webhooks & Callbacks

**Incoming:**
- Not applicable - This is a documentation repository

**Outgoing:**
- Not applicable - This is a static documentation repository

---

*Integration audit: 2026-03-30*