# Pitfalls Research

**Domain:** Personal LLM-maintained modernist cooking knowledge base
**Researched:** 2026-05-17
**Confidence:** MEDIUM

## Critical Pitfalls

### Pitfall 1: Losing Provenance

**What goes wrong:**
Wiki articles become fluent but no longer show where important claims came from.

**Why it happens:**
The agent optimizes for readability and synthesis, then forgets to preserve evidence links.

**How to avoid:**
Require source references in article templates and source summaries. Keep raw files separate from compiled files.

**Warning signs:**
Articles contain ratios, temperatures, safety guidance, or ingredient behavior claims with no source path nearby.

**Phase to address:**
Phase 1 and Phase 2.

---

### Pitfall 2: Indexes Rot

**What goes wrong:**
Indexes claim articles or sources exist that were renamed, moved, or deleted.

**Why it happens:**
Agent updates content files but forgets global index maintenance.

**How to avoid:**
Make index updates part of every compile pass. Add health checks for dead links and missing summaries.

**Warning signs:**
Future sessions need broad search instead of reading indexes; backlinks point nowhere.

**Phase to address:**
Phase 3.

---

### Pitfall 3: Taxonomy Overgrowth

**What goes wrong:**
The wiki gets too many folders and article types before the corpus justifies them.

**Why it happens:**
Modernist cooking has many dimensions: technique, ingredient, tool, process, recipe, science, safety.

**How to avoid:**
Start with a small taxonomy and add categories only when multiple articles need them.

**Warning signs:**
New sources trigger debates about where files belong instead of useful compilation.

**Phase to address:**
Phase 1.

---

### Pitfall 4: Confusing Recipes, Techniques, and Claims

**What goes wrong:**
A recipe note, a technique explanation, and a general culinary claim get merged into one unclear article.

**Why it happens:**
Cooking knowledge is practical and conceptual at the same time.

**How to avoid:**
Use article templates with explicit sections for "what it is", "how to use", "parameters", "evidence", "related".

**Warning signs:**
Articles are long but hard to use while cooking or researching.

**Phase to address:**
Phase 2.

---

### Pitfall 5: Treating Agent Guesses as Food-Safe Facts

**What goes wrong:**
The wiki gives unsafe or unverified guidance about time, temperature, preservation, additives, or substitutions.

**Why it happens:**
LLM synthesis can sound authoritative even when evidence is weak.

**How to avoid:**
Mark confidence, cite sources, and add a safety article category. Avoid presenting unsupported guidance as tested fact.

**Warning signs:**
Safety-sensitive claims have no source, caveat, or confidence note.

**Phase to address:**
Phase 2 and Phase 4.

## Technical Debt Patterns

| Shortcut | Immediate Benefit | Long-term Cost | When Acceptable |
|----------|-------------------|----------------|-----------------|
| No source inventory | Faster first ingest | Agent forgets what has been processed | Never after initial scaffold |
| No article templates | Faster writing | Inconsistent wiki, weak retrieval | Only for throwaway outputs |
| Manual-only indexes | Low tooling | Index rot | Acceptable until corpus reaches repeated maintenance pain |
| No health reports | Less process | Silent quality decay | Only before first real compile |

## Performance Traps

| Trap | Symptoms | Prevention | When It Breaks |
|------|----------|------------|----------------|
| Reading the whole corpus each time | Slow sessions, context overload | Maintain summaries and indexes | Dozens of sources/articles |
| Giant articles | Hard navigation and weak reuse | Split into focused holons | Articles over several thousand words |
| No file naming convention | Duplicate pages and broken links | Slugs and stable paths | Immediately after several sources |

## "Looks Done But Isn't" Checklist

- [ ] **Folder scaffold:** Exists but AGENTS.md does not explain how to use it.
- [ ] **Source ingest:** Raw files exist but source inventory does not track status.
- [ ] **Wiki article:** Reads well but lacks source links.
- [ ] **Index:** Lists pages but is not checked against actual files.
- [ ] **Health check:** Finds issues but does not file a report or follow-up candidates.

## Pitfall-to-Phase Mapping

| Pitfall | Prevention Phase | Verification |
|---------|------------------|--------------|
| Losing provenance | Phase 1 | Article template includes source references |
| Indexes rot | Phase 3 | Health check catches missing links and index drift |
| Taxonomy overgrowth | Phase 1 | Initial taxonomy remains small and documented |
| Confusing article types | Phase 2 | Templates produce distinct source/concept/technique pages |
| Unsafe agent guesses | Phase 2 | Safety-sensitive articles require sources/confidence notes |

## Sources

- `.planning/PROJECT.md`
- FPF evidence graph and strict map/territory distinction
- Domain inference for modernist cooking knowledge management

---
*Pitfalls research for: personal modernist cooking knowledge base*
*Researched: 2026-05-17*
