## 11. Proposed Architecture with LiteLLM

The proposed design uses a company-controlled gateway as the entry point for approved OpenAI model calls. LiteLLM is a candidate for that role and can be restricted to OpenAI backends. The design must identify which client requests actually traverse the gateway and what happens when inspection is unavailable.

```text
Managed user device or approved application
                  |
     Approved chat UI or configured Codex client
                  |
          Company LiteLLM gateway
                  |
     Input inspection before upstream transmission
                  |
          Approved OpenAI endpoint
                  |
     Response inspection before delivery to user

Parallel controls:
  - Restrict unapproved direct model access and public ChatGPT access.
  - Allow documented authentication and auxiliary routes as necessary.
  - Govern tool, plugin and MCP traffic separately.
```

**Chapter sketch**

- Start with a pilot using company applications and Codex CLI configured for approved OpenAI API access through LiteLLM.
- Select the upstream authentication and billing model explicitly. A ChatGPT subscription route is a separate design option, not an assumed equivalent to API-key access.
- Define model allowlists, user authentication, credentials, limits and administrative change control.
- Provide an approved chat interface if public ChatGPT is blocked; an API-backed interface is not automatically feature-equivalent to ChatGPT.
- Minimize content logging and caching; evaluate every scanner and logging destination as a recipient of information.
- Test each additional client, cloud feature and API operation before extending approval.

LiteLLM documents a Codex CLI integration. OpenAI also documents gateway routing and its boundaries. These establish a supported design direction, not complete coverage of every client or auxiliary connection. [LiteLLM Codex integration](https://docs.litellm.ai/docs/proxy/client_setup/codex_cli), [OpenAI gateway routing](https://learn.chatgpt.com/docs/enterprise/connect-to-a-gateway).

**Planned output:** A reviewed architecture with a route inventory, authentication decision and explicit coverage gaps.

