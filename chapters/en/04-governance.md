## 4. Governance: From Business Risk to Approval Criteria

Governance defines how the company decides whether an AI use case is acceptable. The business challenges and research example establish what may be lost; this chapter turns those concerns into ownership, approval criteria and evidence requirements. The following chapters assess contracts, company policy and technical controls against those requirements.

### 4.1 Decision and ownership

The proposed approval unit is a specific business task using identified information through an identified service and access route. Approval of a product name alone is insufficient: the information, account, integrations and permitted actions define the decision boundary. Use the organization's AI inventory to identify relevant tasks; maintaining the complete inventory remains outside this guide.

The business owner sponsors the use case and accepts its remaining business risk. The information owner authorizes disclosure. Legal and privacy reviewers assess relevant obligations, while security and platform owners assess control coverage and operation. One person may hold several roles in a small company, but the decision record should still identify each responsibility.

For each use case, maintain the following record:

| Field | Required decision |
| --- | --- |
| Purpose and benefit | Task, intended users and expected business benefit |
| Information | Classification, information owner, customer restrictions and excluded content |
| Environment | Service, account/workspace or API project, client, integrations and access route |
| Processing | Permitted recipients and purposes, retention requirements and local copies |
| Authority | Allowed reads, changes, external transfers and required human approvals |
| Evidence and gaps | Contract review, relevant settings, control evidence and unresolved limitations |
| Accountability | Named business, information, legal/privacy and security/platform owners |
| Framework and legal applicability | ISO/NIST mapping, EU scope and role, prohibited-use screening, high-risk/transparency assessment, relevant application dates and reasons for exclusions |
| Decision lifecycle | Approve, approve with conditions or decline; rationale, expiry and review triggers |

### 4.2 Proportionate adoption

The following are proposed policy patterns, not statements that a subscription or product guarantees protection. Choose by information sensitivity, contractual restrictions, client coverage and the ability to operate controls. Company size affects available resources but does not determine acceptable exposure.

All patterns require a named owner, written company rules, user training, an approved-services register and an incident contact. An approved business workspace and training alone are not sufficient grounds to submit sensitive research or critical know-how.

| Pattern | Proposed permitted information | Owner and prerequisites | Limits and required evidence | Escalation trigger |
| --- | --- | --- | --- | --- |
| Public or synthetic work | Public material and synthetic data checked for hidden confidential content | Business owner; approved service/account and user training | Record the task and data classification; no approval of real confidential information follows | Real internal, customer or unpublished content becomes necessary |
| Approved business workspace | Internal information specifically authorized by its owner; sensitive research and restricted content excluded by default | Information owner and workspace administrator; reviewed terms, configured sharing, retention and integrations | Environment card records applicable terms, settings and authorized users; policy and training do not establish complete prevention of disclosure | Task needs stronger enforcement, a new integration, or information outside the approved categories |
| Company-controlled gateway | Selected confidential information only after explicit approval; access secrets remain excluded from model context | Security/platform owner; reviewed upstream agreement, supported clients, gateway operations and route restrictions | Require route, inspection, logging and failure-behaviour evidence before confidential use; a gateway does not control provider-internal processing or every client automatically | Unsupported operation, bypass route, mandatory inspection failure or inadequate control of recipients |
| Withhold the sensitive material | No submission of the protected content; use public or synthetic substitutes where useful | Information owner and business owner; task redesigned to avoid external disclosure | Record the restriction and confirm substitutes do not reproduce the secret; some tasks must remain unavailable | Reconsider only when obligations or available safeguards change and a new decision is recorded |

LiteLLM is one gateway candidate; OCI is one possible hosting and network environment. Neither is a universal prerequisite. A simpler pattern must not be used to bypass an obligation that requires stronger controls. If no feasible pattern meets the requirements, withhold the material rather than treating a smaller organization as grounds for accepting it automatically.

### 4.3 Related risks and approval handoffs

Confidentiality approval addresses what information may be processed and under which conditions. It does not authorize reliance on every output or every action an agent can take.

