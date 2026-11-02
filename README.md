# OpenAI secure use

Working guidance on confidentiality and know-how protection when using ChatGPT, Codex and the OpenAI API. The documents are draft version 0.4 and include proposed controls that still require review and validation.

## Documents

- [English master document](openai-confidentiality-draft.md) — introduction, draft status and table of contents; the primary working version.
- [Polish master document](openai-confidentiality-draft-pl.md) — translated introduction and table of contents.

Each master links to 14 chapter files and a references file in `chapters/en/` or `chapters/pl/`. Matching filenames identify corresponding sections across languages.

## Review

- [External review](review.md) — preserved as supplied; describes v0.3 and its earlier chapter numbering.
- [Response and proposed follow-ups](answer.md) — assesses the review against the v0.4 source snapshot and explains numbering changes.

## Versioning

Keep filenames stable and use Git commits for history. Annotated tags identify review snapshots, starting with `v0.4` for the current package. The version and date in each master document identify exported copies; individual chapter filenames do not carry release versions. Chapter number prefixes follow the reading order.

Reviews and responses should identify the source commit SHA. Preserve original reviewer text, and use a new tag for a new snapshot rather than moving an existing published tag.

## Contributing

Use English by default. Edit the relevant chapter file and keep changes focused so colleagues can review them independently. Make substantive changes in the English version first, then update the corresponding Polish translation. If a translation update is deferred, say so in the pull request.

Update both tables of contents when adding, renaming or moving chapters. Keep source links and draft qualifications with the claims they support. Use pull requests for review and agreement on changes.
