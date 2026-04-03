# Architecture

**Analysis Date:** 2026-03-30

## Pattern Overview

**Overall:** Static content documentation structure

**Key Characteristics:**
- Organizes leaked system prompts by AI provider company
- Centralized repository for AI system prompt information
- Hierarchical organization by model/version
- Documentation-focused, no runtime application

## Layers

**Content Layer:**
- Purpose: Stores the actual leaked system prompts and AI instructions
- Location: `[Anthropic/, OpenAI/, Google/, xAI/, Perplexity/, Misc/]`
- Contains: Markdown files containing actual system prompts from various AI models
- Depends on: None (leaf layer with raw content)
- Used by: Researchers studying AI system prompts and safety mechanisms

## Data Flow

**Research/Documentation Flow:**

1. New leaked prompts discovered in public
2. System prompts added to respective company directories as individual markdown files
3. Updates applied to maintain current state of known prompts
4. Researchers access and study documentation for insights/analysis

**Content Organization Approach:**
- Each AI provider gets its own dedicated directory
- Individual system prompts stored as separate markdown files
- Historical versions preserved when available (e.g., `Old/` directory in OpenAI)

## Key Abstractions

**Company-Based Organization:**
- Purpose: Groups system prompts by AI development company
- Examples: `Anthropic/`, `OpenAI/`, `Google/`, `xAI/`, `Perplexity/`
- Pattern: Standardized directory grouping across all vendors

**Model-Specific Prompts:**
- Purpose: Separates system prompts by specific AI model version or type
- Examples: `GPT-4o.md`, `claude-sonnet-4.6.md`, `gemini-2.5-pro.md`
- Pattern: Individual files with descriptive names for different models

## Entry Points

**Repository Root:**
- Location: `[readme.md]`
- Triggers: Initial discovery/access of the repository
- Responsibilities: Provides overview and link to main content sections

## Error Handling

**Strategy:** N/A - Static documentation repository without runtime functionality

## Cross-Cutting Concerns

**Logging:** N/A - Static files without operational logging
**Validation:** Minimal - Just document integrity preservation
**Authentication:** N/A - Public static content, no access controls

---

*Architecture analysis: 2026-03-30*