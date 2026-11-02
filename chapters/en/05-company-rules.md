## 5. Draft Company Rules

Company rules translate the risk assessment into instructions employees can follow. The draft below is a proposed baseline for approval, using the supplied Oracle example as an organizational pattern. It does not transfer Oracle approvals, key-management claims or contractual arrangements to this company.

### Proposed employee-facing rules

1. **Approved environment.** Process non-public company information only through services and access routes listed in the approved-services register. Personal accounts are not approved for this purpose.
2. **Minimum necessary content.** Provide only the information needed for the task. Access to a document does not automatically authorize disclosure to an AI service.
3. **Restricted content.** The standard environment must not receive passwords, private keys, access tokens, authentication codes, full payment card numbers or card verification codes. Authentication secrets must be supplied through approved authentication mechanisms, not included in model context.
4. **Sensitive and regulated information.** Health information, other highly sensitive personal data, classified information and restricted public-sector or defence-contract information require a separately approved environment. Include PHI, FCI and CUI categories where applicable to the company's obligations.
5. **Customer and partner information.** Do not submit information where processing would breach an NDA, contract, legal obligation or the approved purpose of collection.
6. **Know-how.** Unpublished inventions, research, strategic plans, proprietary methods and critical source code require approval from the information owner and security lead before external processing.
7. **Legal and other professional work.** AI may assist authorized preparation and analysis. Professional conclusions and advice require the appropriate qualified human review; AI output is not company approval.
8. **Codex permissions.** Provide only necessary repository, directory, tool and network access. Production changes, external transfers and publication follow the company's approval process.
9. **Integrations and sharing.** New plugins, MCP servers, connectors, shared links and external scanners require approval. Employees must not alter training-sharing or security settings outside their authority.
10. **Incident reporting.** Report an accidental disclosure immediately to **[incident contact]**. Preserve identifiers and relevant evidence without unnecessarily copying the sensitive content. Revoke exposed credentials promptly.
11. **Exceptions.** Record the purpose, information, environment, safeguards, approvers and expiry date. An internal exception cannot override law, contract or provider restrictions.

### Responsibilities and approval record

| Responsibility | Proposed owner |
| --- | --- |
| Approve business uses and accept residual risk | Business owner |
| Classify and authorize use of information | Information owner |
| Configure and verify technical controls | Security and platform owners |
| Review contracts and applicable obligations | Legal adviser; privacy lead where relevant |
| Report errors and follow approved workflows | Every user |

**Planned output:** A short approved policy, an environment card and an exception form. Complete **[company name]**, **[approved environments]**, **[owners]** and **[incident contact]** before issuance.

