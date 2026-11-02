## References

Public sources below were consulted on **2 November 2026**. Retain effective dates separately from access dates. Living documentation and links should be rechecked before implementation. Vendor documentation establishes described functionality; deployment-specific guarantees require the applicable agreement, configuration and validation evidence.

### OpenAI agreements and technical documentation

1. **OpenAI. [Services Agreement](https://openai.com/policies/services-agreement/).** Page marked updated 1 December 2025 and effective 1 January 2026. Supports review of business-service scope, Customer Content, confidentiality and permitted processing. Relevant chapters: 4, 5, 7, 8, 9.
2. **OpenAI. [Usage Policies — revision effective 29 October 2025](https://openai.com/policies/usage-policies/revisions/2025-10-29/).** Acceptable-use reference for this draft's assessment date; not a substitute for provider confidentiality obligations. Relevant chapters: 4, 5.
3. **OpenAI. [Usage Policies — general page](https://openai.com/en-GB/policies/usage-policies/).** User-supplied reference. At consultation, displays a version effective 20 November 2026; track separately as forthcoming. Relevant chapter: 4.
4. **OpenAI. [Data controls in the OpenAI platform](https://developers.openai.com/api/docs/guides/your-data).** API data use, retention, ZDR, endpoint limitations and residency. Relevant chapters: 7, 9.
5. **OpenAI. [Codex authentication](https://learn.chatgpt.com/docs/auth).** Authentication routes and their relationship to administrative and data-handling controls. Relevant chapters: 6, 7, 10.
6. **OpenAI. [Connect to a gateway](https://learn.chatgpt.com/docs/enterprise/connect-to-a-gateway).** Gateway setup, upstream authentication and boundaries between model requests and other traffic. Relevant chapters: 6, 10, 11.
7. **OpenAI. [Codex security cookbook](https://learn.chatgpt.com/docs/enterprise/security-cookbook).** Enterprise configuration, verification and combination of access and action controls. Relevant chapters: 5, 8, 12, 13.

### Gateway, DLP and network controls

8. **LiteLLM. [Connect Codex CLI to LiteLLM](https://docs.litellm.ai/docs/proxy/client_setup/codex_cli).** Integration reference; validate against selected versions and authentication. Relevant chapter: 10.
9. **LiteLLM. [Guardrails — Quick Start](https://docs.litellm.ai/docs/proxy/guardrails/quick_start).** Inspection integrations and enforcement timing. Relevant chapters: 10, 12.
10. **LiteLLM. [Logging](https://docs.litellm.ai/docs/proxy/logging).** Logging destinations and controls; assess potential additional copies of content. Relevant chapters: 9, 10, 13.
11. **Oracle. [Overview of the Network Firewall Service](https://docs.oracle.com/en-us/iaas/Content/network-firewall/overview.htm).** OCI Network Firewall capabilities and routing scope. Relevant chapter: 11.
12. **Palo Alto Networks. [What Is Supported with AI Access Security](https://docs.paloaltonetworks.com/ai-access-security/getting-started/whats-supported-with-ai-access-security).** DLP application support and prerequisites; not evidence of feature inclusion in OCI Network Firewall. Relevant chapters: 11, 12.
13. **Cloudflare. [Set up HTTP filtering](https://developers.cloudflare.com/cloudflare-one/traffic-controls/get-started/http/).** Reference implementation for traffic steering, certificates and web inspection; no product selection is implied. Relevant chapter: 11.

### Research dispute and supplied context

14. **Tristan Buckmaster. [Public statement on work with Levent Alpöge and interactions with OpenAI](https://cims.nyu.edu/~tristanb/statement.pdf).** Researcher's primary account; distinguishes personal collaboration and uncertainty about data use. Relevant chapter: 2.
15. **OpenAI. [On the Navier–Stokes Millennium Prize Problem](https://openai.com/index/navier-stokes-solution/).** Published 8 September 2026, with an investigation update dated 10 September 2026. Provider's account and response to concerns. Relevant chapter: 2.
16. **Andrew Orlowski / Onet, source attributed to The Telegraph. [Article on mathematicians' allegations concerning their discoveries](https://wiadomosci.onet.pl/swiat/najwiekszy-skandal-w-historii-nauki-znani-matematycy-twierdza-ze-ai-ukradla-ich/4s4mvnq).** Published 16 September 2026. User-supplied secondary reporting for context, not independent proof of data misuse. Relevant chapter: 2.
17. **Krzysztof Sulikowski / GeekWeek Interia. [Article on OpenAI and Anthropic mathematics announcements](https://geekweek.interia.pl/technologia/sztuczna-inteligencja/news-wstrzas-w-nauce-openai-i-anthropic-przedstawily-dowody-tego,nId,23565804).** User-supplied secondary reporting on separate announcements; preserve the distinction from the private-session dispute. Relevant chapter: 2.
18. **User-supplied excerpt. Generative Chat at Oracle: Terms of Use & Disclaimer.** No public URL, version or effective date supplied. Used as a policy-design example only. Statements about CSSAP and Oracle Legal approval, Oracle-managed keys and permitted data classes have not been independently verified and do not establish equivalent protection for another deployment. Relevant chapter: 5.

### Local configuration and data lifecycle

19. **OpenAI. [Configuration basics](https://learn.chatgpt.com/docs/config-file/config-basic).** Configuration scopes, precedence and the distinction between defaults and enforced requirements. Relevant chapters: 6, 13.
20. **OpenAI. [Advanced configuration](https://learn.chatgpt.com/docs/config-file/config-advanced).** User configuration, project overrides and examples of local state and credential storage. Relevant chapters: 6, 9.
21. **OpenAI. [Environment variables](https://learn.chatgpt.com/docs/config-file/environment-variables).** `CODEX_HOME` and configurable SQLite state locations. Relevant chapter: 6.
22. **OpenAI. [Configuration reference](https://learn.chatgpt.com/docs/config-file/config-reference).** Supported keys and scope-specific restrictions; history settings must not be treated as global deletion controls. Relevant chapters: 6, 9, 13.
23. **OpenAI. [Custom instructions with AGENTS.md](https://learn.chatgpt.com/docs/agent-configuration/agents-md).** User and project instruction discovery and inclusion in context. Relevant chapters: 6, 12.
24. **OpenAI. [Memories](https://learn.chatgpt.com/docs/customization/memories).** Local Codex memory storage, reuse and controls, distinguished from ChatGPT web memory. Relevant chapters: 6, 9.
25. **OpenAI. [Troubleshooting](https://learn.chatgpt.com/docs/reference/troubleshooting).** Session, archived-session and application-log locations; review sensitive data before sharing diagnostics. Relevant chapters: 6, 9, 13.
26. **OpenAI. [Projects and chats](https://learn.chatgpt.com/docs/projects).** Shared ChatGPT project context, distinguished from local repository and Codex state. Relevant chapter: 6.

### Additional OpenAI policy and contract sources

27. **OpenAI. [Data Processing Addendum](https://openai.com/policies/data-processing-addendum/).** Updated 1 December 2025; effective 1 January 2026. Personal-data processing terms, instructions, breach notification, audit conditions and deletion. Relevant chapter: 4.
28. **OpenAI. [Europe Terms of Use](https://openai.com/policies/eu-terms-of-use/).** Updated 16 January 2026. Individual-service terms for the EEA, Switzerland and UK; distinct from business agreements. Relevant chapter: 4.
29. **OpenAI. [Europe Privacy Policy](https://openai.com/policies/eu-privacy-policy/).** Updated 24 August 2026. Personal-data privacy notice; its scope excludes business content processed on a customer's behalf. Relevant chapter: 4.
30. **OpenAI. [Service Terms](https://openai.com/policies/service-terms/).** Updated 16 October 2026. Additional feature-specific provisions. Relevant chapter: 4.
31. **OpenAI. [Enterprise privacy](https://openai.com/enterprise-privacy/).** Updated 8 January 2026. Provider descriptions of business-data protection and access. Relevant chapter: 4.
32. **OpenAI. [Sub-processor list](https://openai.com/policies/sub-processor-list/).** Updated 14 October 2026. Recipients, service scope, processing purposes and locations. Relevant chapter: 4.
33. **OpenAI. [How your data is used to improve model performance](https://openai.com/policies/how-your-data-is-used-to-improve-model-performance/).** Updated 13 March 2026. Individual and business training-use distinctions and data-sharing choices. Relevant chapter: 4.
