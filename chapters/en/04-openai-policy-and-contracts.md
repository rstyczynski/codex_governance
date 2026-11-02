## 4. OpenAI Policy and Contract Perspective

OpenAI's commitments must be assessed against the service the company actually purchases and the terms it accepts. The documents below answer different questions: what the parties may do with information, how personal data is processed, which uses are permitted, and which controls are available. The practical conclusion is that business confidentiality combines contractual duties and configured controls; it is not a promise that OpenAI is technically unable to access content.

### 4.1 Identify the applicable documents

For individual services in Poland, start with the Europe Terms of Use; business services follow a separate contractual route. A paid personal account should not be treated as equivalent to a company agreement. [Europe Terms of Use, opening provisions](https://openai.com/policies/eu-terms-of-use/).

| Document | Question to resolve |
| --- | --- |
| [Services Agreement](https://openai.com/policies/services-agreement/) and the company's order or negotiated agreement | What has OpenAI agreed with this company? |
| [Data Processing Addendum](https://openai.com/policies/data-processing-addendum/) | What applies to personal data processed on the company's behalf? |
| [Service Terms](https://openai.com/policies/service-terms/) | What changes for an enabled feature? |
| [Usage Policies](https://openai.com/policies/usage-policies/revisions/2025-10-29/) | Is the intended activity permitted? |

For Codex, record the sign-in and upstream route. Authentication affects applicable controls and data-handling policies; putting LiteLLM in the route does not by itself change the agreement. [Codex authentication](https://learn.chatgpt.com/docs/auth).

### 4.2 Confidentiality and permitted use of business content

Sections 4.2 and 7 of the Services Agreement restrict content use, require explicit agreement for service improvement, and impose confidentiality obligations. They permit specified disclosures, including necessary recipients under confidentiality duties and legally required disclosure. These are contractual commitments with exceptions, not an absolute access prohibition. [Services Agreement, sections 4.2 and 7](https://openai.com/policies/services-agreement/).

**Company decision:** Treat unpublished methods and research as confidential even after personal identifiers are removed. Keep ownership, confidentiality and permitted reuse as separate approval questions. Before approving critical know-how, review remedies and liability in the accepted agreement rather than assuming full compensation for any loss.

### 4.3 Model training and secondary use

OpenAI distinguishes individual-service content, which may be used for training subject to controls, from business inputs and outputs, which are not used for training by default. It describes an explicit API data-sharing option, including feedback. Training permissions must therefore be checked alongside account type and administrator settings. [Model-improvement policy](https://openai.com/policies/how-your-data-is-used-to-improve-model-performance/).

**Company decision:** Disable unauthorized sharing and review feedback workflows. A training opt-out is not a substitute for restrictions on other uses, storage or onward transfer.

### 4.4 Personal data and the DPA

The DPA governs personal data processed on the customer's behalf. It covers documented instructions, confidentiality, breach notification, conditional audit rights, subprocessors and return or deletion subject to legal retention. Its definition of Customer Data is narrower than all business knowledge. [DPA, sections 1–4 and 6](https://openai.com/policies/data-processing-addendum/).

The Europe Privacy Policy expressly excludes content processed on behalf of business customers from its scope and directs readers to customer agreements. Do not use that policy as the sole basis for approving business-content processing. [Europe Privacy Policy, scope](https://openai.com/policies/eu-privacy-policy/).

**Company decision:** Identify the relevant privacy roles, processing purpose, authorization to disclose, transfer arrangements and retention instructions. Assess non-personal know-how under confidentiality commitments as well.

### 4.5 Security, access and retention

OpenAI's enterprise privacy statement describes encryption, access restrictions and product-specific circumstances for authorized personnel access. These descriptions do not mean that the provider cannot process readable information. [Enterprise privacy](https://openai.com/enterprise-privacy/).

API retention controls have endpoint-specific eligibility and exceptions. No-training, no-retention and no-human-access are different claims. [API data controls](https://developers.openai.com/api/docs/guides/your-data).

**Company decision:** Approve an explicit retention and access profile for each route. Include local Codex state and company gateway copies; OpenAI settings do not delete those stores.

### 4.6 Subprocessors, integrations and feature terms

OpenAI publishes subprocessors with product, location and processing-purpose information. Use that inventory to assess the selected service, rather than assuming a single recipient or processing country. [Sub-processor list](https://openai.com/policies/sub-processor-list/).

Service Terms add feature-specific provisions, including beta disclaimers, administration, GPT sharing and third-party Apps. Enabling a feature can change recipients and rights; a general workspace approval is insufficient. [Service Terms, sections 2, 3, 5 and 7](https://openai.com/policies/service-terms/).

**Company decision:** Approve LiteLLM hosting, scanners, logging systems and external tools separately. Their access is not justified by OpenAI's commitments alone.

### 4.7 Acceptable use and policy versions

Usage Policies impose obligations on users, including privacy, safety and restrictions on certain activities. They are not a replacement for provider confidentiality obligations and do not make an otherwise unauthorized disclosure lawful. [Usage Policies](https://openai.com/policies/usage-policies/revisions/2025-10-29/).

The assessment date is **2 November 2026**. Use the revision effective **29 October 2025**. The [general policy page](https://openai.com/en-GB/policies/usage-policies/) currently displays a revision effective **20 November 2026**; record it as forthcoming and assess its effect before that date.

### 4.8 Deployment approval record

The company should retain an approval record connecting its contractual assessment to the deployed configuration. This is the evidence needed to explain why a particular workflow is permitted.

- Identify the legal entity, accepted agreements, service, workspace or API project and versions.
- Record permitted data categories, training-sharing choices, retention and recipients.
- Record integration approvals, configuration evidence and responsible owners.
- Review confidentiality remedies, liability, feature exclusions and incident procedures against the value of the information.
- Reassess changes in terms, product features, authentication and data flows.

For this document, a **contractual commitment** is a term binding the parties, a **provider description** explains intended operation, and **deployment evidence** demonstrates observed controls. All three inform approval; none alone establishes protection against every confidentiality risk. The data-flow and technical chapters specify what must be configured and tested.