| Related risk | Responsible review | Required handoff |
| --- | --- | --- |
| Incorrect or fabricated output | Business/process owner and a qualified subject reviewer | Define checks before an output informs a decision, publication or customer delivery |
| Bias and unfair treatment | Business/process owner with the relevant risk, HR or legal reviewer | Assess impacts on affected people before using outputs in consequential decisions |
| Rights in inputs and outputs | Information owner and legal reviewer | Establish permission to supply inputs and conditions for reuse or publication of outputs |
| Agent changes and external actions | System/process owner and security/change approver | Define allowed actions, human approval points and recovery responsibility |
| Other model or regulatory risks | Organization's AI governance or risk owner | Route the use case to the broader assessment and record any unmet requirements |

The use-case record should name the actual reviewer or existing process for each relevant handoff. An unresolved prerequisite prevents approval of that use; this guide does not replace those assessments or assert overall conformity with a standard.

### 4.4 Approval and reassessment

Use the decision record and the following criteria to approve, conditionally approve or decline the task:

- Record the business purpose, expected benefit, information involved and consequences of disclosure or reuse for each proposed use case.
- Assign a business sponsor, information owner, legal reviewer and security owner; identify who may accept residual risk.
- Define the permitted recipients, processing purposes, access routes and retention requirements before selecting controls.
- Establish approval criteria: acceptable contractual commitments, enforceable company rules, verified technical coverage and documented limitations.
- Maintain a decision record linking each business risk to a requirement, proposed control, required evidence and accountable owner.
- Define exception approval, expiry and reassessment triggers when the use case, provider terms, clients or integrations change.
- Require validation and an operating owner before confidential production use; the final operations chapter specifies the tests and incident procedures.

### 4.5 Standards and legal applicability

Use [Appendix A](../../appendices/en/appendix-a-standards-and-regulatory-mapping.md) as the crosswalk for this decision record. For every relevant ISO clause, NIST outcome or legal article, record applicability, supporting chapter, required evidence, gap and owner. The appendix distinguishes a documented proposal from an operating control.

ISO/IEC 42001 provides the management-system structure; NIST AI RMF organizes risk outcomes; EU AI Act applicability requires a separate decision on scope, role, purpose and timing. Do not assign high-risk deployer duties to ordinary use merely because information is confidential. Conversely, confidentiality controls do not resolve obligations arising from a high-risk use or a provider role. Record the assessment rather than assuming that a supplier's compliance covers the company's own activity.

The organization should connect the confidentiality decision to its management review, impact assessment, competence, audit and corrective-action processes where relevant. Missing organizational records remain gaps even when this document describes the intended approach.

### 4.6 Reusing cloud and source-code governance

Cloud services and hosted source platforms such as GitHub provide useful precedents for AI adoption: companies entrust external providers with business-critical workloads and intellectual property while retaining responsibility for their own use. AI governance should reuse the organization's supplier, information-security and engineering processes, with additional assessment of model behaviour and business consequences. This is a proposed governance mapping, not evidence that the company already operates the controls.

AWS's shared-responsibility model illustrates that provider and customer duties depend on the service used. GitHub rulesets illustrate enforceable change controls, including required reviews and status checks. These sources support the underlying practices; they do not establish equivalent controls in an AI product. [AWS shared responsibility](https://aws.amazon.com/compliance/shared-responsibility-model/), [GitHub rulesets](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-rulesets/available-rules-for-rulesets).

An approved provider does not make every workload acceptable. Similarly, an approved AI service does not authorize every submission, integration or action. The approval unit in Section 4.1 remains the business task, information, environment and authority involved. Git is a version-control system; hosted-platform administration, repository permissions and review enforcement are separate controls that must be configured and operated.

