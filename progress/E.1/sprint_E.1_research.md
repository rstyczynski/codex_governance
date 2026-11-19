# E.1 — Research basis for OpenAI confidentiality guidance

The [product vision](../Sprint.0/sprint_Sprint.0_analysis.md) defines the
intended value and scope. The [source register](sprint_E.1_sources.md) records
the research inputs and their limitations.

## Research objective

Determine what an organization must understand before entrusting confidential
information or business know-how to ChatGPT, Codex or the OpenAI API. The
research should support practical guidance for small, medium-sized and large
organizations, connecting business concerns with contractual, organizational
and technical protection.

The central question is not whether an AI product is simply “secure”. It is
whether a particular business task may use particular information through a
particular service and access route, under conditions the organization can
understand and accept.

## Confidentiality includes business knowledge

Personal information is only one category of sensitive material. Source code,
pricing methods, strategic plans and unpublished research may retain their
commercial value after names and identifiers are removed. Anonymization alone
therefore cannot establish that a disclosure is acceptable.

The analysis must distinguish ownership from permission to process information.
It must also distinguish permission to read information internally from
permission to send it to an external service. A useful approval boundary
includes the information owner, intended task, recipients and permitted use.

## Different failures require different evidence

The incident and research-dispute material raises three distinct concerns:
an employee submitting material without authority, a provider failing to
isolate information, and suspected reuse of unpublished work. They should not
be combined into a single claim that a provider steals customer information.

A reported submission establishes neither subsequent training use nor onward
disclosure. A provider's incident report is evidence of its stated findings,
not an independent investigation. Similarity between research results and the
timing of announcements may motivate investigation but cannot alone establish
the origin of a result.

For the confidential-research case, the researcher's statement and provider's
response must remain separate accounts. Claims, investigations and unresolved
questions need distinct treatment. Legal proceedings likewise require reading
the operative decision rather than treating an allegation or initial penalty
announcement as the final outcome.

The practical implication is to preserve enough provenance to investigate a
concern: what information was submitted, by whom, through which account and
under which terms. Evidence collection must itself avoid unnecessary copies
of confidential content.

