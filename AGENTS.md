<!-- GSD:project-start source:PROJECT.md -->
## Project

**Modernist Cooking Knowledge Base**

A personal markdown knowledge base for modernist cooking research. The user collects source material and manual notes as markdown in `raw/`, and the LLM agent compiles that material into a structured wiki with summaries, concept articles, backlinks, indexes, and source traceability.

This is not a multi-user product or polished application. It is a local, agent-maintained research workspace where the wiki is primarily written and maintained by the LLM, while the user can read or edit files whenever useful.

**Core Value:** Turn collected cooking sources and notes into a coherent, source-traceable modernist cooking wiki that gets more useful after every ingest and refinement pass.

### Constraints

- **Audience**: Single-user only - optimize for the user's own cooking research and agent workflow.
- **Input format**: Markdown-first - the user can handle conversion before ingest.
- **Storage**: Local filesystem - plain files and folders should remain readable and editable.
- **Authority model**: Agent-writable - the LLM may directly update the wiki without a review workflow.
- **Frontend**: Minimal - no dedicated UI is required for v1.
- **Scale**: Small-to-medium corpus - avoid infrastructure that only pays off at large scale.
- **Traceability**: Source links matter - important claims should preserve provenance where practical.
<!-- GSD:project-end -->

<!-- GSD:stack-start source:research/STACK.md -->
## Technology Stack

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
- Use pure markdown and AGENTS.md rules.
- Because the agent can read indexes and key files directly.
- Add generated index files and optional Python health scripts.
- Because future sessions need quick orientation and integrity checks.
- Add a small search CLI over markdown before RAG.
- Because local lexical search plus curated indexes may be enough at this scale.
## Sources
- Project context in `.planning/PROJECT.md`
- FPF framing from user request and loaded `fpf` skill terminology
- Inference from current workspace constraints and available tooling
<!-- GSD:stack-end -->

<!-- GSD:conventions-start source:CONVENTIONS.md -->
## Conventions

Conventions not yet established. Will populate as patterns emerge during development.
<!-- GSD:conventions-end -->

<!-- GSD:architecture-start source:ARCHITECTURE.md -->
## Architecture

Architecture not yet mapped. Follow existing patterns found in the codebase.
<!-- GSD:architecture-end -->

<!-- GSD:skills-start source:skills/ -->
## Project Skills

No project skills found. Add skills to any of: `.claude/skills/`, `.agents/skills/`, `.cursor/skills/`, `.github/skills/`, or `.codex/skills/` with a `SKILL.md` index file.
<!-- GSD:skills-end -->

<!-- GSD:workflow-start source:GSD defaults -->
## GSD Workflow Enforcement

Before using Edit, Write, or other file-changing tools, start work through a GSD command so planning artifacts and execution context stay in sync.

Use these entry points:
- `/gsd-quick` for small fixes, doc updates, and ad-hoc tasks
- `/gsd-debug` for investigation and bug fixing
- `/gsd-execute-phase` for planned phase work

Do not make direct repo edits outside a GSD workflow unless the user explicitly asks to bypass it.
<!-- GSD:workflow-end -->

## Knowledge Base Operating Rules

### Folder Roles

- `knowledge/raw/` is the evidence layer. `knowledge/raw/inbox/` is the default landing zone for converted markdown sources and manual notes. Do not rewrite raw sources during compile or cleanup passes unless the user explicitly asks.
- `knowledge/sources/` contains one source-summary markdown file per processed raw source.
- `knowledge/wiki/` contains compiled knowledge articles. These are agent-maintained and may be edited directly.
- `knowledge/indexes/` contains navigation files that future agent sessions should read first. Start with `knowledge/indexes/README.md` before assuming detailed source, article, backlink, or open-question indexes exist.
- `knowledge/outputs/` contains exploratory answers, comparisons, briefs, and recipe-development notes.
- `knowledge/health/` contains audit reports and improvement suggestions.

### Compile Rules

When compiling raw sources into wiki content:

1. Inspect the source inventory before writing.
2. Create or update a source summary for every processed raw file.
3. Write compiled knowledge into `knowledge/wiki/`, not back into `knowledge/raw/`.
4. Prefer focused articles over giant catch-all pages.
5. Update relevant indexes after creating, renaming, or materially changing articles.
6. Track open questions instead of inventing certainty.

Do not rewrite raw sources in `knowledge/raw/` or `knowledge/raw/inbox/` during compile, cleanup, indexing, or health passes unless the user explicitly asks for that raw file to be edited.

### Evidence Rules

- Important culinary claims should cite a source summary or raw source path where practical.
- Safety-sensitive guidance needs extra caution: time, temperature, preservation, additives, substitutions, and food-safety claims should not be presented as certain without evidence.
- Distinguish source-backed facts from agent synthesis.
- If evidence is weak, say so in the article or open-questions index.

### Modernist Cooking Taxonomy

Start with these wiki areas and add new ones only when repeated content pressure appears:

- `concepts/`
- `techniques/`
- `ingredients/`
- `equipment/`
- `recipes/`
- `safety/`

### Health Checks

Health passes should look for:

- Raw sources without summaries.
- Wiki articles with weak or missing source references.
- Dead links or renamed files not reflected in indexes.
- Duplicate or near-duplicate concepts.
- Missing backlinks between clearly related topics.
- Candidate articles implied by sources but not yet written.



<!-- GSD:profile-start -->
## Developer Profile

> Profile not yet configured. Run `/gsd-profile-user` to generate your developer profile.
> This section is managed by `generate-claude-profile` -- do not edit manually.
<!-- GSD:profile-end -->
