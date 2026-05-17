# Phase 1: Knowledge Base Scaffold - Context

**Gathered:** 2026-05-17
**Status:** Ready for planning

<domain>
## Phase Boundary

This phase establishes the local markdown knowledge-base scaffold for Wero: the `knowledge/` folder structure, the source-handling boundary between raw evidence and compiled wiki content, the project operating contract, the root README orientation, and the first index entry point for future agent sessions.

It does not define source-summary templates, wiki article templates, backlink maintenance, health-check report formats, or output filing conventions beyond enough placeholder structure to make those future phases obvious and navigable.

</domain>

<decisions>
## Implementation Decisions

### Folder Granularity
- **D-01:** Create the full practical v1 folder scaffold immediately, not just the six top-level folders. The scaffold should include the required durable areas plus obvious first-level subfolders needed for Phase 1 orientation.
- **D-02:** Include the modernist cooking wiki taxonomy from the project contract under `knowledge/wiki/`: `concepts/`, `techniques/`, `ingredients/`, `equipment/`, `recipes/`, and `safety/`.
- **D-03:** Include a raw source inbox path so the user can begin placing converted markdown sources without conversion automation. Prefer `knowledge/raw/inbox/` as the default landing zone.
- **D-04:** Include `knowledge/health/reports/` so later audit reports have an obvious home without needing to change the scaffold.
- **D-05:** Keep placeholder files lightweight. Use small README files only where they clarify boundaries or orientation, and `.gitkeep` only where an otherwise-empty folder must exist in git.

### Evidence Boundary
- **D-06:** Treat `knowledge/raw/` as the FPF evidence layer. Raw files are source evidence and must not be rewritten during compile or cleanup passes unless the user explicitly asks.
- **D-07:** Treat `knowledge/sources/` and `knowledge/wiki/` as derived episteme layers. Source summaries and wiki articles may be agent-maintained, but important claims should preserve traceability back to source summaries or raw paths where practical.
- **D-08:** Make the raw-vs-derived distinction visible in the scaffold, ideally through `knowledge/raw/README.md` and `knowledge/indexes/README.md`.

### Index Entry Point
- **D-09:** `knowledge/indexes/README.md` should be a practical orientation guide for future agent sessions, not only a stub. It should say what to read first, what each knowledge area means, and which indexes will be added in later phases.
- **D-10:** The first index entry point should acknowledge planned but not-yet-created indexes instead of pretending they exist.

### Operating Contract and README
- **D-11:** Preserve the existing `AGENTS.md` direction and strengthen it only where Phase 1 needs concrete scaffold rules: folder roles, raw source safety, compile boundaries, index updates, source traceability, and safety caution.
- **D-12:** The root README should remain readable for the user while giving enough workflow detail that a future agent can orient itself without reading the whole planning directory.

### the agent's Discretion
- The user explicitly delegated all gray areas except folder granularity to the agent.
- The agent may choose exact placeholder filenames and wording as long as the scaffold remains markdown-first, local-filesystem readable, source-traceable, and not overbuilt.
- The agent may avoid creating premature templates for source summaries, wiki articles, health reports, and outputs because those are scoped to later phases.

</decisions>

<canonical_refs>
## Canonical References

**Downstream agents MUST read these before planning or implementing.**

### Project Planning
- `.planning/PROJECT.md` - Defines the project purpose, constraints, FPF framing, and key decisions.
- `.planning/REQUIREMENTS.md` - Defines Phase 1 requirements: SCF-01, SCF-02, SCF-03, SRC-01, SRC-04, and IDX-01.
- `.planning/ROADMAP.md` - Defines Phase 1 scope, success criteria, and phase ordering.
- `.planning/STATE.md` - Shows current workflow state and Phase 1 as the active phase.

### Existing User-Facing Contract
- `AGENTS.md` - Current project-local agent operating contract and knowledge-base rules.
- `README.md` - Current root orientation for the Wero knowledge base.

No external ADRs or specs were referenced during discussion.

</canonical_refs>

<code_context>
## Existing Code Insights

### Reusable Assets
- `AGENTS.md`: Already contains project constraints, folder roles, compile rules, evidence rules, taxonomy, and health-check guidance. Phase 1 should refine or preserve this rather than replace it wholesale.
- `README.md`: Already explains the purpose, FPF-inspired knowledge model, repository shape, and basic workflow. Phase 1 can update it after the concrete scaffold exists.

### Established Patterns
- Markdown-first project artifacts are the established pattern.
- Git is already initialized and used for planning artifacts.
- No application code or UI patterns exist; this phase is filesystem and documentation work.

### Integration Points
- New scaffold files should live under `knowledge/`.
- Planning outputs for this phase live under `.planning/phases/01-knowledge-base-scaffold/`.
- Future phases will build on the scaffold by adding templates, indexes, health workflows, and output filing conventions.

</code_context>

<specifics>
## Specific Ideas

- User selected folder granularity option: "Srazu vsyo nuzhnoe" / create everything needed immediately.
- Use the FPF framing already in the project: raw as evidence layer, wiki as episteme layer, source links as evidence graph, and agent passes as transformer work.

</specifics>

<deferred>
## Deferred Ideas

None - discussion stayed within Phase 1 scope.

</deferred>

---

*Phase: 1-Knowledge Base Scaffold*
*Context gathered: 2026-05-17*
