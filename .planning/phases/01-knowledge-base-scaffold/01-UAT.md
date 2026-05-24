---
status: testing
phase: 01-knowledge-base-scaffold
source:
  - 01-01-SUMMARY.md
started: 2026-05-24T18:42:02.823Z
updated: 2026-05-24T18:42:02.823Z
---

## Current Test

number: 1
name: Knowledge Scaffold Exists
expected: |
  The repository has a `knowledge/` folder with `raw/inbox`, `sources`, `wiki/concepts`, `wiki/techniques`, `wiki/ingredients`, `wiki/equipment`, `wiki/recipes`, `wiki/safety`, `indexes`, `outputs`, and `health/reports` paths.
awaiting: user response

## Tests

### 1. Knowledge Scaffold Exists
expected: The repository has a `knowledge/` folder with `raw/inbox`, `sources`, `wiki/concepts`, `wiki/techniques`, `wiki/ingredients`, `wiki/equipment`, `wiki/recipes`, `wiki/safety`, `indexes`, `outputs`, and `health/reports` paths.
result: [pending]

### 2. Raw Evidence Boundary Is Clear
expected: `knowledge/raw/README.md` tells you that raw files are evidence, new markdown sources go in `knowledge/raw/inbox/`, raw sources should not be rewritten during compile or cleanup passes unless explicitly requested, and derived summaries/articles belong in `knowledge/sources/` and `knowledge/wiki/`.
result: [pending]

### 3. Index Entry Point Orients Future Sessions
expected: `knowledge/indexes/README.md` tells future sessions what to read first, explains the roles of raw, sources, wiki, indexes, outputs, and health, and marks later source/concept/article/backlink/open-question indexes as planned rather than already available.
result: [pending]

### 4. Root And Agent Docs Match The Scaffold
expected: `README.md` and `AGENTS.md` name the concrete scaffold paths, preserve the no-rewrite raw source rule, and point future agent sessions to `knowledge/indexes/README.md`.
result: [pending]

## Summary

total: 4
passed: 0
issues: 0
pending: 4
skipped: 0
blocked: 0

## Gaps

[none yet]
