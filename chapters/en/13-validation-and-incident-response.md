## 13. Validation, Operations and Incident Response

Approval should follow demonstrated control of the intended workflows, rather than installation of individual products. Validation must confirm that approved tasks remain usable, restricted transfers are prevented on covered routes, and failure conditions do not silently disable protection. Ongoing operation must preserve those properties as products and policies change.

**Chapter sketch**

| Validation area | Pilot acceptance evidence |
| --- | --- |
| Approved route | Application and Codex test calls reach the intended OpenAI backend through LiteLLM |
| Bypass prevention | Unapproved direct access fails on managed devices, including remote operation |
| Input protection | Synthetic restricted content is blocked before upstream submission |
| Scanner failure | Mandatory checks fail closed without an automatic direct fallback |
| Feature coverage | Each permitted request type has a recorded test; unsupported routes remain blocked |
| Log confidentiality | Credentials and restricted test content are absent from routine logs, traces and exports |
| Agent boundaries | Attempts to read restricted paths or make unapproved external transfers fail |
| Configuration boundaries | Effective settings and managed requirements are checked under user, project and session overrides |
| Local data lifecycle | Synthetic markers are traced through sessions, enabled memories, artefacts and backups; cleanup is verified per store |
| Incident handling | A simulated disclosure produces a report, credential response and evidence record |

- Assign ownership for updates, dependency security, certificates, rule changes and access reviews.
- Establish review triggers for new models, changed terms, new client versions and additional integrations.
- Define incident containment, credential rotation, provider contact and assessment of contractual or legal notification duties.
- Record residual risk, especially undetected know-how, authorized recipients and unmanaged personal devices outside the controlled boundary.
- Specify an approval gate and rollback plan before introducing confidential production information.

**Planned output:** A pilot report, operating runbook, incident procedure and signed deployment decision.

