## 9. Technical Protection and Its Limits

Security mechanisms protect against particular threats. Encryption can protect a connection or stored data, access controls can restrict authorized users, and agent sandboxes can limit actions on a machine. These mechanisms do not all provide the same protection against the service operator or against an authorized but inappropriate disclosure.

**Chapter sketch**

- Explain encryption in transit, encryption at rest and customer-managed keys, including which components can still decrypt data.
- Examine account isolation, role-based access, administrative access and access logging for the selected products.
- Distinguish network restrictions and agent sandboxing from restrictions on what OpenAI may do with received content.
- Explain confidential computing and attestation as stronger architectural options only where documented and applicable; do not assume their presence in standard ChatGPT or Codex.
- Assess audit reports by system scope, assessment period, controls tested and exceptions, rather than by certification logos alone.

OpenAI's Codex security cookbook describes how enterprise controls can be combined with existing identity, endpoint and network protections. It is a basis for configuration review, not evidence that this company's deployment is already secure. [Codex security cookbook](https://learn.chatgpt.com/docs/enterprise/security-cookbook).

**Planned output:** A control matrix showing threat, mechanism, evidence, limitations and residual trust.