| Existing governance practice | Reuse for AI confidentiality and know-how protection | Evidence or extension needed |
| --- | --- | --- |
| Supplier onboarding and shared responsibility | Review the AI service through existing procurement, legal, privacy and security processes | Record permitted processing, training use, retention, recipients, incident support and the division of duties for the actual service and agreement |
| Workload and repository registration | Link each AI task to its business owner and the organization's AI inventory | Identify the account, client, data sources, integrations and approved access route; provider approval alone is insufficient |
| Identity and least privilege | Reuse SSO, account lifecycle, service identities and access reviews where supported | Verify what the user and agent can read, disclose and change; permission to read information does not itself authorize external submission |
| Information classification and secrets management | Apply existing disclosure restrictions to prompts, files, retrieved content and logs | Check derived information and retrieval indexes; keep access secrets outside model context and avoid unnecessary content copies |
| Pull requests, peer review and release checks | Review changes to prompts, model selection, retrieval configuration, tools and permissions | Record the deployed configuration and relevant evaluation results; reassess material provider-side changes even when no local commit changes |
| Monitoring and incident response | Reuse incident ownership, escalation, containment and evidence handling | Validate available request and action records, supplier investigation support and privacy-aware retention; test connector revocation and fallback arrangements |
| Exceptions and service retirement | Reuse risk acceptance, expiry, periodic review and decommissioning | Address credentials, integrations, local copies, retrieval indexes and supplier retention limits; disabling access is not evidence of complete deletion |

**Oracle OCI as a business-policy and contract precedent**

Oracle OCI provides a cloud example at the supplier-governance level. Oracle describes its contract model as an agreement, ordering document and service policies; its agreements include the Cloud Services Agreement (CSA) and Oracle Master Agreement (OMA). For an actual purchase, identify the applicable agreement, order, incorporated service specifications and amendments rather than assuming that a public template defines the company's rights. [Oracle contract model](https://www.oracle.com/contracts/), [Oracle Cloud Services contracts](https://www.oracle.com/contracts/cloud-services/).

The following mapping concerns the business relationship with an external provider. It does not require hosting AI in OCI or adopting OCI infrastructure technology. These are proposed review questions, not findings that Oracle or an AI supplier accepts particular obligations.

| Business-policy or contract topic | Cloud/OCI review to reuse | Application to an AI service |
| --- | --- | --- |
| Approved service and contract scope | Identify the contracting entity, purchased service, order and applicable policies | Confirm that the actual product, account and intended business use fall within the reviewed terms; approval of one service does not extend automatically to another |
| Confidentiality and business information | Review content rights, confidentiality duties, permitted processing and exceptions | Establish permitted use of prompts, files, source code and outputs, including training or other secondary use; a personal-data agreement alone does not settle protection of non-personal know-how |
| Recipients and processing location | Assess subcontracting, processing locations, international transfers and required disclosures | Identify who may receive submitted information and under what terms; check separately any connected third-party service |
| Assurance and accountability | Review security commitments, available assurance evidence, incident notification, cooperation and liability limits | Record what evidence and assistance the company can obtain after suspected disclosure or misuse; assess remaining exposure against the value of the information |
| Service lifecycle and exit | Review policy changes, renewal, suspension, continuity, retrieval and deletion conditions | Reassess material changes in processing terms; establish how the company can stop use, recover needed business records and address retained copies |

Apply the same internal decision process used to authorize confidential workloads with a cloud supplier: procurement identifies the purchased scope, legal/privacy assess the applicable terms, the information owner authorizes disclosure and the business owner accepts documented residual risk. Translate that decision into employee rules specifying approved services, permitted information, prohibited submissions and exception owners. Supplier acceptable-use rules and the company's permission to disclose information are separate requirements.

The reusable output is a supplier approval record linked to the use-case record in Section 4.1, with the agreement and policy versions, approved information categories, conditions, gaps and reassessment date. Oracle's published contract structure supplies a precedent for this review; it does not establish that cloud and AI terms offer equivalent protection. The OpenAI-specific contract assessment remains in [Chapter 5](05-openai-policy-and-contracts.md).

**Confidentiality commitments and provider access: OCI, GitHub and OpenAI**

The central business question is whether the provider can access readable information, under what authority and for what purposes. A confidentiality commitment restricts access, use and disclosure; it does not by itself establish that the provider is technically unable to read the information. Assess automated service processing separately from access by personnel and from secondary use such as model training.

