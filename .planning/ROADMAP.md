# Roadmap: Modernist Cooking Knowledge Base

**Created:** 2026-05-17
**Granularity:** Standard
**Execution:** Sequential
**Requirements covered:** 21 / 21

## Phase Overview

| # | Phase | Goal | Requirements | UI hint |
|---|-------|------|--------------|---------|
| 1 | Knowledge Base Scaffold | Establish the filesystem, agent contract, and initial orientation files for the knowledge base | SCF-01, SCF-02, SCF-03, SRC-01, SRC-04, IDX-01 | no |
| 2 | Source Summaries and Wiki Templates | Define source summary and wiki article formats, then prove the compile path on seed modernist cooking content | SRC-02, SRC-03, WIKI-01, WIKI-02, WIKI-03 | no |
| 3 | Index and Backlink Maintenance | Make the knowledge base navigable through maintained source, concept, article, backlink, and question indexes | WIKI-04, IDX-02, IDX-03, IDX-04 | no |
| 4 | Health Checks and Audit Reports | Add an agent workflow for finding integrity problems and proposing improvements | HLT-01, HLT-02, HLT-03 | no |
| 5 | Outputs and Filing Workflow | Let Q&A and research outputs become durable artifacts without polluting canonical wiki pages | OUT-01, OUT-02, OUT-03 | no |

## Phase Details

### Phase 1: Knowledge Base Scaffold

**Goal:** Establish a clean local structure and operating contract so future agent sessions know how to work safely in the knowledge base.

**Requirements:** SCF-01, SCF-02, SCF-03, SRC-01, SRC-04, IDX-01

**Success criteria:**
1. `knowledge/` exists with raw, sources, wiki, indexes, outputs, and health areas.
2. `AGENTS.md` defines source handling, compile rules, evidence rules, index rules, and health-check rules.
3. Root README explains the purpose of the project and the basic source-ingest workflow.
4. Raw source files are explicitly treated as evidence files that compile passes do not rewrite.
5. `knowledge/indexes/README.md` tells future sessions what to read first.

**Notes:**
- Keep the taxonomy small: concepts, techniques, ingredients, equipment, recipes, safety.
- This phase prevents provenance loss before the first compile pass.

### Phase 2: Source Summaries and Wiki Templates

**Goal:** Create repeatable formats for source summaries and wiki articles, then validate them with initial modernist cooking material.

**Requirements:** SRC-02, SRC-03, WIKI-01, WIKI-02, WIKI-03

**Success criteria:**
1. Source inventory format records path, title, type, status, related topics, and summary path.
2. Source summaries include key ideas, useful facts, modernist cooking concepts, and source references.
3. Wiki templates exist for concepts, techniques, ingredients, equipment, recipes, and safety topics.
4. At least one seed compile pass produces source summaries and wiki articles from markdown input.
5. Important culinary claims in generated articles include practical source references where possible.

**Notes:**
- Safety-sensitive claims need source links and confidence/caution notes.
- Templates should distinguish evidence, synthesis, practical use, and open questions.

### Phase 3: Index and Backlink Maintenance

**Goal:** Keep the wiki navigable as the corpus grows.

**Requirements:** WIKI-04, IDX-02, IDX-03, IDX-04

**Success criteria:**
1. Source, concept, article, and backlink indexes exist as markdown files.
2. Wiki articles include related links to other articles and source summaries.
3. Compile workflow instructions require updating indexes after article changes.
4. Open questions and candidate article gaps are tracked in an index.
5. A future agent can orient itself from indexes without reading the entire corpus.

**Notes:**
- This is the small-scale alternative to RAG for the first version.
- Indexes are useful only if updating them is part of the workflow.

### Phase 4: Health Checks and Audit Reports

**Goal:** Add a refinement loop that detects decay, inconsistencies, missing evidence, and candidate improvements.

**Requirements:** HLT-01, HLT-02, HLT-03

**Success criteria:**
1. Health-check workflow describes checks for missing summaries, dead links, stale indexes, duplicate concepts, and weakly sourced claims.
2. Health reports can be written under `knowledge/health/reports/`.
3. Reports include severity, affected files, suggested fixes, and follow-up candidates.
4. Health checks can propose new wiki articles or source follow-ups.
5. The workflow preserves audit trail instead of silently rewriting everything.

**Notes:**
- Start with an agent checklist; add scripts only if repeated checks become tedious.

### Phase 5: Outputs and Filing Workflow

**Goal:** Make user queries and explorations accumulate into the knowledge base.

**Requirements:** OUT-01, OUT-02, OUT-03

**Success criteria:**
1. Output conventions exist for research answers, comparison tables, technique briefs, and recipe-development notes.
2. Outputs are saved separately from canonical wiki articles by default.
3. Filing rules explain when to link an output, summarize it, or promote durable findings into wiki articles.
4. Indexes can reference useful outputs.
5. A completed output can improve future questions without requiring the user to manually rewrite the wiki.

**Notes:**
- This phase turns exploration into durable episteme.

## Coverage Matrix

| Requirement | Phase | Status |
|-------------|-------|--------|
| SCF-01 | Phase 1 | Pending |
| SCF-02 | Phase 1 | Pending |
| SCF-03 | Phase 1 | Pending |
| SRC-01 | Phase 1 | Pending |
| SRC-04 | Phase 1 | Pending |
| IDX-01 | Phase 1 | Pending |
| SRC-02 | Phase 2 | Pending |
| SRC-03 | Phase 2 | Pending |
| WIKI-01 | Phase 2 | Pending |
| WIKI-02 | Phase 2 | Pending |
| WIKI-03 | Phase 2 | Pending |
| WIKI-04 | Phase 3 | Pending |
| IDX-02 | Phase 3 | Pending |
| IDX-03 | Phase 3 | Pending |
| IDX-04 | Phase 3 | Pending |
| HLT-01 | Phase 4 | Pending |
| HLT-02 | Phase 4 | Pending |
| HLT-03 | Phase 4 | Pending |
| OUT-01 | Phase 5 | Pending |
| OUT-02 | Phase 5 | Pending |
| OUT-03 | Phase 5 | Pending |

## Phase Ordering Rationale

1. Scaffold comes first because the agent needs clear boundaries before it writes the wiki.
2. Source summaries and templates come before indexes because there must be real content to index.
3. Index maintenance comes before health checks because many health checks validate index integrity.
4. Health checks come before outputs so output filing can reuse integrity conventions.
5. Outputs come last because they are most valuable once the base has a stable structure and indexes.

---
*Roadmap created: 2026-05-17*
