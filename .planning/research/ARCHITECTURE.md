# Architecture Research

**Domain:** Personal LLM-maintained modernist cooking knowledge base
**Researched:** 2026-05-17
**Confidence:** MEDIUM

## Standard Architecture

### System Overview

```text
User-converted markdown sources
        |
        v
knowledge/raw/
        |
        v
Agent compile workflow
        |
        +--> knowledge/indexes/     source inventory, concept map, article index
        +--> knowledge/wiki/        concept, technique, ingredient, equipment articles
        +--> knowledge/outputs/     research answers, tables, briefs, future slides
        |
        v
Agent health workflow
        |
        +--> gap reports, dead-link checks, weak evidence notes, article candidates
```

### Component Responsibilities

| Component | Responsibility | Typical Implementation |
|-----------|----------------|------------------------|
| `knowledge/raw/` | Stores converted source markdown and manual notes | User-managed files, stable paths |
| `knowledge/sources/` | Stores per-source summaries and extraction notes | Agent-written markdown |
| `knowledge/wiki/` | Stores compiled knowledge articles | Agent-written markdown with related links |
| `knowledge/indexes/` | Gives future agents fast orientation | Agent-maintained index markdown or JSON |
| `knowledge/outputs/` | Stores derived answers and artifacts | Agent-written markdown, tables, later charts/slides |
| `AGENTS.md` | Defines operating rules | Project-local agent contract |
| `scripts/` | Optional automation | Python/PowerShell scripts added only when repeated tasks emerge |

## Recommended Project Structure

```text
AGENTS.md
README.md
knowledge/
  raw/
    inbox/
    processed/
  sources/
  wiki/
    concepts/
    techniques/
    ingredients/
    equipment/
    recipes/
    safety/
  indexes/
    README.md
    sources.md
    concepts.md
    backlinks.md
    open-questions.md
  outputs/
    research-notes/
    comparisons/
    briefs/
  health/
    reports/
scripts/
```

### Structure Rationale

- **`raw/`:** preserves the evidence layer; source files should not be silently rewritten by compile passes.
- **`sources/`:** gives one concise orientation artifact per raw document.
- **`wiki/`:** separates compiled episteme from raw evidence.
- **`indexes/`:** substitutes for heavier retrieval infrastructure at the initial scale.
- **`outputs/`:** lets Q&A and explorations "add up" without immediately mixing them into canonical wiki articles.
- **`health/`:** preserves audit trail for cleanup passes and integrity checks.

## Architectural Patterns

### Pattern 1: Evidence-Preserving Compile

**What:** Raw files remain source-of-truth evidence; compiled wiki articles cite them rather than replacing them.
**When to use:** Always for ingest and compile.
**Trade-offs:** More files and references, but much better auditability.

### Pattern 2: Agent-Readable Indexes

**What:** Maintain small markdown indexes that summarize what exists and where to look.
**When to use:** Before adding RAG or databases.
**Trade-offs:** Indexes can go stale, so health checks must verify them.

### Pattern 3: Promote Outputs Deliberately

**What:** Save Q&A outputs first, then promote durable findings into wiki articles when useful.
**When to use:** For exploratory research.
**Trade-offs:** Avoids polluting canonical wiki pages, but requires periodic filing.

## Data Flow

1. **Ingest:** User adds converted markdown to `knowledge/raw/inbox/`.
2. **Inventory:** Agent records source path, title, type, status, and suspected topics in `knowledge/indexes/sources.md`.
3. **Summarize:** Agent writes a source summary in `knowledge/sources/`.
4. **Compile:** Agent creates or updates wiki articles with links to source summaries and raw sources.
5. **Index:** Agent updates concept, source, and backlink indexes.
6. **Use:** User asks questions; agent writes outputs.
7. **File:** Useful outputs are linked, summarized, or promoted into wiki.
8. **Audit:** Agent runs health checks and records reports.

## Anti-Patterns

### Anti-Pattern 1: Mixing Raw and Compiled Knowledge

**What people do:** Edit source notes into article form in place.
**Why it's wrong:** Provenance gets blurred; future agents cannot distinguish evidence from synthesis.
**Do this instead:** Keep raw sources immutable-ish and write compiled artifacts separately.

### Anti-Pattern 2: Creating Too Many Article Types

**What people do:** Invent a folder/type for every nuance.
**Why it's wrong:** Agents spend more effort classifying than compiling.
**Do this instead:** Start with a small taxonomy and expand only when repeated pressure appears.

### Anti-Pattern 3: Unsourced Culinary Advice

**What people do:** Let the agent invent confident cooking guidance.
**Why it's wrong:** Modernist cooking involves temperatures, additives, ratios, and safety.
**Do this instead:** Mark unsupported synthesis and cite raw sources for important claims.

## Sources

- `.planning/PROJECT.md`
- `.planning/research/FEATURES.md`
- FPF concepts: evidence graph, episteme, holon, transformer, evolution loop

---
*Architecture research for: personal modernist cooking knowledge base*
*Researched: 2026-05-17*
