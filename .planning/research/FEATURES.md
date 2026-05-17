# Feature Research

**Domain:** Personal LLM-maintained modernist cooking knowledge base
**Researched:** 2026-05-17
**Confidence:** MEDIUM

## Feature Landscape

### Table Stakes

| Feature | Why Expected | Complexity | Notes |
|---------|--------------|------------|-------|
| Raw source area | User needs a simple drop zone for converted markdown and notes | LOW | Start with `knowledge/raw/` or similar |
| Source processing status | Agent needs to know what has been compiled | MEDIUM | Can be an index file, frontmatter, or both |
| Source summaries | Future sessions need fast orientation | LOW | One summary per source, with important concepts |
| Wiki article structure | Agent output needs consistency | MEDIUM | Templates for concept, technique, ingredient, equipment, recipe note |
| Backlinks and related links | Knowledge needs to connect across concepts | MEDIUM | Maintain explicit "Related" sections |
| Master indexes | Small-scale alternative to RAG | MEDIUM | Concepts, sources, techniques, ingredients, equipment, outputs |
| Source traceability | Claims should point back to raw evidence where practical | MEDIUM | Use source references by path and section/quote when possible |
| Health checks | Agent needs to improve integrity over time | MEDIUM | Gaps, dead links, unsourced claims, duplicate concepts |

### Differentiators

| Feature | Value Proposition | Complexity | Notes |
|---------|-------------------|------------|-------|
| Cooking-specific taxonomy | Makes the base useful for modernist cooking, not generic notes | MEDIUM | Techniques, functions, ingredients, ratios, temperatures, tools, safety |
| Compile passes | Turns raw material into a coherent wiki | MEDIUM | Agent workflow can be documented before scripting |
| Filed outputs | Q&A and research outputs improve the base | MEDIUM | Save useful answers to `outputs/` or promote into `wiki/` |
| Evidence/confidence notes | Separates source-backed facts from agent synthesis | MEDIUM | Especially important for safety, temperatures, and substitutions |
| Candidate article generation | Finds missing concepts from raw sources | MEDIUM | Health check can propose next wiki articles |

### Anti-Features

| Feature | Why Requested | Why Problematic | Alternative |
|---------|---------------|-----------------|-------------|
| Full UI | Feels like a product | Distracts from the personal workflow | File conventions and AGENTS.md first |
| Automatic source conversion | Seems convenient | User already handles conversion; high edge-case cost | Accept markdown sources only |
| Perfect citation granularity | Desirable for rigor | Expensive before the workflow proves itself | Practical path/section references in v1 |
| Fine-tuning | Attractive long-term | Premature and not needed for a local corpus | Agent-readable indexes and summaries |

## Feature Dependencies

```text
Folder conventions
  -> Source inventory
    -> Source summaries
      -> Wiki compile
        -> Backlinks and indexes
          -> Health checks
            -> Filed outputs and refinements
```

### MVP Definition

### Launch With (v1)

- [ ] Folder structure for raw sources, wiki articles, indexes, and outputs.
- [ ] AGENTS.md with compile rules, source traceability rules, and health-check rules.
- [ ] Initial modernist cooking taxonomy and article templates.
- [ ] Source inventory format that tracks processing state.
- [ ] First compile workflow that transforms raw markdown into source summaries and wiki articles.

### Add After Validation (v1.x)

- [ ] Health-check script or checklist for dead links, unsourced claims, and missing summaries.
- [ ] Generated concept map or backlink report.
- [ ] Simple search CLI for the wiki and source summaries.
- [ ] Output filing workflow for Q&A and research artifacts.

### Future Consideration (v2+)

- [ ] Lightweight local web UI.
- [ ] RAG/vector search.
- [ ] Synthetic data generation.
- [ ] Fine-tuning experiments.

## Feature Prioritization Matrix

| Feature | User Value | Implementation Cost | Priority |
|---------|------------|---------------------|----------|
| Folder conventions | HIGH | LOW | P1 |
| AGENTS.md workflow rules | HIGH | LOW | P1 |
| Source inventory | HIGH | MEDIUM | P1 |
| Source summaries | HIGH | LOW | P1 |
| Wiki article templates | HIGH | LOW | P1 |
| Traceability conventions | HIGH | MEDIUM | P1 |
| Health checks | MEDIUM | MEDIUM | P2 |
| Search CLI | MEDIUM | MEDIUM | P2 |
| Visual outputs | MEDIUM | MEDIUM | P3 |

## Sources

- Project context in `.planning/PROJECT.md`
- User-stated desired workflow and constraints
- FPF evidence graph and episteme framing

---
*Feature research for: personal modernist cooking knowledge base*
*Researched: 2026-05-17*
