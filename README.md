# OpenAI secure use

Working guidance on confidentiality and know-how protection when using ChatGPT, Codex and the OpenAI API. The documents are draft version 0.5 and include proposed controls that still require review and validation.

This repository covers the confidentiality and know-how domain of AI governance for OpenAI use. It supports information-use and access decisions; an organization-wide AI inventory is an input. It does not constitute a complete AI governance framework or establish compliance or certification. Confidentiality approval does not replace quality, fairness, output-rights or agent-action reviews.

## Documents

- [Master document](openai-confidentiality-draft.md) — introduction, draft status and table of contents.

The project is maintained in English only. The master document links to 14 chapter files and a references file in `chapters/en/`, plus a standards/regulatory appendix in `appendices/en/`.

## Standards and regulatory mapping

[Standards and regulatory mapping](appendices/en/appendix-a-standards-and-regulatory-mapping.md)

The mapping connects ISO/IEC 42001:2023 management clauses, selected NIST AI RMF 1.0 outcomes and applicable EU AI Act provisions to the chapters, evidence requirements and gaps. Legal applicability depends on scope, role, intended use and timing. It is not a certification or compliance declaration.

## Review

- [External review](review/round1/review.md) — preserved as supplied; describes v0.3 and its earlier chapter numbering.
- [Response and proposed follow-ups](review/round1/answer.md) — assesses the review against the v0.4 source snapshot and explains numbering changes.
- [Reviewer feedback](review/round1/review-feedback.md) — preserved as supplied; supports the proposed response and follow-up sequence, with the subsequent document changes recorded in the response. Technical execution remains outside the current document revision.

## Versioning

Keep filenames stable and use Git commits for history. Annotated tags identify review snapshots, starting with `v0.4` for the first tagged review package. The version and date in each master document identify exported copies; individual chapter filenames do not carry release versions. Chapter number prefixes follow the reading order.

Store each review exchange in `review/roundN/` (the current exchange is `review/round1/`). Reviews and responses should identify the source commit SHA. Preserve original reviewer text, and use a new tag for a new snapshot rather than moving an existing published tag.

## Contributing

Maintain all project documentation in English. Edit the relevant chapter file and keep changes focused so colleagues can review them independently.

Update the table of contents when adding, renaming or moving chapters. Keep source links and draft qualifications with the claims they support. Use pull requests for review and agreement on changes.