| Example | What the published material establishes | Business interpretation |
| --- | --- | --- |
| OCI Block Volume | Volumes and backups are encrypted at rest, using Oracle-managed keys by default, with customer-managed keys available. The storage service uses the configured encryption scheme to make data available for authorized use | Standard storage encryption does not establish that Oracle's service cannot decrypt the volume. It also does not establish that Oracle employees have unrestricted access. Assess contractual restrictions and access assurance separately. [Oracle Block Volume encryption](https://docs.oracle.com/en-us/iaas/Content/Block/Concepts/blockvolumeencryption.htm) |
| GitHub private repositories | The public Terms of Service treat private content as confidential but permit defined personnel access, including security, support and service-integrity purposes, and address legally compelled disclosure | Private means restricted access under the applicable terms, not technical unreadability by GitHub. Check the customer's actual agreement and any additional feature terms. [GitHub Terms, Section E](https://docs.github.com/en/site-policy/github-terms/github-terms-of-service#e-private-repositories) |
| GitHub Actions secrets | GitHub explicitly documents that uploaded secrets can be decrypted for injection into a workflow runtime | Stored credentials are a separate case from confidential source code. Encryption before upload does not mean GitHub cannot decrypt them. [GitHub Actions secrets](https://docs.github.com/en/actions/concepts/security/secrets) |
| OpenAI API | Submitted content is processed to produce a response. API data is not used for model training by default unless the customer opts in. Retention and human-review provisions depend on the applicable controls, model and features | No training is a purpose limitation, not a promise that information is unreadable to the service. Assess processing, personnel access, retention and secondary use independently; do not apply API provisions automatically to ChatGPT or Codex accounts. [OpenAI API data controls](https://developers.openai.com/api/docs/guides/your-data) |

For OCI, the conclusion about service decryption follows from the documented encryption design; it is not a finding about an employee's ability or authorization to extract customer disks. Customer-managed keys alone do not establish provider inability to read data while an authorized service uses those keys. A stronger claim requires evidence about the specific service and key-access arrangement.

The important difference is the authorized purpose. Storage can hold customer-encrypted content without interpreting its meaning; ordinary hosted AI inference requires the submitted information in a form the model can process. GitHub also processes content for enabled features and supplies decrypted secrets to workflows. None of these processing activities automatically grants permission for unrelated reuse.

The proposed approval test is therefore consistent across suppliers: **what can the service read, when may personnel access it, what uses are permitted, what evidence supports those limits, and what risk remains?** For AI, add explicit assessment of training and other secondary uses, safety review, retained prompts and outputs, and onward disclosure through integrations. The provider's ability to process content is not evidence of misuse; the business decision concerns whether the permitted processing and safeguards are acceptable for the information involved.

Existing governance workflows can also supply practical AI use cases:

- **Coding assistance:** Reuse repository permissions, secret controls, pull requests, independent review and CI checks. Separately authorize the source material sent to the service. Letting an assistant propose a change need not grant permission to merge or deploy it.
- **Internal knowledge assistance:** Reuse document ownership, classification and access reviews. Verify that retrieval respects the requesting user's permissions and that disclosure to the AI service is authorized. Answer quality and source support require the review identified in Section 4.3.
- **An agent with operational access:** Reuse service-account approval, least privilege and change management. Explicitly authorize tools, external transfers and consequential actions; require enforced approval gates where appropriate and define recovery ownership.

The analogy has limits. A secure and available service can still produce an incorrect answer, and untrusted retrieved content can attempt to redirect an assistant. NIST's Generative AI Profile provides additional risk context, including confabulation, information security and human–AI interaction. Those broader risks require the handoffs in Section 4.3 rather than an expansion of confidentiality approval into overall AI approval. [NIST Generative AI Profile](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.600-1.pdf).

Enforce disclosure and action boundaries through permissions, gateways and approval mechanisms with verified coverage. Instructions to a model are useful behavioural guidance but do not establish an access-control boundary. Version history can support investigation, but it cannot reverse an external disclosure or guarantee reproduction of a previous model response.

For each applicable row, mark the existing control **reuse**, **extend** or **add** in the use-case decision record, with an owner, required evidence and unresolved gap. Reuse existing approvals and operational processes where they cover the requirement; add AI-specific checks where their coverage ends. The following chapters examine the contractual, policy and technical evidence needed for that decision.

**Planned output:** A use-case approval record, responsibility matrix and control acceptance criteria, including the cloud and source-governance controls reused or extended for the analysis that follows.
