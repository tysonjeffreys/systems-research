# Publishing And Versioning

## Source Of Truth

- Source of truth for paper text and release notes is this repository.
- Zipped paper bundles and companion notes must be updated together in the same release batch.

## Versioning Rules

- Use semantic paper versions already present in filenames when available (for example: `v1.4.1`).
- For repository-level snapshots, tag with date-based releases:
  - `papers-vYYYY-MM-DD`
- Keep one release-note entry per paper update, even when batching publication.

## Publication States

- `draft`: local edits not yet tagged.
- `published`: tagged commit with release notes and synchronized bundles.

## Release Checklist

1. Update paper source (`main.tex`) and repack corresponding zip bundle.
2. Update companion implementation notes if claims reference harness behavior.
3. Add or update per-paper release note in `release-notes/`.
4. Update top-level `CHANGELOG.md`.
5. Record cross-project commit references for linked harnesses:
   - `regulated-agent-replay-suite`
   - `regulated-retrieval-gates`
6. Tag the repository (`papers-vYYYY-MM-DD`) after validation.

## Initial Backfill Policy

- Pre-git history is represented as semantic backfill notes, not reconstructed micro-commits.
- If historical snapshots are later recovered, add them as archival entries without rewriting existing history.
