# Project test profile

Status: Draft — documentation product

## Purpose

This profile defines validation for the guidance product described by the
[vision](../README.md#product-vision), [SRS](srs.md), [NFR register](../NFR.md)
and [candidate document architecture](architecture.md). It defines required
checks, not evidence that they have passed.

## Applicable checks

The product is Markdown guidance. Software builds, unit tests, integration
tests and deployment experiments are not applicable. Source review, reader
walkthroughs, document consistency and local-link checks remain required under
the [local documentation-only policy](../RUPStrikesBack.patch/RUP_patch.md#documentation-only-research-and-construction-allocation).

## Structural validation

Run from the repository checkout with Git and ripgrep available:

```bash
cd "$(git rev-parse --show-toplevel)"
git diff --check
rg --files README.md NFR.md docs chapters appendices
```

The whitespace check must return successfully without diagnostics. The
inventory must include the requirements, architecture, test profile and guide
content. Review untracked additions too; ordinary Git diffs omit them.

Resolve local links relative to each containing file, check target existence
and section anchors, and inspect reciprocal references in connected documents.
Check the master table of contents against chapter names and reading order.
File existence alone does not validate a claim or reader journey.

## Functional and source validation

Walk SRS UC-001 through UC-006 using the guide and non-confidential illustrative
tasks. Record relevant passages, the observable decision outcome and missing
steps against each success criterion. UC-004 requires all three organizational
contexts. Review affected journeys again after content changes; justify any
reused evidence by its version and continuing applicability.

For each new or materially changed factual claim, inspect supporting evidence
for attribution, scope, version and date applicability. Revalidate time-sensitive
claims before asserting currentness. Distinguish documented provider behavior,
contractual commitments, analysis and proposals. A reachable URL alone does
not prove support. Pending source checks remain explicit.

## NFR validation and regression

For every increment, record results and evidence for every applicable NFR,
including effects on existing content. Explain non-applicability and reused
evidence. Assess whether the register needs extending and update it for accepted
changes. Review the SRS and record updates or a justified no-change decision.

Use the increment's existing validation/audit record. Missing evidence remains
pending; structural success does not establish reader comprehension, source
accuracy or Product Owner acceptance. An applicable accepted NFR that is unmet
blocks completion under the local policy.

## Test-data and dependency policy

Use public, synthetic or explicitly authorized material. Local structural checks
need no credentials or external services; source review may need network access.
Do not include sensitive customer material or credentials in examples or logs.

## Handover and future changes

Open the actual guide and demonstrate the promised reader decisions during
handover. Deployment tests and organizational approvals belong to adopting
organizations; the guide must explain required evidence without implying
execution. A selected export format needs rendering and readability checks.
Any future code-bearing scope needs an updated architecture and exact build
and software-test commands before implementation.
