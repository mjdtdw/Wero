# Requirements: Modernist Cooking Knowledge Base

**Defined:** 2026-05-17
**Core Value:** Turn collected cooking sources and notes into a coherent, source-traceable modernist cooking wiki that gets more useful after every ingest and refinement pass.

## v1 Requirements

### Scaffold

- [ ] **SCF-01**: User has a `knowledge/` folder structure with separate areas for raw sources, source summaries, compiled wiki articles, indexes, outputs, and health reports.
- [ ] **SCF-02**: User has an `AGENTS.md` operating contract that explains how the agent ingests sources, compiles wiki articles, preserves evidence, updates indexes, and runs health checks.
- [ ] **SCF-03**: User has a root README that explains the knowledge base purpose and the basic workflow for adding converted markdown sources.

### Sources

- [ ] **SRC-01**: User can place converted markdown sources and manual notes into a raw source inbox without needing any conversion automation.
- [ ] **SRC-02**: Agent can maintain a source inventory that records each source path, title, type, processing status, related topics, and summary path.
- [ ] **SRC-03**: Agent can write a concise source summary for each processed raw source, including key ideas, modernist cooking concepts, useful facts, and source path.
- [ ] **SRC-04**: Agent can distinguish raw evidence files from compiled wiki files and avoid rewriting raw sources during compile passes.

### Wiki

- [ ] **WIKI-01**: Agent can create and update compiled wiki articles for modernist cooking concepts, techniques, ingredients, equipment, recipes, and safety topics.
- [ ] **WIKI-02**: Wiki articles follow templates that include overview, practical use, important parameters, evidence/source references, related links, and open questions.
- [ ] **WIKI-03**: Important culinary claims in wiki articles can reference source summaries or raw source paths where practical.
- [ ] **WIKI-04**: Wiki articles can link to related concepts so the knowledge base becomes navigable across topics.

### Indexes

- [ ] **IDX-01**: Agent can maintain an index entry point that tells future sessions what files to read first.
- [ ] **IDX-02**: Agent can maintain source, concept, article, and backlink indexes as markdown files.
- [ ] **IDX-03**: Agent can update indexes after compile passes so newly created or changed articles are discoverable.
- [ ] **IDX-04**: Agent can maintain an open-questions index for gaps, uncertainties, and candidate future research.

### Health

- [ ] **HLT-01**: Agent can run a health-check workflow that looks for missing source summaries, dead links, stale indexes, duplicate concepts, and weakly sourced claims.
- [ ] **HLT-02**: Agent can write health reports that list findings, severity, affected files, and suggested fixes.
- [ ] **HLT-03**: Agent can propose candidate new articles or source follow-ups discovered during health checks.

### Outputs

- [ ] **OUT-01**: Agent can write markdown outputs for research answers, comparison tables, technique briefs, and recipe-development notes.
- [ ] **OUT-02**: Agent can file useful outputs back into the knowledge base by linking them from indexes or promoting durable findings into wiki articles.
- [ ] **OUT-03**: Agent can keep exploratory outputs separate from canonical wiki articles until they are intentionally promoted.

## v2 Requirements

Deferred to future release. Tracked but not in current roadmap.

### Automation

- **AUTO-01**: Agent can run scripts that automatically validate links, source inventory consistency, and index coverage.
- **AUTO-02**: User has a simple search CLI over sources, summaries, wiki articles, and outputs.
- **AUTO-03**: Agent can generate visual outputs such as matplotlib charts or Marp slide decks.
- **AUTO-04**: Agent can build a graph view of source-to-concept and concept-to-concept links.

### Retrieval

- **RTR-01**: Knowledge base can use a lightweight local search index if markdown indexes stop being enough.
- **RTR-02**: Knowledge base can evaluate whether RAG/vector search is useful after the corpus grows.

### Advanced Learning

- **ADV-01**: User can experiment with synthetic data generation from the curated wiki.
- **ADV-02**: User can evaluate fine-tuning ideas after the knowledge base has stable, high-quality content.

## Out of Scope

Explicitly excluded. Documented to prevent scope creep.

| Feature | Reason |
|---------|--------|
| Multi-user collaboration | The tool is exclusively for the user's own workflow |
| Polished product UI | Plain files and Codex are enough for v1 |
| Automatic PDF/web/image conversion | User can convert sources to markdown manually |
| Frontend/editor agnosticism | No need to support multiple frontends in v1 |
| Vector database/RAG | Markdown indexes and summaries should be tested first |
| Fine-tuning pipeline | Premature before the wiki exists and proves useful |
| Fully automated food-safety authority | Safety-sensitive guidance needs sources and caution, not unsupported agent certainty |

## Traceability

Which phases cover which requirements. Updated during roadmap creation.

| Requirement | Phase | Status |
|-------------|-------|--------|
| SCF-01 | Unmapped | Pending |
| SCF-02 | Unmapped | Pending |
| SCF-03 | Unmapped | Pending |
| SRC-01 | Unmapped | Pending |
| SRC-02 | Unmapped | Pending |
| SRC-03 | Unmapped | Pending |
| SRC-04 | Unmapped | Pending |
| WIKI-01 | Unmapped | Pending |
| WIKI-02 | Unmapped | Pending |
| WIKI-03 | Unmapped | Pending |
| WIKI-04 | Unmapped | Pending |
| IDX-01 | Unmapped | Pending |
| IDX-02 | Unmapped | Pending |
| IDX-03 | Unmapped | Pending |
| IDX-04 | Unmapped | Pending |
| HLT-01 | Unmapped | Pending |
| HLT-02 | Unmapped | Pending |
| HLT-03 | Unmapped | Pending |
| OUT-01 | Unmapped | Pending |
| OUT-02 | Unmapped | Pending |
| OUT-03 | Unmapped | Pending |

**Coverage:**
- v1 requirements: 21 total
- Mapped to phases: 0
- Unmapped: 21

---
*Requirements defined: 2026-05-17*
*Last updated: 2026-05-17 after initial definition*
