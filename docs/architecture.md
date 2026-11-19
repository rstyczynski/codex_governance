# Candidate guidance architecture

Status: Candidate.

## Scope and authoritative relationships

This is the architecture of the guidance product defined by the
[vision](../README.md#product-vision) and [SRS](srs.md). It explains how maintained
documents support reader decisions and the [NFR register](../NFR.md).
The [test profile](test-profile.md) defines validation.
It is not an accepted design or validation result for an OpenAI deployment.

## Reader journey and content responsibilities

The [master document](../openai-confidentiality-draft.md) introduces the
boundary, draft status and reading order. Chapters 1–3 establish assets,
business concerns and the research case; chapter 4 connects them to ownership,
approval and proportionate adoption. Chapters 5–6 explain supplier assessment
and proposed company rules. Chapters 7–10 explain data flows, accounts,
protection limits and retention. Chapters 11–13 discuss optional architecture,
network controls and DLP/agent safeguards. Chapter 14 addresses validation,
operations and incidents. Chapter 15 and Appendix A provide references and
standards/regulatory mapping with applicability limits.

FR-001 and FR-005 are primarily supported by chapters 1–4; FR-002 by chapters
4 and 6; FR-003 by chapters 5 and 7–10; FR-004 by chapters 7–14; FR-006 by
chapters 4 and 14. These are intended coverage locations, not passed acceptance
results. Each walkthrough must verify that the explanations connect across
chapters instead of merely finding matching section titles.

## Information and evidence flow

Source material and research findings inform attributed claims and clearly
marked analysis. Those claims support reader-facing decisions, proposed
controls and required validation evidence. An adopting organization supplies
its own agreements, configuration, accountable owners, deployment tests and
approvals. The guide must keep these evidence boundaries visible throughout
the reader journey (NFR-002 through NFR-004).

The repository stores Markdown source with stable chapter filenames and Git
history. Source links stay near claims; the research source register records
research provenance. NFR.md owns quality requirements, the SRS owns integrated
requirements context, and the backlog owns delivery priority. This avoids
separate normative copies that drift (NFR-006 and NFR-008).

## Design choices and alternatives

Retain the existing master-and-chapters organization so readers can navigate
from the business problem to governance, technical options and verification.
A single expanded file would simplify export but make focused chapter review
harder; a hosted interactive application would introduce an unsupported
implementation and operating scope. Neither alternative is needed for this
baseline. Export/publication tooling remains a later decision.

Use organizational context and information sensitivity to explain adoption
choices; do not prescribe a fixed stack by company size (NFR-005). Use synthetic
examples and bounded evidence descriptions (NFR-007). Explain terminology and
decisions for the intended readers rather than using configuration detail as
a substitute for reasoning (NFR-001).

### Testing Strategy

The selected product has no executable runtime, so software build, unit,
integration and infrastructure gates are not applicable. Documentation checks
and reader-journey review remain mandatory despite `Test: none` and
`Regression: none` in the existing plan. Exact local structural commands and
manual review scenarios are defined in the test profile. No deployment
experiment or software test skeleton is needed for this architecture.

Review each changed requirement and its connected content, then the complete
NFR register. Walk UC-001 and UC-003 across the high-risk approval and control
boundaries. Walk UC-004 in all three organizational contexts. Recheck employee
rules, incidents and maintenance through UC-002, UC-005 and UC-006. Missing
source evidence or reader understanding remains a gap even when all links work.

## Assumptions, risks and next refinement

Existing Markdown files are the maintained delivery source; the guide is a
working draft. Reader usability has not been established through a field
study, technical examples have not been deployed, and sources have not been
established as current for a release. The SRS identifies these
risks and NFRs define the review discipline.

E.1 research should refine unsupported claims and uncertainty boundaries.
C.1 should refine the guide from those findings and demonstrate the reader
journeys. No prototype child PBIs are proposed for this document-only scope.
The roadmap and plan own lifecycle intent and scheduling respectively; this
candidate does not advance their statuses.
