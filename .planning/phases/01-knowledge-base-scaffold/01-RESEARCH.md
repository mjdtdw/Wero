# Phase 1: Knowledge Base Scaffold - Research

**Phase:** 1 - Knowledge Base Scaffold
**Researched:** 2026-05-17
**Status:** Complete

## Research Question

What needs to be known to plan a safe, source-traceable filesystem scaffold for the Modernist Cooking Knowledge Base?

## Inputs Reviewed

- `.planning/PROJECT.md`
- `.planning/REQUIREMENTS.md`
- `.planning/ROADMAP.md`
- `.planning/STATE.md`
- `.planning/phases/01-knowledge-base-scaffold/01-CONTEXT.md`
- `AGENTS.md`
- `README.md`
- FPF skill core terminology: Holon, Episteme, Evidence Graph, Strict Distinction, Ontological Parsimony, Canonical Evolution Loop

## Key Findings

### 1. The scaffold is the first safety boundary

Phase 1 is not just folder creation. It establishes the boundary that prevents future compile passes from mixing raw evidence with agent-authored synthesis.

Planning implication: the executor should create `knowledge/raw/README.md` and `knowledge/indexes/README.md` early, because these files carry the rule that raw source files are evidence and derived files belong elsewhere.

### 2. Use a full practical v1 scaffold, not a giant taxonomy

The user selected "create everything needed immediately." The useful scaffold is deeper than six top-level directories, but should still stop before Phase 2 templates and Phase 3 indexes.

Recommended scaffold:

```text
knowledge/
  raw/
    inbox/
  sources/
  wiki/
    concepts/
    techniques/
    ingredients/
    equipment/
    recipes/
    safety/
  indexes/
  outputs/
  health/
    reports/
```

Planning implication: create placeholder `.gitkeep` files only for otherwise-empty folders that need to be tracked. Use README files where the reader needs rules, not everywhere.

### 3. FPF maps cleanly onto the folder roles

- `knowledge/raw/` is the evidence layer.
- `knowledge/sources/` is a derived source-summary layer.
- `knowledge/wiki/` is the evolving episteme layer.
- `knowledge/indexes/` is the navigation and evidence-graph orientation layer.
- Each source, summary, article, output, and index is a holon: useful alone and as part of the larger knowledge system.
- Agent work should preserve Strict Distinction: raw sources are not summaries, summaries are not wiki articles, outputs are not canonical wiki pages until promoted.

Planning implication: Phase 1 docs should use these terms sparingly but concretely, so future sessions have a durable mental model without needing a heavy ontology.

### 4. Existing docs are reusable, not disposable

`AGENTS.md` already defines most operating rules. `README.md` already explains the project and workflow. The plan should refine these docs after creating the scaffold rather than replacing them wholesale.

Planning implication: tasks should update docs in place, preserving the current project framing while adding concrete paths that become true once `knowledge/` exists.

### 5. Verification is mostly structural plus textual

There is no application code to test. Verification should check:

- all required folders exist;
- raw inbox exists;
- wiki taxonomy folders exist;
- index entry point exists and tells future sessions what to read first;
- root README names the scaffold and source-ingest workflow;
- `AGENTS.md` keeps raw-source non-rewrite and source-traceability rules;
- no Phase 2 templates are overproduced.

## Risks and Mitigations

| Risk | Mitigation |
|------|------------|
| Overbuilding future phases | Create folders and orientation only; defer source-summary templates, article templates, health report formats, and output filing details. |
| Raw files later rewritten accidentally | Put explicit no-rewrite rules in `knowledge/raw/README.md`, `knowledge/indexes/README.md`, and `AGENTS.md`. |
| Index entry point claims nonexistent indexes exist | Phrase planned indexes as "coming in later phases" until they are created. |
| Empty folders disappear from git | Add `.gitkeep` in otherwise-empty directories. |
| Documentation drift | Update README after scaffold creation so the documented paths match the actual filesystem. |

## Recommended Plan Shape

Use one implementation plan in Wave 1:

1. Create the practical v1 `knowledge/` scaffold.
2. Add boundary/orientation docs for raw and indexes.
3. Add `.gitkeep` placeholders for empty tracked directories.
4. Update `AGENTS.md` and root `README.md` to reference the concrete scaffold.
5. Verify with PowerShell path checks and targeted text searches.

## FPF Assurance Notes

- **Evidence Graph:** Important future culinary claims must point to source summaries or raw paths. Phase 1 lays down the directories and rules for this graph.
- **Strict Distinction:** Raw evidence, source summaries, wiki synthesis, exploratory outputs, and health reports are separate roles. This distinction must be visible in docs and paths.
- **Ontological Parsimony:** Do not introduce database, vector store, UI, or automation scripts in Phase 1.
- **Canonical Evolution Loop:** The scaffold supports future observe -> refine -> deploy -> audit passes: ingest raw sources, compile summaries/wiki, use outputs, and audit health.

## RESEARCH COMPLETE

Phase 1 can be planned as a single focused scaffold/documentation plan.