Research inputs include the [researcher's statement](https://cims.nyu.edu/~tristanb/statement.pdf),
[OpenAI's response](https://openai.com/index/navier-stokes-solution/),
the [provider incident report](https://openai.com/index/march-20-chatgpt-outage/)
and [Samsung incident reporting](https://www.cybersecuritydive.com/news/Samsung-Electronics-ChatGPT-leak-data-privacy/647219/).
The Samsung report is a secondary source; disputed accounts are not independent
proof of misuse.

## Provider commitments and residual trust

Supplier assessment must separate the agreement binding the parties from
product descriptions and observed deployment behaviour. Each answers a
different question. A product description explains intended operation; an
agreement establishes obligations; a technical check can establish behaviour
only within the conditions tested.

“No model training” does not mean “no processing”, “no retention” or “no
possible personnel access”. OpenAI describes business-data training exclusions
by default. Its API documentation separately addresses monitoring and
application state. The relevant product, feature, account and agreement must
therefore be identified before applying a provider statement to a business
use. [Enterprise privacy](https://openai.com/enterprise-privacy/),
[API data controls](https://developers.openai.com/api/docs/guides/your-data).

The resulting assessment should ask what processing is permitted, who may
receive information, how access is constrained, what records and assistance
are available after an incident, and which retention and deletion conditions
apply. A personal-data agreement should not substitute for consideration of
non-personal confidential know-how.

## Distinguish services, accounts and contractual instruments

The research identifies separate assessment questions for personal accounts,
company-managed workspaces and API projects. Paying for access does not itself
answer who administers the environment, which agreement applies or which
information the organization authorizes for submission. Codex authentication
and upstream routing also need an explicit assessment rather than assumptions
based on the client name.

A supplier assessment needs several kinds of document. The service agreement
and actual order address the purchased service and obligations between the
parties. A data-processing addendum addresses its defined personal-data scope.
Feature terms can introduce additional conditions. Acceptable-use policies
restrict activities but do not constitute permission from an information owner
to disclose confidential material. Privacy notices and security descriptions
must be read within their stated scope.

The resulting research conclusion is to identify the actual legal entity,
service, account, authentication route and enabled features before comparing
terms or recommending controls. Preserve effective dates separately from
consultation dates. A forthcoming policy revision must not silently replace
the version applicable to the assessed use.

The research inputs are the [Services Agreement](https://openai.com/policies/services-agreement/),
[Data Processing Addendum](https://openai.com/policies/data-processing-addendum/),
[Service Terms](https://openai.com/policies/service-terms/),
[Europe Terms of Use](https://openai.com/policies/eu-terms-of-use/) and
[authentication documentation](https://learn.chatgpt.com/docs/auth).
No signed customer agreement was supplied for an organization-specific conclusion.

## Translate responsibilities into usable company rules

The analysis supports a short employee-facing policy that explains approved
environments, permitted information, minimum necessary disclosure, restricted
content, integration approval, incident reporting and exceptions. Access
credentials need separate treatment from ordinary business content; an
exception process must not imply authority to override contractual or legal
restrictions.

Several responsibilities must remain identifiable even where one person holds
multiple roles. The business owner judges value and residual business risk;
the information owner authorizes disclosure; legal and privacy advisers assess
relevant obligations; security and platform owners assess and operate controls.
Users need an understandable route to obtain approval or report a mistake.

A supplied Oracle employee-use excerpt offers a policy-design example. It does
not establish another organization's approvals, contract terms or key-management
arrangements. Its version and effective date were not supplied. The research
therefore supports adapting the policy pattern, not copying its assurances.

## Learn from established supplier governance

Organizations already entrust valuable information to cloud and hosted
source-code providers. Procurement, supplier assessment, information
classification, identity management, least privilege, exception handling and
incident response provide useful starting points for AI adoption.

The analogy must not imply equivalent contracts or technical protection.
Encryption and private access need to be considered alongside the service's
ability to process readable content. Supplier access for delivering or
supporting a service is also distinct from permission to reuse information
for an unrelated purpose.

The research direction is to identify which existing organizational controls
can be reused, where AI changes the information flow, and which additional
questions need an explicit decision. Sources include the
[AWS shared-responsibility model](https://aws.amazon.com/compliance/shared-responsibility-model/),
[Oracle contract model](https://www.oracle.com/contracts/) and
[GitHub private-repository terms](https://docs.github.com/en/site-policy/github-terms/github-terms-of-service#e-private-repositories).
These are comparison inputs, not approval of an OpenAI deployment.

### Oracle cloud governance as a research input

Oracle's [Cloud Adoption Framework governance guidance](https://docs.oracle.com/en-us/iaas/Content/cloud-adoption-framework/governance.htm)
provides a broader precedent than the supplier contract alone. It connects
business objectives, accountable roles, vendor management, information
protection, controlled changes and ongoing review.

The proposed application to AI is to reuse the organization's cloud-adoption
decision process: identify the business use and information owner, review the
supplier and purchased scope, assign operating responsibilities, approve
conditions and exceptions, and reassess material changes. This is an analytical
transfer of governance practices, not a claim that cloud approval covers AI.

Oracle's [risk and compliance guidance](https://docs.oracle.com/en-us/iaas/Content/cloud-adoption-framework/risk-and-compliance.htm)
adds shared responsibility, information classification, data-flow analysis and
gap assessment as research inputs. For AI, extend those questions to prompts,
retrieved context, tools, secondary use and disclosure through agent actions.
A provider's assurance evidence does not replace the customer's responsibilities.

These practices concern organizational decisions and accountability. They do
not require OCI hosting. Small organizations may combine roles; medium-sized
organizations need coordination across teams; large organizations need consistent
oversight across business units. The responsibilities remain identifiable in
each case. The transfer to these contexts is our analysis, not an Oracle
endorsement of the proposed AI guidance.

## Map the complete information path

The disclosure boundary includes more than a typed prompt. Relevant material
can include uploaded files, selected repository content, retrieved documents,
tool results, conversation context and diagnostic output. Connected services
introduce additional recipients that need their own assessment.

Local execution of a tool does not establish where model inference occurs.
Likewise, a locally stored record may later be synchronized, backed up,
exported or supplied as context. The assessment needs both the logical use of
information and its actual storage and transmission paths.

Account type, authentication route and enabled features are part of that map.
An application name or paid subscription alone is insufficient to identify
the applicable administrative and contractual boundary. Configuration,
instructions and enforced restrictions must also be distinguished: a written
instruction is not proof that a prohibited read or transfer is prevented.

## Evaluate controls by their boundaries

A company-controlled gateway is a candidate control for selected workflows,
not a universal solution. Its value depends on whether the relevant requests
actually pass through it, which operations it supports and what happens when
a required check fails. Authentication, auxiliary traffic and external tools
must be assessed separately where they follow other paths.

Inspection intended to prevent disclosure must act before restricted material
is transmitted. Checking a response cannot undo disclosure of its prompt.
LiteLLM documents different guardrail execution modes, making check placement
an explicit design concern. Its documentation establishes a possible mechanism,
not tested coverage for a particular organization.
[Guardrail modes](https://docs.litellm.ai/docs/proxy/guardrails/quick_start).

DLP can be evaluated against defined content categories and realistic examples.
The research does not establish reliable detection of every novel invention
or business idea. False positives, missed detections, unsupported content types
and scanner failures all affect whether a control is useful.

Network restrictions and endpoint controls can support approved routes, but
coverage depends on the actual routing and managed-device boundary. Introducing
another scanner, gateway or logging service also introduces another place where
information may be processed or stored.

## Separate access controls from provider unreadability

Encryption, account isolation, administrative permissions and agent sandboxes
address different threats. The analysis must identify the protected asset,
threat actor and point of enforcement before saying that a safeguard meets a
confidentiality requirement.

In particular, encryption at rest and customer-managed keys should not be
presented as evidence that a service cannot process readable information while
performing its authorized function. Restrictions on personnel access and
contractual limits on secondary use require their own evidence. Stronger
architectural claims, such as confidential processing with attestation, need
specific support for the actual service rather than inference from general
security terminology.

Assurance reports likewise need a defined system scope, assessment period,
control coverage and exceptions. A certification logo cannot answer every
question about a particular task or integration.

For network protection, the research identifies DNS restrictions, web inspection,
firewall routing and endpoint management as complementary design considerations.
An OCI-hosted enforcement point does not by itself cover an employee's arbitrary
off-network connection. A managed firewall's underlying vendor does not establish
that separately marketed DLP capabilities are included in that service.
[Oracle Network Firewall overview](https://docs.oracle.com/en-us/iaas/Content/network-firewall/overview.htm),
[Palo Alto application support](https://docs.paloaltonetworks.com/ai-access-security/getting-started/whats-supported-with-ai-access-security),
[HTTP-filtering prerequisites](https://developers.cloudflare.com/cloudflare-one/traffic-controls/get-started/http/).

## Define evidence for failures and ongoing operation

The research supports evaluating normal use and failure conditions together.
An adopting organization needs evidence that a supported task remains usable,
restricted input is stopped before disclosure, mandatory scanner failure does
not permit an unnoticed fallback, and unapproved routes cannot bypass the
intended boundary.

That evidence also needs to cover logs and diagnostics, agent access and action
permissions, configuration overrides, and retained local data. A simulated
incident can examine reporting, containment, credential response and evidence
preservation. These are proposed verification questions, not experiments
performed by this research.

Continuing protection requires ownership of updates, access reviews,
certificates, inspection rules and reassessment. Changes in service terms,
features, models, clients or integrations can invalidate an earlier decision.
The guidance should explain that operating responsibility alongside initial
approval, without promising a tested deployment or an organizational sign-off.

## Treat retention as an information lifecycle

The assessment should distinguish provider monitoring, application state,
conversation records, local sessions, memories, logs, caches and backups.
Disabling one feature or deleting one visible item is not evidence that all
copies are gone.

Retention requirements need an owner, purpose, location, duration, deletion
mechanism and applicable exceptions. The same discipline applies to evidence
retained for investigation. A record created to demonstrate confidentiality
must not become an uncontrolled disclosure channel.

## Apply the research to three organization sizes

For a small organization, the research points toward clear permitted-use rules,
explicit responsibility even when roles are combined, understandable supplier
conditions and controls that can be operated with limited specialist support.
Where adequate protection cannot be established, using public or synthetic
material—or withholding sensitive content—remains a valid decision.

For a medium-sized organization, coordination becomes central: teams need
consistent service approval, information classification, account administration,
exception handling and incident ownership. Additional technical enforcement
should address an identified need and have a sustainable operating owner.

For a large organization, the analysis must accommodate business-unit boundaries,
specialist review functions, varied environments and consistent evidence across
many uses. Central governance still needs use-specific decisions; approval of
a supplier does not authorize every task or category of information.

These are analytical implications of differing organizational capacity, not
results of a comparative field study. Size does not reduce confidentiality
obligations or determine a fixed technology package. Information sensitivity,
contractual restrictions and required assurance remain the deciding factors.

## Relate confidentiality to wider governance

The research identifies standards and regulatory mapping as a way to connect
confidentiality decisions to wider organizational processes. It must distinguish
applicability, a documented proposal and evidence that a control operates.
The guide should not turn thematic alignment into a claim of certification or
legal compliance.

Confidentiality approval also leaves separate questions about output accuracy,
fairness, rights and authority for consequential actions. The appropriate
handoffs need to be clear without expanding this research into a complete AI
governance programme. Relevant research inputs include the
[ISO management-system description](https://www.iso.org/standard/42001),
[NIST AI RMF](https://airc.nist.gov/airmf-resources/airmf/5-sec-core/) and
[EU AI Act overview](https://digital-strategy.ec.europa.eu/en/policies/regulatory-framework-ai).
Specific legal applicability and dates require a separate current assessment.

The standards research used public descriptions and an explanatory overview
for the ISO clause structure; the full licensed normative standard was not
available for a conformity assessment. NIST mapping was limited to selected
confidentiality-relevant risk outcomes. EU screening concerned role, purpose
and applicability before duties; confidential information alone was not used
to classify a deployment. None of these activities supplies organizational
operating records or a complete management-system assessment.

## Direction for developing the guide

The guide should lead from the business task and information at risk to the
supplier conditions, organizational responsibilities, possible safeguards and
evidence needed for a decision. It should explain the interaction of these
measures rather than present a product checklist as proof of protection.

Case studies should distinguish evidence from allegation. Technical examples
should identify their assumptions and unsupported paths. Organizational
examples should serve all three sizes without equating size with sensitivity.
Templates should help readers define their own approvals and evidence; they
must not suggest that the guide supplies an approved organizational policy or
a tested deployment.

## Questions remaining

The research does not establish the effectiveness of a particular deployment,
complete support across every client or feature, reliable detection of arbitrary
know-how, or the adequacy of a particular organization's contracts and controls.
Those questions require scoped evidence from the adopting organization.

For the guidance itself, the remaining work is to substantiate detailed claims,
keep account and feature boundaries accurate, make the three organizational
contexts concrete, and preserve the distinction between recommendations and
verified protection. Source versions and case status need rechecking before
publication. The research is documentary; no deployment experiment or field
study is claimed.
