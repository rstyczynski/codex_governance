## 12. DLP and Agent Controls

DLP inspects content for defined sensitive information, while agent controls limit which information and systems an assistant can reach. Combining them can reduce accidental disclosure. The detection of a recognizable credential or known document must be distinguished from recognition of a novel business idea, which may have no reliable detectable signature.

**Chapter sketch**

- Define detection for synthetic credentials, personal data, document labels, known confidential passages and company-specific patterns.
- Place mandatory input checks before transmission to OpenAI. A response check protects subsequent delivery, not the confidentiality of a prompt already sent upstream.
- Configure a fail-closed response for mandatory scanner failure, with a controlled exception process.
- Establish coverage for attachments, images, tool results, streaming, batch operations and references to previously uploaded files. Treat untested paths as unapproved.
- Limit Codex file access, network access and tool privileges; treat retrieved instructions and repository content as potentially untrusted.
- Evaluate false positives and false negatives on realistic company examples.

LiteLLM distinguishes pre-call, post-call, parallel and logging-only guardrail modes. For the proposed no-disclosure requirement, use a supported blocking pre-call path: parallel checks may already send the request upstream, and logging-only checks do not prevent disclosure. [LiteLLM guardrail modes](https://docs.litellm.ai/docs/proxy/guardrails/quick_start). Third-party DLP product documentation can inform requirements, but its support for ChatGPT Web must not be assumed to include Codex or an API integration. [Palo Alto support matrix](https://docs.paloaltonetworks.com/ai-access-security/getting-started/whats-supported-with-ai-access-security).

**Planned output:** A detection policy, channel-coverage matrix and evidence that blocked test content did not reach the upstream endpoint.

