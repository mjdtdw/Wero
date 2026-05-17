# Stack Research

**Domain:** Personal LLM-maintained modernist cooking knowledge base
**Researched:** 2026-05-17
**Confidence:** MEDIUM

## Recommended Stack

### Core Technologies

| Technology | Version | Purpose | Why Recommended |
|------------|---------|---------|-----------------|
| Markdown files | CommonMark-style | Primary knowledge substrate | Easy for user and LLM agent to read, write, diff, link, and reorganize |
| Git | Current local install | Version history for agent-written knowledge | Gives rollback, audit trail, and review of large wiki changes |
| AGENTS.md | Project-local | Agent operating contract | Keeps compile, citation, naming, and health-check rules visible to future sessions |
| PowerShell scripts | Built-in on Windows | Optional local automation | Fits the current workspace without adding runtime friction |
| Python | 3.13 available locally | Optional indexes, audits, reports, plots | Best lightweight tool for text processing, CSV/JSON, matplotlib outputs, and future simple search |

### Supporting Libraries

| Library | Version | Purpose | When to Use |
|---------|---------|---------|-------------|
| PyYAML | Optional | Parse markdown frontmatter | If article metadata becomes structured |
| markdown-it-py or Python-Markdown | Optional | Markdown parsing/rendering | If health checks need structured markdown parsing |
| networkx | Optional | Knowledge graph analysis | If backlinks/concept links need graph checks |
| matplotlib | Optional | Visual outputs | For derived charts, diagrams, and cooking comparisons |

### Development Tools

| Tool | Purpose | Notes |
|------|---------|-------|
| ripgrep | Fast text search | Useful for agent navigation and health checks |
| git diff/status | Change inspection | Required before and after agent compile passes |
| pytest | Script verification | Use once scripts exist |

## Alternatives Considered

| Recommended | Alternative | When to Use Alternative |
|-------------|-------------|-------------------------|
| Plain markdown folders | Database-backed app | Only if file scale or query needs outgrow agent-readable indexes |
| Agent-maintained indexes | Vector database/RAG | Only after markdown indexes fail for the actual corpus |
| Python scripts | Node/TypeScript CLI | If the repo later becomes a richer app or web UI |
| AGENTS.md contract | Hardcoded workflow engine | If repeated manual agent instructions become brittle |

## What NOT to Use

| Avoid | Why | Use Instead |
|-------|-----|-------------|
| Early vector database | Adds infrastructure before proving need | Source summaries, indexes, backlinks, and search |
| Polished UI first | Does not serve the current core value | Plain files plus Codex workflow |
| Unstructured wiki writes | Agent output becomes hard to audit | File conventions, indexes, and source traceability |
| Claim-only articles | Cooking knowledge needs provenance and safety context | Article sections with sources and confidence notes |

## Stack Patterns by Variant

**If the base stays small:**
- Use pure markdown and AGENTS.md rules.
- Because the agent can read indexes and key files directly.

**If the base reaches hundreds of articles:**
- Add generated index files and optional Python health scripts.
- Because future sessions need quick orientation and integrity checks.

**If Q&A becomes central later:**
- Add a small search CLI over markdown before RAG.
- Because local lexical search plus curated indexes may be enough at this scale.

## Sources

- Project context in `.planning/PROJECT.md`
- FPF framing from user request and loaded `fpf` skill terminology
- Inference from current workspace constraints and available tooling

---
*Stack research for: personal modernist cooking knowledge base*
*Researched: 2026-05-17*
