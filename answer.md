# Response to the external review

**Round:** 1 — confidentiality guidance; engineering response. No sprint applies.\
**Date:** 2 November 2026.\
**Revision:** This response assesses source commit `f55dfb44978bdb3b28a44efcee910ddb666d215a` on `main` in [codex_governance](https://github.com/rstyczynski/codex_governance). The supplied review describes v0.3; its exact reviewed SHA was not supplied. The earlier committed baseline is `b9eb44e9aaaa6cfad0d67d3f96663786218a026f`. Do not treat the review as an independent assessment of the new v0.4 research chapter. This response, review capture and versioning note are subsequent additions to the source snapshot.\
**Reviewer:** External reviewer; identity, model and tools not supplied. Response prepared by Codex.\
**Scope:** Documentation scope, maturity, proportionality and proposed framework mapping. No implementation, deployment test, compliance assessment or independent audit was performed.\
**Inputs:** [Original review](review.md), [English master](openai-confidentiality-draft.md), [Polish master](openai-confidentiality-draft-pl.md), and the chapter files linked below.

The review is useful and broadly consistent with the document's intended boundary. We agree that the work should remain a practical confidentiality and know-how guide for OpenAI use. A complete organization-wide AI governance system would be a separate undertaking. Positive comments about control design do not establish implementation effectiveness or compliance.

The five gap bullets are mapped below to stable finding IDs. Severity reflects this working draft, not a production assurance rating. Positions and proposed actions are engineering recommendations; they are not owner-approved scope changes. The review round remains open pending disposition of these proposals.

| Finding | Review topic | Position |
| --- | --- | --- |
| R1-M1 | Narrow focus | Partly agreed |
| R1-M2 | Sketched technical and operational chapters | Agreed |
| R1-M3 | Scaling guidance | Agreed |
| R1-L1 | Framework crosswalk | Partly agreed |
| R1-M4 | Broader AI risks | Agreed |

## Revision and chapter corrections

The current package is v0.4. A new research findings chapter was added after the version described in the review, shifting later chapter numbers:

| Review reference | Current location |
| --- | --- |
| Chapter 3 — governance | [Chapter 4](chapters/en/04-governance.md) |
| Chapter 4 — policy and contracts | [Chapter 5](chapters/en/05-openai-policy-and-contracts.md) |
| Chapter 5 — company rules | [Chapter 6](chapters/en/06-company-rules.md) |

The [new Chapter 3](chapters/en/03-research-findings-and-business-lessons.md) distinguishes reported disclosures, provider incidents, suspected reuse and legal outcomes. The review is preserved byte-for-byte, including its original numbering and version references.

## R1-M1 — Scope of the guidance

**Position:** Partly agreed. The introduction already limits the analysis to OpenAI confidentiality. That is an intentional boundary, rather than a requirement to expand into other vendors or internal model development. The repository name could nevertheless create a broader expectation.

**Proposed action:** Add a short scope statement to the README and introduction explaining that this is one control domain within wider AI governance. Reference an organization-wide AI inventory as an external input without attempting to build that entire program here.

**Acceptance:** Both languages identify the covered services, information risks, intended decisions and exclusions. No claim of complete AI governance or certification appears.

## R1-M2 — Implementation readiness

**Position:** Agreed. [Architecture](chapters/en/11-litellm-architecture.md), [network enforcement](chapters/en/12-network-enforcement-and-oci.md), [DLP and agent controls](chapters/en/13-dlp-and-agent-controls.md), and [validation and operations](chapters/en/14-validation-and-incident-response.md) still contain sketches. The existing acceptance table specifies intended evidence; it does not report passed tests.

**Proposed action:** Develop one bounded pilot design first: supported clients and operations, authentication, data paths, control ownership, failure behaviour and exceptions. Then execute and record the corresponding acceptance checks.

**Acceptance:** Each approved route has a documented configuration and observed test evidence. Unsupported routes and remaining uncertainties are explicit. The document continues to state that production approval is pending until the evidence exists.

## R1-M3 — Proportionate adoption

**Position:** Agreed. The introduction makes the LiteLLM route the default architecture under consideration. The draft lacks a clear explanation of when that complexity is justified.

**Proposed action:** Describe a minimum organizational baseline and optional stronger enforcement patterns. Select controls by information sensitivity, contractual obligations, client coverage and available operating capability, with company size as context. An approved business workspace and training should not be described as sufficient for every sensitive research use case.

**Acceptance:** Each pattern states permitted information, owner, prerequisites, limitations, evidence needed and escalation triggers. LiteLLM and OCI are identified as design choices rather than universal prerequisites.

## R1-L1 — Framework mapping

**Position:** Partly agreed. A concise crosswalk could help readers relate this control domain to a wider management system. The review's descriptions of NIST, ISO and EU obligations have not been independently validated in this response and should not be copied into the guidance as established compliance conclusions.

**Proposed action:** Prepare a separately sourced appendix mapping selected requirements to document sections, evidence and gaps. Verify framework editions and the applicability of any legal obligations before publication. Distinguish thematic alignment from conformity, certification and legal compliance.

**Acceptance:** Every mapping has an authoritative reference, applicable version, scope explanation and evidence link or an explicit gap. No blanket claim of compliance follows from a chapter cross-reference.

## R1-M4 — Risks beyond confidentiality

**Position:** Agreed. [Company rules](chapters/en/06-company-rules.md) address some human review and agent permissions, but the package does not assess the full set of AI risks named by the reviewer.

**Proposed action:** Add a brief boundary and handoff note covering output accuracy, bias, output rights, agent actions and other model risks. Identify the responsible review or approval process without turning this document into a general framework.

**Acceptance:** Readers can identify the additional assessments needed for a use case. Confidentiality approval is never presented as approval of output quality, rights, fairness or autonomous actions.

## Proposed follow-up order

1. Clarify scope and risk handoffs: R1-M1 and R1-M4.
2. Define proportionate adoption patterns: R1-M3.
3. Complete and test a bounded pilot: R1-M2.
4. Add the sourced crosswalk if needed for a customer, auditor or organizational requirement: R1-L1.

Proposed owners are the document owner for scope and adoption guidance, security/platform owners for the pilot, and legal or governance reviewers for any standards and legal mapping. Assignments and implementation remain unapproved. A further expert exchange is unnecessary for capturing this response; an independent recheck would be useful after selected changes and pilot evidence exist.

## Versioning approach

Keep stable filenames, including the requested `review.md` and `answer.md`. Git preserves their history; use an annotated `v0.4` tag for this snapshot. Retain the short version and date in both master documents for exported copies. Do not add versions to every chapter filename or maintain duplicate version folders. Review replies should cite commit SHAs because chapter numbers can change.

For later reviews, retain this snapshot in Git and identify the new reviewed SHA explicitly. Never silently revise an earlier reviewer's words. Moving a published tag to a newer revision would defeat its purpose; create a new version instead.

## Checks performed

- Read the complete supplied review and relevant source chapters; reconciled review chapter numbers against the current ToC.
- Verified sequential chapter numbering and existing chapter links in both master documents.
- Checked the captured review against the supplied attachment byte-for-byte, local Markdown links, and patch whitespace.
- No gateway, network, DLP or incident-response tests were run. No independent standards mapping or legal analysis was performed. Proposed follow-ups above are not implemented or independently verified.
