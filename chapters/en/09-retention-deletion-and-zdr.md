## 9. Retention, Deletion and Zero Data Retention

The business must distinguish information used temporarily for a response from information retained for history, application state, monitoring or legal obligations. Disabling model training does not resolve all of these questions, and deleting an item from a user interface does not establish that every copy has immediately disappeared.

**Chapter sketch**

- Inventory retention separately for ChatGPT, Codex, API features, company systems and external integrations.
- Review deletion procedures, backups, security investigations and legally required preservation.
- Check Zero Data Retention (ZDR) eligibility and exclusions at model, feature, endpoint and project level.
- Document residency of stored information separately from location of processing.
- Define rules for gateway logs, caches, scanner evidence and troubleshooting exports.
- Assess local sessions, memories, application databases, project artefacts and their backups separately. Disabling `history.persistence` controls the named history feature; it is not evidence that every local persistence mechanism is disabled. Verify each store and the scope of any deletion command. [Configuration reference](https://learn.chatgpt.com/docs/config-file/config-reference).

OpenAI's API documentation distinguishes abuse-monitoring logs from application state, describes standard monitoring retention and sets out ZDR eligibility and exceptions. It also describes circumstances under which safety retention can affect eligible customers. These API provisions must not be generalized to all ChatGPT or Codex usage. [OpenAI data controls](https://developers.openai.com/api/docs/guides/your-data).

**Planned output:** A retention schedule identifying content, location, duration, deletion mechanism and exceptions.

