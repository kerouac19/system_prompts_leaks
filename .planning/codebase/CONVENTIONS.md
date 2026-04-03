# Coding Conventions

**Analysis Date:** 2026-03-30

## File Organization

**Directory Structure:**
- By platform/provider: `OpenAI/`, `Google/`, `Anthropic/`, `Perplexity/`, `xAI/`, `Misc/`
- Markdown files grouped under their respective providers

**File Naming:**
- Uses descriptive names that clearly identify the specific model/features referenced
- Examples: `GPT-4o.md`, `gemini-3.1-pro.md`, `claude.html`
- Specific model variants clearly indicated in filename

## Documentation Standards

**Markdown Format:**
- Uses standard Markdown syntax extensively
- Headers marked with `#`, `##`, `###` etc.
- Code blocks properly formatted with backticks
- Inline formatting for emphasis: bold (**text**) and italic (*text*)

**Content Organization:**
- Clear hierarchical structure with well-defined sections
- Horizontal rules (`---`) used to separate major sections
- Proper use of numbered and bulleted lists
- Complex tool definitions contained within code blocks with JSON syntax

## Text Formatting

**Headers:**
- Consistent header hierarchy maintained throughout
- Section titles are descriptive and self-explanatory

**Code Blocks:**
- Uses proper language identifiers: `json`, `javascript`, `python`, etc.
- Complex schema definitions formatted with proper indentation

**Inline Formatting:**
- LaTeX formatted with `$` and `$$` delimiters for mathematical expressions
- Proper use of blockquotes with `>`
- Links formatted according to Markdown specification

## Metadata and Constants

**Date References:**
- Dates consistently formatted (e.g., "Current date: 2026-02-04")
- Time references in standardized formats

**Variable Placeholders:**
- Uses consistent placeholder formatting: `<placeholder>`
- Templates defined with schema structures

## Style Consistency

**Terminology:**
- Technical terminology used consistently across files
- Model names capitalized and formatted consistently
- Tool names properly referenced throughout

**Capitalization:**
- Proper nouns capitalized: "OpenAI", "GPT-4o", "WebP", "SVG"
- Acronyms handled appropriately: "LaTeX", "UI", "API"

## Document Structure

**Content Sections:**
- System identification at the beginning of documents
- Clear definition of capabilities and constraints
- Tool definitions grouped logically, often with JSON schemas
- Guidelines and limitations sectioned separately

**Visual Elements:**
- Proper spacing between sections
- Consistent indentation for nested content
- Horizontal separators for logical grouping

## Quality Guidelines

**Completeness:**
- Comprehensive coverage of functionality per file
- Detailed descriptions of features and limitations
- Explicit guardrails and constraints defined

**Clarity:**
- Clear, readable English text
- Logical organization of related concepts
- Step-by-step instructions with proper ordering