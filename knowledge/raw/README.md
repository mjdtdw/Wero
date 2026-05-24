# Raw Evidence

`knowledge/raw/` is the evidence layer for Wero. Put converted markdown sources and manual notes in `knowledge/raw/inbox/` when they are ready for an agent ingest pass.

Do not rewrite raw sources during compile, cleanup, or wiki maintenance passes unless the user explicitly asks for that specific raw file to change. Raw files are source evidence, not working drafts.

Derived files belong elsewhere:

- Source summaries go in `knowledge/sources/`.
- Compiled wiki articles go in `knowledge/wiki/`.
- Exploratory answers and briefs go in `knowledge/outputs/`.
- Audit reports go in `knowledge/health/reports/`.

When a raw source has been processed, preserve enough path information in the derived summary or wiki article for future sessions to trace important claims back to the evidence.
