# Guidance requirements specification

Status: Draft.

## Purpose and authority

The [product vision](../README.md#product-vision) defines intended value.
This SRS owns the guidance product's boundary, actor model, use cases,
functional requirements and release scope. [NFR.md](../NFR.md) is the
authoritative non-functional requirements register, incorporated by reference.
The [candidate architecture](architecture.md) owns document design and the
[test profile](test-profile.md) owns validation methods.

The [Product Backlog](../BACKLOG.md) owns prioritized delivery work.
PBI-003 through PBI-010 cover Inception definition and review; PBI-017 covers
the research basis and PBI-018 delivers the guidance. Requirements below
describe intended outcomes, not claims that the existing draft passes review.

## Product boundary and context

The product is an English-language guide to confidentiality and protection of
business know-how in organizational OpenAI use. It supports assessment of a
proposed task, information, service, account, access route, safeguards and
residual risk. Inputs include an organization's AI inventory, information
classification, supplier agreements and existing governance arrangements.
Outputs are understandable guidance, proposed decision records, example
controls and validation questions that an organization can adapt.

ChatGPT, Codex, the OpenAI API, connected services and organizational
infrastructure are subjects of assessment. They are external to the guide;
the product neither calls their APIs nor enforces their configuration.
Implementing a gateway, firewall, DLP system or production deployment is
outside the deliverable. LiteLLM and OCI are candidate examples, not universal
requirements. Comprehensive AI governance, certification and organization-specific
legal or deployment approval are outside the boundary.

## Stakeholders

Business sponsors need useful adoption decisions. Information owners need
control of disclosure. Employees and technical teams need workable rules.
Security, privacy and legal functions need reviewable assumptions and evidence.
Guide maintainers need source traceability and manageable updates. The Product
Owner determines project scope, priorities and acceptance. Small, medium-sized
and large organizations are reader contexts, not distinct approval authorities.

## Actors

**ACT-001 — Business decision maker.** Uses the guide to assess value,
identify accountable owners and decide whether to approve, restrict, defer
or reject a proposed use within the organization's decision process.

**ACT-002 — Information owner.** Determines the sensitivity of information
and whether its disclosure for the proposed task is authorized.

**ACT-003 — Security or platform practitioner.** Assesses information flows,
control boundaries, operational ownership and evidence needed to rely on safeguards.

**ACT-004 — Legal or privacy adviser.** Assesses applicable agreements,
obligations and legal/privacy review needs, with explicit applicability limits.

**ACT-005 — Employee or use-case proposer.** Finds permitted-use rules,
requests approval and identifies how to report a suspected disclosure.

**ACT-006 — Guide maintainer or reviewer.** Updates content, checks sources,
reviews requirements coverage and records limitations and review outcomes.

One person may perform several roles. External systems have no interactive
actor role in this document-only product; providers and tools are assessed
entities and evidence sources. An executable product would require revisiting
this actor model rather than treating described components as actors.

## Use cases and success criteria

### UC-001 — Assess a proposed organizational use

Primary actor: ACT-001. Supporting actors: ACT-002, ACT-003 and ACT-004.
Trigger: a proposed task involving OpenAI assistance. Preconditions: the task
and information owner can be identified; missing details remain explicit.

The reader identifies the benefit and information involved, determines the
service/account/access route, reviews supplier conditions and information
flows, selects proportionate safeguards and assigns review responsibilities.
The reader records an approval, restriction, deferral or rejection, with
conditions, residual risk and reassessment triggers.

If authority, terms or control evidence is missing, the reader defers the
decision or excludes sensitive information. Conflicting confidentiality and
other approval needs are routed to the responsible reviewers. Postcondition:
the reasoning and unresolved evidence are visible. Success: a reviewer can
identify the task, information, owner, conditions, decision and remaining risk
without interpreting a proposed control as demonstrated protection.

### UC-002 — Establish usable employee rules

Primary actor: ACT-003; supporting actors: ACT-001, ACT-002, ACT-004 and ACT-005.
Trigger: organizational adoption or a policy gap. The reader derives permitted
environments and information categories, disclosure limits, approval and
exception routes, incident reporting and named responsibilities. Missing
organizational decisions remain pending. Success: an employee can determine
whether a representative task is permitted and where to obtain help; example
rules are visibly subject to organizational approval.

### UC-003 — Assess a proposed technical safeguard

Primary actor: ACT-003; supporting actors: ACT-002 and ACT-004.
Trigger: a workflow needs technical protection. Preconditions: intended task,
data flow and required protection are stated.

The reader maps information and recipients, identifies enforcement points,
states supported clients and content, and defines evidence for normal use,
restricted input, scanner failure, bypass, logs and recovery. The reader
assigns an operating owner and records limits. If coverage cannot be established,
the reader records the gap and restricts or defers the affected use rather
than declaring protection. Postcondition: a bounded validation plan exists.
Success: each claimed safeguard has a threat, boundary, failure behavior and
required evidence; the guide does not imply that the plan has been executed.

### UC-004 — Adapt adoption to organizational capacity

Primary actor: ACT-001; supporting actor: ACT-003. The reader compares small,
medium-sized and large organizational contexts, assigns responsibilities and
chooses an operable approach based on sensitivity and assurance needs.
Success: each context has a practical approach and explicit limits; size alone
does not authorize weaker protection or mandate a specific vendor stack.

### UC-005 — Prepare for a suspected disclosure

Primary actor: ACT-005; supporting actors: ACT-001 through ACT-004.
Trigger: a suspected unauthorized submission or exposure. The reader finds
reporting, containment, evidence-preservation and reassessment guidance.
Where logs are incomplete, the uncertainty is recorded; sensitive content is
not unnecessarily copied into investigation records. Success: responsibilities,
immediate decisions and evidence gaps can be identified without claiming that
an incident exercise has already been performed.

### UC-006 — Maintain the guide after new evidence

Primary actor: ACT-006; supporting actors: ACT-003 and ACT-004.
Trigger: a product increment, review finding or changed source/assumption.
The maintainer checks affected claims, functional coverage and connected
documents, validates applicable NFRs, assesses missing NFRs and records SRS
changes or a no-change decision. Success: changed claims have provenance,
validation results and visible limitations; unresolved approvals remain explicit.

## Functional requirements

**FR-001 — Support use decisions.** The guide shall explain how to connect a
business task, information sensitivity, ownership, service/account/route,
approval conditions and residual risk. Acceptance: UC-001 can be walked through
using the guide with a reviewable decision outcome. Delivery: PBI-018;
research dependency: PBI-017.

**FR-002 — Explain governance and employee rules.** The guide shall identify
responsibilities, permitted-use decisions, exceptions and handoffs to other
AI governance reviews. Acceptance: UC-002 identifies an employee's next action
and responsible decision maker. Delivery: PBI-018; dependency: PBI-017.

**FR-003 — Explain supplier and information-lifecycle assessment.** The guide
shall distinguish service/account boundaries, contractual instruments,
processing, retention, deletion and secondary-use questions. Acceptance:
UC-001 and UC-003 identify the evidence needed for the actual use rather than
inferring approval from a product name or subscription. Delivery: PBI-018;
dependency: PBI-017.

**FR-004 — Explain technical safeguards and validation.** The guide shall cover
information flows, identity, network/gateway controls, DLP, agent permissions,
operating responsibilities and failure/bypass validation. Acceptance: UC-003
produces bounded checks and exposes unsupported coverage. Delivery: PBI-018;
dependency: PBI-017.

**FR-005 — Support three organizational contexts.** The guide shall provide
practical adoption guidance for small, medium-sized and large organizations.
Acceptance: UC-004 yields understandable responsibilities, choices and limits
for each context. Delivery: PBI-018; dependency: PBI-017.

**FR-006 — Support incidents and reassessment.** The guide shall explain
reporting, containment, proportionate evidence preservation and reassessment
after material changes. Acceptance: UC-005 identifies immediate actions and
UC-006 identifies what must be revisited. Delivery: PBI-018; dependency: PBI-017.

## Non-functional requirements

Apply the complete [root NFR register](../NFR.md). Functional requirements state
what the guide helps readers accomplish; NFRs state the quality and evidence
conditions those explanations must satisfy. Implementation work for an NFR
may be prioritized in the backlog without duplicating its normative wording.

## Initial release scope and acceptance

The proposed first release is a reviewed guide covering FR-001 through FR-006,
all six use-case walkthroughs and all applicable NFRs. The
[master document](../openai-confidentiality-draft.md) is the reader entry point.
Chapter-level sketches must be resolved or explicitly excluded by the Product
Owner before release; a complete table of contents alone is insufficient.

Release acceptance requires recorded functional walkthroughs, NFR results,
source and consistency review, local-link checks, visible remaining limitations
and Product Owner acceptance. Publication format, date and distribution
arrangements remain open decisions. Existing draft version 0.5 is not a
release-acceptance claim. No infrastructure, implemented control, deployment
test, certification or organization-specific approval is supplied by this release.

## Constraints, assumptions and risks

The guide remains English-only and uses the established Markdown/chapter
structure. It relies on public evidence and declared research inputs; no signed
customer agreement or adopting organization's configuration has been supplied.
Source statements may change, so source review must match the claim and version.

**RISK-001 — Stale or overbroad claims.** Mitigate with scoped source review,
effective/consultation-date distinctions and explicit uncertainty; see NFR-002
and NFR-003. **RISK-002 — Proposed controls mistaken for proven protection.**
Mitigate with NFR-004 and UC-003. **RISK-003 — Advice impractical for a reader's
capacity.** Mitigate with UC-004 and NFR-005. **RISK-004 — Examples disclose
confidential information.** Mitigate with NFR-007. **RISK-005 — Baseline and
delivery records drift.** Mitigate with NFR-006 and NFR-008.

## Maintenance and unresolved decisions

Review this SRS with every increment under the [local policy](../RUP_patch.md).
Update affected requirements and links alongside the change; record a no-change
decision when appropriate. Requirements and proposed release scope are subject
to Product Owner review. Delivery priorities remain owned by the backlog and
sprint plan.
