# Non-functional requirements

Status: Draft.

## Authority and validation

The [vision](README.md#product-vision) defines intended value, the
[SRS](docs/srs.md) owns functional requirements and scope, and this file owns
non-functional requirements for the guidance product. The
[candidate architecture](docs/architecture.md) explains the document design;
the [test profile](docs/test-profile.md) defines checks.
The [local policy](RUP_patch.md) requires review of the entire register for
every product increment, including compliance, regression and missing requirements.

NFR identifiers are stable. Record each requirement's result and evidence in
the increment's validation record, explaining any non-applicability or reused
evidence. Assess additions and changes even when the outcome is no change.
An unrun check remains pending; file existence is not a compliance result.
The criteria below use explicit review methods rather than invented numeric
targets. They apply to all maintained product content unless stated otherwise.

## NFR-001 — English and understandable explanations

The guide shall use English and explain terms and reasoning sufficiently for
its business, technical, security and legal readers to follow the intended
decisions. Source quotations and proper names may retain their original form.
Source: [project language scope](README.md#documents) and
[vision](README.md#product-vision). Validation: review changed prose for language,
unexplained terminology and missing reasoning; walk through affected SRS use
cases and record any point requiring unstated specialist knowledge.

## NFR-002 — Traceable evidence

Material factual claims shall identify supporting sources or be explicitly
identified as analysis, proposals or unresolved questions. Disputed accounts
shall retain attribution and uncertainty. Source: the
[research basis](progress/E.1/sprint_E.1_research.md).
Validation: inspect each new or materially changed factual claim against its
linked evidence, checking that the evidence supports the actual scope of the
claim. A functioning URL alone does not demonstrate support.

## NFR-003 — Scoped and dated claims

Service, contract, policy and control claims shall identify their relevant scope
and version/date where necessary to interpret applicability. Distinguish a
source's effective date from its consultation date and expose unresolved
currentness. Source: the research basis and
[source register](progress/E.1/sprint_E.1_sources.md). Validation: inspect affected
claims for service/account/feature boundaries and date applicability; revalidate
changed or time-sensitive sources before asserting that they are current.

## NFR-004 — Honest assurance boundaries

The guide shall distinguish proposed safeguards, provider statements, tested
behavior and organization-specific approval. It shall not imply that the guide
implements a deployment, proves compliance, or resolves unrelated governance
reviews. Source: [product boundary](docs/srs.md#product-boundary-and-context)
and the [master introduction](openai-confidentiality-draft.md#introduction).
Validation: inspect changed assurance claims, examples and conclusions for
matching evidence and explicit limits. Missing deployment evidence must remain
visible rather than being represented as a passed test.

## NFR-005 — Proportionate applicability

Guidance shall remain usable across small, medium-sized and large organizational
contexts without treating size as permission for weaker required protection or
making optional technology universal. Source: the product vision and research
basis. Validation: perform UC-004 for all three contexts after changes to adoption
guidance; for other changes, inspect their effect on those contexts and justify
reuse of prior walkthrough evidence where appropriate.

## NFR-006 — Navigable and consistent documentation

Maintained documents shall link to related authoritative documents and state
ownership of requirements, design, operating steps and evidence. Local links,
relevant anchors, names and scope descriptions shall remain consistent.
Source: [local materialization policy](RUPStrikesBack.patch/RUP_patch.md#keep-materialized-documents-connected).
Validation: check local links and anchors, reciprocal references and changed
descriptions. Review connected documents in the same increment and preserve
historical evidence rather than silently rewriting it.

## NFR-007 — Safe illustrative information

Examples and retained review evidence shall avoid unnecessary disclosure of
real confidential information, credentials or personal data. Clearly identify
synthetic or illustrative records. Source: the product's confidentiality purpose
and the research basis's evidence-preservation guidance. Validation: inspect
added examples, screenshots, commands and logs for sensitive content and
provenance before including them. An adopting organization's real records are
outside this repository's required fixtures.

## NFR-008 — Reviewable changes and validation status

Every product increment shall record functional and NFR validation, assess NFR
completeness, and reconcile the SRS and connected documents. Evidence shall
identify what was inspected, outstanding gaps and the basis for reused results.
Source: [requirements maintenance policy](RUPStrikesBack.patch/RUP_patch.md#maintain-non-functional-requirements-and-the-srs-with-every-increment)
and P8 of the local patch. Validation: inspect the increment's review record
for every NFR, extension/no-change assessment, SRS decision and actual check
results; do not infer Product Owner acceptance from automated checks or silence.

## Changes and completeness assessment

19 November 2026: initial register extracts existing language, evidence,
applicability, assurance, navigation and confidentiality constraints and adds
the explicitly requested per-increment maintenance discipline. No runtime,
latency, availability or software-performance targets are introduced for this
document-only product. Reassess the register if publication requirements,
reader evaluation evidence or the product boundary changes.
