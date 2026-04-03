# Codebase Structure

**Analysis Date:** 2026-03-30

## Directory Layout

```
system_prompts_leaks/
├── readme.md               # Main entry point with project overview
├── .github/                # GitHub-specific files (FUNDING.yml)
├── .planning/              # GSD planning artifacts
│   └── codebase/           # Architecture and integration analysis
├── Anthropic/              # Anthropic AI model system prompts
├── Google/                 # Google AI model system prompts  
├── OpenAI/                 # OpenAI model system prompts
├── xAI/                    # xAI model system prompts
├── Perplexity/             # Perplexity AI system prompts
├── Misc/                   # Miscellaneous system prompts from other sources
```

## Directory Purposes

**Anthropic/:**
- Purpose: Stores all system prompts related to Anthropic's AI models
- Contains: Claude Sonnet, Opus, Haiku system prompts, API instructions, computer use prompts
- Key files: `claude-sonnet-4.6.md`, `claude-opus-4.6.md`, `claude.html`, raw prompts in `/raw`

**OpenAI/:**
- Purpose: Stores all system prompts related to OpenAI's GPT models
- Contains: GPT-4, GPT-4o, GPT-5, o3, o4-mini system prompts and tools specifications
- Key files: `GPT-4o.md`, `gpt-5.1-default.md`, `gpt-5.4-thinking.md`, API documentation in `/API`

**Google/:**
- Purpose: Stores all system prompts related to Google's AI models
- Contains: Gemini series system prompts and interface instructions
- Key files: `gemini-2.5-pro.md`, `gemini-2.5-flash.md`, `notebooklm-chat.md`

**xAI/:**
- Purpose: Stores all system prompts related to xAI's models
- Contains: Grok series system prompts
- Key files: `grok-3.md`, `grok-4.md`, `grok-comet.md`

**Perplexity/:**
- Purpose: Stores all system prompts related to Perplexity AI models
- Contains: Comet, Voice Assistant, and other PPLX model prompts
- Key files: Various Perplexity system prompt variations

## Key File Locations

**Entry Points:**
- `readme.md`: Main repository introduction and navigation

**Configuration:**
- `.github/FUNDING.yml`: Funding information
- `.planning/codebase/`: Architecture analysis and planning docs

**Core Content:**
- `Anthropic/claude.html`: HTML rendering of Claude prompt information
- `Anthropic/claude-sonnet-4.6.md`: Latest Claude Sonnet system prompt
- `OpenAI/GPT-4o.md`: GPT-4o system prompt with tools specification

## Naming Conventions

**Files:**
- Model-centric: `model-name-version.md` (e.g., `gpt-5.1-default.md`)
- Feature-specific: `feature-description.md` (e.g., `chatgpt-atlas.md`)
- API-specific: `model-generation-api.md` (e.g., `gpt-5.3-chat-api.md`)

**Directories:**
- Company name: Capitalized vendor names (e.g., `OpenAI/`, `Anthropic/`, `Google/`)

## Where to Add New Content

**New AI Model System Prompt:**
- Primary location: Create in respective company directory (e.g., `OpenAI/new-model.md` for new OpenAI models)
- Tests: There are no automated tests for static markdown content
- Documentation: Add alongside existing prompts for that model

**New Company Section:**
- Implementation: Create new capitalized directory (e.g., `Mistral/`, `Cohere/`)
- Examples to follow: Follow Anthropic or OpenAI structure for organizing their prompts

## Special Directories

**API Subdirectories:**
- Purpose: Some major vendors like OpenAI have dedicated API directories containing platform-specific prompt versions
- Generated: No
- Committed: Yes

**Old Subdirectories:**
- Purpose: History and evolution tracking of prompts over time
- Generated: No  
- Committed: Yes

**Raw Subdirectories:**
- Purpose: Raw, less processed versions of prompts (especially in Anthropic section)
- Generated: No
- Committed: Yes

---

*Structure analysis: 2026-03-30*