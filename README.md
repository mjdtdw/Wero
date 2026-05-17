# Wero

Wero is a personal markdown knowledge base for modernist cooking research.

The repository is designed for a workflow where the user collects source material as markdown, and an LLM agent turns that material into a structured, source-traceable wiki. The wiki is meant to be maintained mostly by the agent: source summaries, concept articles, backlinks, indexes, health checks, and durable research outputs all live as plain files.

This is not a public product, multi-user app, or polished frontend. It is a local research workspace for building a useful modernist cooking episteme over time.

## Core Idea

The workflow is intentionally file-first:

1. Add converted markdown sources and manual notes.
2. Let the agent summarize raw sources.
3. Let the agent compile source material into wiki articles.
4. Maintain indexes and backlinks so future sessions can navigate quickly.
5. Ask questions and save useful outputs.
6. File durable findings back into the wiki.
7. Run health checks to find weak evidence, stale links, missing summaries, and candidate new articles.

The important distinction is evidence versus synthesis. Raw sources are the evidence layer. Wiki articles are the compiled knowledge layer. Outputs are exploratory artifacts that can later be promoted into the wiki.

## Knowledge Model

Wero uses a small FPF-inspired model:

- **Evidence layer:** raw markdown sources and manual notes.
- **Episteme layer:** compiled wiki articles maintained by the agent.
- **Holons:** every source, summary, article, output, and index should be useful alone and as part of the larger system.
- **Transformer:** the LLM agent turns sources into summaries, articles, indexes, audits, and outputs.
- **Evidence graph:** important claims should point back to source summaries or raw source paths where practical.
- **Evolution loop:** ingest, compile, query, file, audit, refine.

## Repository Shape

The planned knowledge workspace has six durable areas:

- a raw evidence area for converted sources and manual notes,
- a source-summary area for one compact summary per processed source,
- a compiled wiki area for modernist cooking knowledge,
- an index area for navigation, backlinks, open questions, and future-agent orientation,
- an output area for research answers, comparisons, briefs, and recipe-development notes,
- a health area for audit reports and improvement suggestions.

The current repo includes GSD planning artifacts and an agent contract. The concrete folder scaffold is planned in Phase 1.

## How To Use

For a fresh source:

1. Convert the source to markdown yourself.
2. Put it in the raw source inbox once Phase 1 has created the knowledge structure.
3. Ask the agent to process the inbox.
4. The agent should create or update:
   - a source inventory entry,
   - a source summary,
   - relevant wiki articles,
   - relevant indexes and backlinks,
   - open questions when evidence is incomplete.

For a research question:

1. Ask the agent to answer against the wiki and indexes.
2. Save the answer as a markdown output when it is useful.
3. Promote durable findings into wiki articles only when they become stable knowledge.

For maintenance:

1. Ask the agent to run a health check.
2. Review the health report.
3. Let the agent fix missing summaries, stale indexes, weakly sourced claims, duplicate concepts, and candidate article gaps.

## Agent Rules

The agent should follow these project rules:

- Do not rewrite raw sources during compile passes unless explicitly asked.
- Write compiled knowledge into the wiki layer.
- Keep source summaries separate from wiki articles.
- Cite source summaries or raw paths for important culinary claims where practical.
- Treat safety-sensitive cooking guidance with extra caution.
- Update indexes after creating, renaming, or materially changing articles.
- Track open questions instead of inventing certainty.

The full operating contract is in the project agent guide.

## Roadmap

The planned v1 has five phases:

1. **Knowledge Base Scaffold** - create the filesystem, agent contract, and orientation files.
2. **Source Summaries and Wiki Templates** - define source and article formats, then prove the compile path.
3. **Index and Backlink Maintenance** - make the knowledge base navigable.
4. **Health Checks and Audit Reports** - add integrity checks and improvement reports.
5. **Outputs and Filing Workflow** - make Q&A and research outputs accumulate back into the base.

Planning details live in the GSD artifacts.

## Current Status

Project planning is complete. The repo currently has:

- project context,
- workflow configuration,
- research notes,
- v1 requirements,
- a five-phase roadmap,
- an agent operating contract.

The next build step is Phase 1: create the knowledge base scaffold.

## Working With GSD

Recommended next commands:

```text
$gsd-discuss-phase 1
$gsd-plan-phase 1
```

Use discussion when the phase needs more context. Use direct planning when the desired implementation is already clear.
