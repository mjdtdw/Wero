# Modernist Cooking Knowledge Base

## What This Is

A personal markdown knowledge base for modernist cooking research. The user collects source material and manual notes as markdown in `raw/`, and the LLM agent compiles that material into a structured wiki with summaries, concept articles, backlinks, indexes, and source traceability.

This is not a multi-user product or polished application. It is a local, agent-maintained research workspace where the wiki is primarily written and maintained by the LLM, while the user can read or edit files whenever useful.

## Core Value

Turn collected cooking sources and notes into a coherent, source-traceable modernist cooking wiki that gets more useful after every ingest and refinement pass.

## Requirements

### Validated

(None yet - ship to validate)

### Active

- [ ] User can place converted markdown sources and manual notes into a raw source area.
- [ ] Agent can summarize every raw source and track whether it has been processed.
- [ ] Agent can compile source material into readable wiki articles about modernist cooking topics.
- [ ] Wiki articles can link to related concepts, source summaries, techniques, ingredients, tools, and outputs.
- [ ] Important claims in wiki articles can point back to raw source material where practical.
- [ ] Agent can maintain indexes that help future agents quickly understand the knowledge base.
- [ ] Agent can run health checks to find gaps, inconsistencies, weakly sourced claims, and candidate new articles.
- [ ] Agent can produce markdown-based outputs, such as research notes, comparison tables, recipes, technique briefs, and future slide-style documents, then file useful outputs back into the wiki.

### Out of Scope

- Multi-user collaboration - this is exclusively for the user's own research workflow.
- Polished product UI - Codex and ordinary file browsing are enough for v1.
- Source conversion automation - the user can convert PDFs, web pages, images, and other inputs into markdown manually before ingest.
- Editor agnosticism - Obsidian may be useful, but v1 does not need to support multiple frontends or generic vault compatibility.
- Fancy RAG or vector infrastructure - small-scale markdown indexes and agent-readable summaries are the first bet.
- Fine-tuning or synthetic data pipelines - interesting future direction, but not part of initial scope.

## Context

The motivating idea is that modern LLMs can maintain small-to-medium personal knowledge bases directly as markdown. Instead of treating the LLM only as a coding assistant, the user wants to use it as a knowledge compiler: ingesting raw sources, maintaining a wiki, answering questions against that wiki, generating derived artifacts, and filing useful outputs back into the system.

The initial domain is modernist cooking. Likely knowledge areas include techniques, ingredient functions, equipment, hydrocolloids, emulsions, gels, foams, sous-vide, fermentation, texture modification, plating, recipe development, safety constraints, and comparisons between traditional and modernist approaches.

FPF framing:

- `raw/` is the evidence layer: source documents and manual notes.
- `wiki/` is the evolving episteme: agent-authored knowledge artifacts.
- Each source, concept article, recipe note, and output is a holon: useful alone and as part of the larger system.
- The LLM agent is a transformer: it turns raw inputs into summaries, concepts, indexes, audits, and outputs.
- Source links form an evidence graph, allowing important claims to be traced back to raw material.
- The operating loop is observe -> refine -> deploy -> audit: ingest sources, compile wiki, use it for questions, file outputs, then audit and improve.

## Constraints

- **Audience**: Single-user only - optimize for the user's own cooking research and agent workflow.
- **Input format**: Markdown-first - the user can handle conversion before ingest.
- **Storage**: Local filesystem - plain files and folders should remain readable and editable.
- **Authority model**: Agent-writable - the LLM may directly update the wiki without a review workflow.
- **Frontend**: Minimal - no dedicated UI is required for v1.
- **Scale**: Small-to-medium corpus - avoid infrastructure that only pays off at large scale.
- **Traceability**: Source links matter - important claims should preserve provenance where practical.

## Key Decisions

| Decision | Rationale | Outcome |
|----------|-----------|---------|
| Build a personal tool rather than a public product | The immediate value is in the user's own research workflow, not packaging for others | - Pending |
| Focus v1 on building the knowledge base | A coherent base is the foundation for later Q&A, outputs, and health checks | - Pending |
| Use markdown as the primary substrate | It is easy for the user and agents to read, write, diff, and reorganize | - Pending |
| Let the agent write wiki files directly | The wiki is intended to be the agent's working domain, with the user intervening only when desired | - Pending |
| Start with modernist cooking | Gives the project a concrete domain for folder conventions, article types, and validation examples | - Pending |
| Defer source conversion | The user can already convert sources to markdown; v1 should focus on compilation and maintenance | - Pending |

## Evolution

This document evolves at phase transitions and milestone boundaries.

**After each phase transition** (via `$gsd-transition`):
1. Requirements invalidated? -> Move to Out of Scope with reason
2. Requirements validated? -> Move to Validated with phase reference
3. New requirements emerged? -> Add to Active
4. Decisions to log? -> Add to Key Decisions
5. "What This Is" still accurate? -> Update if drifted

**After each milestone** (via `$gsd-complete-milestone`):
1. Full review of all sections
2. Core Value check - still the right priority?
3. Audit Out of Scope - reasons still valid?
4. Update Context with current state

---
*Last updated: 2026-05-17 after initialization*
