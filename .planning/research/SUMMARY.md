# Project Research Summary

**Project:** Modernist Cooking Knowledge Base
**Domain:** Personal LLM-maintained culinary knowledge base
**Researched:** 2026-05-17
**Confidence:** MEDIUM

## Executive Summary

The project should start as a plain-file knowledge workspace, not an application. The durable value comes from conventions: separating raw evidence from compiled wiki articles, preserving source traceability, maintaining agent-readable indexes, and defining repeatable compile and health-check workflows in AGENTS.md.

For v1, the strongest architecture is markdown-first and local-first. The user can handle source conversion manually, so the project should focus on the agent's job: summarize sources, compile modernist cooking concepts, maintain backlinks/indexes, and record health findings. Fancy retrieval, UI, and fine-tuning should wait until the markdown corpus itself proves the workflow.

The main risk is fluent but weakly sourced culinary synthesis. Modernist cooking includes safety-sensitive parameters, ingredient ratios, equipment constraints, and chemical/physical mechanisms. The wiki needs practical source references and confidence notes before it can become a trusted cooking/research tool.

## Key Findings

### Recommended Stack

Use plain markdown, git, AGENTS.md, and optional Python scripts. Markdown is the source and wiki substrate; git gives rollback and auditability; AGENTS.md gives future sessions a stable operating contract; Python can be added later for health checks, search, and visual outputs.

**Core technologies:**
- Markdown: primary knowledge files and wiki articles.
- Git: history and rollback for agent-authored changes.
- AGENTS.md: compile, citation, and health-check rules.
- Python: optional scripts for indexes, audits, search, and plots.

### Expected Features

**Must have:**
- Raw markdown source area.
- Source inventory and processing status.
- Per-source summaries.
- Wiki article templates for modernist cooking.
- Related links/backlinks and master indexes.
- Practical source traceability.

**Should have:**
- Health checks for dead links, missing summaries, weak evidence, and candidate articles.
- Output filing workflow for Q&A results and research briefs.
- Cooking-specific taxonomy for techniques, ingredients, equipment, recipes, and safety.

**Defer:**
- Dedicated UI.
- Automatic PDF/web/image conversion.
- RAG/vector database.
- Fine-tuning or synthetic data generation.

### Architecture Approach

The system should have an evidence layer (`knowledge/raw/`), a source-summary layer (`knowledge/sources/`), an episteme layer (`knowledge/wiki/`), an orientation layer (`knowledge/indexes/`), an output layer (`knowledge/outputs/`), and an audit layer (`knowledge/health/`). Compile and health workflows move knowledge through these layers without erasing provenance.

**Major components:**
1. `knowledge/raw/` - source evidence and manual notes.
2. `knowledge/sources/` - agent-written source summaries.
3. `knowledge/wiki/` - compiled modernist cooking knowledge.
4. `knowledge/indexes/` - agent-readable maps and inventories.
5. `knowledge/outputs/` - derived answers, comparisons, and briefs.
6. `AGENTS.md` - project-local operating contract.

### Critical Pitfalls

1. **Losing provenance** - require source references in templates.
2. **Indexes rot** - update indexes during every compile pass and later script checks.
3. **Taxonomy overgrowth** - start with a small folder model.
4. **Mixing recipes, techniques, and claims** - use distinct article templates.
5. **Unsafe agent guesses** - cite safety-sensitive claims and mark confidence.

## Implications for Roadmap

### Phase 1: Knowledge Base Scaffold
**Rationale:** The filesystem and agent contract must exist before sources can be compiled safely.
**Delivers:** Folder structure, AGENTS.md rules, initial indexes, source inventory format.
**Addresses:** Folder conventions, source area, operating rules.
**Avoids:** Taxonomy overgrowth and provenance loss.

### Phase 2: Source Compile Workflow
**Rationale:** The core value is converting raw markdown into useful wiki knowledge.
**Delivers:** Source summaries, article templates, first compile pass on seed modernist cooking material.
**Addresses:** Source summaries, wiki articles, source traceability.
**Avoids:** Unsourced culinary claims and article-type confusion.

### Phase 3: Indexing and Backlink Maintenance
**Rationale:** The base needs to stay navigable as it grows.
**Delivers:** Concept/source/backlink indexes and update rules.
**Addresses:** Master indexes, related links, future-agent orientation.
**Avoids:** Index rot.

### Phase 4: Health Checks and Refinement Loop
**Rationale:** Quality improves through audit passes, not one-time generation.
**Delivers:** Health check workflow for gaps, dead links, weak sources, duplicate concepts, and article candidates.
**Addresses:** Integrity checks and incremental improvement.
**Avoids:** Silent quality decay.

### Phase 5: Outputs and Filing Workflow
**Rationale:** User queries should produce durable artifacts that can improve the wiki.
**Delivers:** Markdown output conventions, comparison/brief templates, filing rules.
**Addresses:** Q&A outputs and cumulative exploration.

### Research Flags

- **Phase 2:** May need deeper domain research when defining modernist cooking article templates.
- **Phase 4:** May need script design if manual health checks become repetitive.
- **Phase 5:** May need output format decisions if slide/plot outputs become important.

## Confidence Assessment

| Area | Confidence | Notes |
|------|------------|-------|
| Stack | MEDIUM | Based on project constraints and existing local tooling |
| Features | MEDIUM | Directly grounded in user-stated workflow |
| Architecture | MEDIUM | Strong fit for markdown-first agent workflow |
| Pitfalls | MEDIUM | Inferred from knowledge-base and culinary-domain risks |

**Overall confidence:** MEDIUM

### Gaps to Address

- First seed sources are not known yet; Phase 2 should adapt templates after seeing real modernist cooking material.
- Citation granularity should be validated in practice; v1 should start practical rather than perfect.
- Script needs should emerge from repeated manual work, not be assumed upfront.

## Sources

### Primary

- `.planning/PROJECT.md` - project context and constraints.
- User conversation - desired workflow and scope.

### Secondary

- FPF skill terminology - evidence graph, episteme, holon, transformer, evolution loop.

---
*Research completed: 2026-05-17*
*Ready for roadmap: yes*
