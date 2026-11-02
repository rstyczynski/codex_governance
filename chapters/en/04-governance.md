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

**Planned output:** A use-case approval record, responsibility matrix and control acceptance criteria for the analysis that follows.
