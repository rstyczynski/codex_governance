## References

Public sources below were consulted on **2 November 2026**. Retain effective dates separately from access dates. Living documentation and links should be rechecked before implementation. Vendor documentation establishes described functionality; deployment-specific guarantees require the applicable agreement, configuration and validation evidence.

### OpenAI agreements and technical documentation

1. **OpenAI. [Services Agreement](https://openai.com/policies/services-agreement/).** Page marked updated 1 December 2025 and effective 1 January 2026. Supports review of business-service scope, Customer Content, confidentiality and permitted processing. Relevant chapters: 5, 6, 8, 9, 10.
2. **OpenAI. [Usage Policies — revision effective 29 October 2025](https://openai.com/policies/usage-policies/revisions/2025-10-29/).** Acceptable-use reference for this draft's assessment date; not a substitute for provider confidentiality obligations. Relevant chapters: 5, 6.
3. **OpenAI. [Usage Policies — general page](https://openai.com/en-GB/policies/usage-policies/).** User-supplied reference. At consultation, displays a version effective 20 November 2026; track separately as forthcoming. Relevant chapter: 5.
4. **OpenAI. [Data controls in the OpenAI platform](https://developers.openai.com/api/docs/guides/your-data).** API data use, retention, ZDR, endpoint limitations and residency. Relevant chapters: 8, 10.
5. **OpenAI. [Codex authentication](https://learn.chatgpt.com/docs/auth).** Authentication routes and their relationship to administrative and data-handling controls. Relevant chapters: 7, 8, 11.
6. **OpenAI. [Connect to a gateway](https://learn.chatgpt.com/docs/enterprise/connect-to-a-gateway).** Gateway setup, upstream authentication and boundaries between model requests and other traffic. Relevant chapters: 7, 11, 12.
7. **OpenAI. [Codex security cookbook](https://learn.chatgpt.com/docs/enterprise/security-cookbook).** Enterprise configuration, verification and combination of access and action controls. Relevant chapters: 6, 9, 13, 14.

### Gateway, DLP and network controls

8. **LiteLLM. [Connect Codex CLI to LiteLLM](https://docs.litellm.ai/docs/proxy/client_setup/codex_cli).** Integration reference; validate against selected versions and authentication. Relevant chapter: 11.
9. **LiteLLM. [Guardrails — Quick Start](https://docs.litellm.ai/docs/proxy/guardrails/quick_start).** Inspection integrations and enforcement timing. Relevant chapters: 11, 13.
10. **LiteLLM. [Logging](https://docs.litellm.ai/docs/proxy/logging).** Logging destinations and controls; assess potential additional copies of content. Relevant chapters: 10, 11, 14.
11. **Oracle. [Overview of the Network Firewall Service](https://docs.oracle.com/en-us/iaas/Content/network-firewall/overview.htm).** OCI Network Firewall capabilities and routing scope. Relevant chapter: 12.
12. **Palo Alto Networks. [What Is Supported with AI Access Security](https://docs.paloaltonetworks.com/ai-access-security/getting-started/whats-supported-with-ai-access-security).** DLP application support and prerequisites; not evidence of feature inclusion in OCI Network Firewall. Relevant chapters: 12, 13.
13. **Cloudflare. [Set up HTTP filtering](https://developers.cloudflare.com/cloudflare-one/traffic-controls/get-started/http/).** Reference implementation for traffic steering, certificates and web inspection; no product selection is implied. Relevant chapter: 12.

### Research dispute and supplied context

14. **Tristan Buckmaster. [Public statement on work with Levent Alpöge and interactions with OpenAI](https://cims.nyu.edu/~tristanb/statement.pdf).** Researcher's primary account; distinguishes personal collaboration and uncertainty about data use. Relevant chapters: 2, 3.
15. **OpenAI. [On the Navier–Stokes Millennium Prize Problem](https://openai.com/index/navier-stokes-solution/).** Published 8 September 2026, with an investigation update dated 10 September 2026. Provider's account and response to concerns. Relevant chapters: 2, 3.
16. **Andrew Orlowski / Onet, source attributed to The Telegraph. [Article on mathematicians' allegations concerning their discoveries](https://wiadomosci.onet.pl/swiat/najwiekszy-skandal-w-historii-nauki-znani-matematycy-twierdza-ze-ai-ukradla-ich/4s4mvnq).** Published 16 September 2026. User-supplied secondary reporting for context, not independent proof of data misuse. Relevant chapter: 2.
17. **Krzysztof Sulikowski / GeekWeek Interia. [Article on OpenAI and Anthropic mathematics announcements](https://geekweek.interia.pl/technologia/sztuczna-inteligencja/news-wstrzas-w-nauce-openai-i-anthropic-przedstawily-dowody-tego,nId,23565804).** User-supplied secondary reporting on separate announcements; preserve the distinction from the private-session dispute. Relevant chapter: 2.
18. **User-supplied excerpt. Generative Chat at Oracle: Terms of Use & Disclaimer.** No public URL, version or effective date supplied. Used as a policy-design example only. Statements about CSSAP and Oracle Legal approval, Oracle-managed keys and permitted data classes have not been independently verified and do not establish equivalent protection for another deployment. Relevant chapter: 6.

### Local configuration and data lifecycle

19. **OpenAI. [Configuration basics](https://learn.chatgpt.com/docs/config-file/config-basic).** Configuration scopes, precedence and the distinction between defaults and enforced requirements. Relevant chapters: 7, 14.
20. **OpenAI. [Advanced configuration](https://learn.chatgpt.com/docs/config-file/config-advanced).** User configuration, project overrides and examples of local state and credential storage. Relevant chapters: 7, 10.
21. **OpenAI. [Environment variables](https://learn.chatgpt.com/docs/config-file/environment-variables).** `CODEX_HOME` and configurable SQLite state locations. Relevant chapter: 7.
22. **OpenAI. [Configuration reference](https://learn.chatgpt.com/docs/config-file/config-reference).** Supported keys and scope-specific restrictions; history settings must not be treated as global deletion controls. Relevant chapters: 7, 10, 14.
23. **OpenAI. [Custom instructions with AGENTS.md](https://learn.chatgpt.com/docs/agent-configuration/agents-md).** User and project instruction discovery and inclusion in context. Relevant chapters: 7, 13.
24. **OpenAI. [Memories](https://learn.chatgpt.com/docs/customization/memories).** Local Codex memory storage, reuse and controls, distinguished from ChatGPT web memory. Relevant chapters: 7, 10.
25. **OpenAI. [Troubleshooting](https://learn.chatgpt.com/docs/reference/troubleshooting).** Session, archived-session and application-log locations; review sensitive data before sharing diagnostics. Relevant chapters: 7, 10, 14.
26. **OpenAI. [Projects and chats](https://learn.chatgpt.com/docs/projects).** Shared ChatGPT project context, distinguished from local repository and Codex state. Relevant chapter: 7.

### Additional OpenAI policy and contract sources

27. **OpenAI. [Data Processing Addendum](https://openai.com/policies/data-processing-addendum/).** Updated 1 December 2025; effective 1 January 2026. Personal-data processing terms, instructions, breach notification, audit conditions and deletion. Relevant chapter: 5.
28. **OpenAI. [Europe Terms of Use](https://openai.com/policies/eu-terms-of-use/).** Updated 16 January 2026. Individual-service terms for the EEA, Switzerland and UK; distinct from business agreements. Relevant chapter: 5.
29. **OpenAI. [Europe Privacy Policy](https://openai.com/policies/eu-privacy-policy/).** Updated 24 August 2026. Personal-data privacy notice; its scope excludes business content processed on a customer's behalf. Relevant chapter: 5.
30. **OpenAI. [Service Terms](https://openai.com/policies/service-terms/).** Updated 16 October 2026. Additional feature-specific provisions. Relevant chapter: 5.
31. **OpenAI. [Enterprise privacy](https://openai.com/enterprise-privacy/).** Updated 8 January 2026. Provider descriptions of business-data protection and access. Relevant chapter: 5.
32. **OpenAI. [Sub-processor list](https://openai.com/policies/sub-processor-list/).** Updated 14 October 2026. Recipients, service scope, processing purposes and locations. Relevant chapter: 5.
33. **OpenAI. [How your data is used to improve model performance](https://openai.com/policies/how-your-data-is-used-to-improve-model-performance/).** Updated 13 March 2026. Individual and business training-use distinctions and data-sharing choices. Relevant chapter: 5.

### Additional incident and legal research

34. **Cybersecurity Dive. [Samsung employees leaked corporate data in ChatGPT: report](https://www.cybersecuritydive.com/news/Samsung-Electronics-ChatGPT-leak-data-privacy/647219/).** Published 10 April 2023; rechecked 2 November 2026. Secondary reporting of employee submissions, not evidence of subsequent provider reuse. Relevant chapter: 3.
35. **OpenAI. [March 20 ChatGPT outage: Here’s what happened](https://openai.com/index/march-20-chatgpt-outage/).** Published 24 March 2023; rechecked 2 November 2026. Provider incident report. Relevant chapter: 3.
36. **Garante. [ChatGPT investigation announcement, with court-outcome update](https://www.garanteprivacy.it/home/docweb/-/docweb-display/docweb/10085432).** Rechecked 2 November 2026; read the update alongside the original penalty announcement. Relevant chapter: 3.
37. **Tribunale di Roma. [Judgment in OpenAI's challenge to Garante decision 755/2024](https://dei.web.uniroma1.it/sites/default/files/allegati/2026-05/Trib_Roma_OpenAI_Garante_2026.pdf).** Decided 18 March 2026; copy hosted by Sapienza University, rechecked 2 November 2026. Grounds and operative outcome on pages 5–7. Relevant chapter: 3.

### Standards and EU AI Act mapping

Sources below were checked on 2 November 2026. They support Chapter 4 and Appendix A. The mapping is an author assessment, not a finding by ISO, NIST or the Commission.

38. **ISO. [ISO/IEC 42001:2023, edition 1](https://www.iso.org/standard/42001).** Official scope and management-system description; full normative text not reproduced.
39. **Kimberly Lucy / Microsoft. [Overview of ISO/IEC 42001, hosted by UNIDO](https://www.unido.org/sites/default/files/files/2025-07/Microsoft%20-%20Overview%20of%20ISO%20IEC%2042001.pdf).** Author-presented overview; slide 5 supports the clause structure, not a normative conformity assessment.
40. **NIST. [AI RMF 1.0 Core](https://airc.nist.gov/airmf-resources/airmf/5-sec-core/).** January 2023 framework; selected categories/subcategories used for the confidentiality mapping.
41. **NIST. [AI 600-1: Generative AI Profile](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.600-1.pdf).** July 2024; companion generative-AI risk context.
42. **EU. [Regulation (EU) 2024/1689, consolidated identifier 27 July 2026](https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=CELEX:02024R1689-20260727).** Consolidation identified by the Commission article explorer; current article texts consulted through the next reference.
43. **European Commission. [AI Act Explorer](https://ai-act-service-desk.ec.europa.eu/en/ai-act/article-2).** Articles 2, 3, 4, 5, 6, 25, 26, 27 and 50, individually linked in Appendix A; role and use-case applicability screening.
44. **European Commission. [Current AI Act implementation timeline](https://ai-act-service-desk.ec.europa.eu/en/ai-act/eu-ai-act-implementation-timeline).** Amended application dates and transitional milestones as at the assessment date.
45. **European Commission. [AI Act policy overview](https://digital-strategy.ec.europa.eu/en/policies/regulatory-framework-ai).** Distinguishes the regulatory areas relevant to the role-specific handoffs.

### Cloud and hosted source-code governance precedents

46. **AWS. [Shared Responsibility Model](https://aws.amazon.com/compliance/shared-responsibility-model/).** Provider/customer responsibility split, dependent on the selected service. Supports the governance analogy in Section 4.6, not an assertion of equivalent AI product controls.
47. **GitHub. [Available rules for rulesets](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-rulesets/available-rules-for-rulesets).** Configurable review and status-check enforcement, subject to platform scope and availability. Supports the change-control analogy in Section 4.6; Git version history alone does not enforce these controls.
48. **Oracle. [Oracle Contracts](https://www.oracle.com/contracts/).** Agreement, order and service-policy contract model, including CSA and OMA agreement families. Supports the business-level supplier-governance precedent in Section 4.6; not an assessment of a signed customer agreement.
49. **Oracle. [Cloud Services contracts](https://www.oracle.com/contracts/cloud-services/).** Entry point for applicable cloud agreements and related service specifications by product, country and language. Use the documents incorporated into the actual order when assessing OCI obligations; Section 4.6's comparison does not assert equivalent AI terms or require OCI deployment.
50. **Oracle. [Block Volume Encryption](https://docs.oracle.com/en-us/iaas/Content/Block/Concepts/blockvolumeencryption.htm).** Encryption at rest, Oracle-managed and customer-managed keys, and additional customer encryption. Supports Section 4.6's distinction between service decryption and contractual confidentiality; does not establish unrestricted personnel access.
51. **GitHub. [Terms of Service, Section E: Private Repositories](https://docs.github.com/en/site-policy/github-terms/github-terms-of-service#e-private-repositories).** Public terms effective 27 April 2026; confidentiality, permitted access and additional-feature provisions. Section 4.6 uses these as a public example; the customer's applicable enterprise or negotiated agreement must be checked separately.
52. **GitHub. [GitHub Actions secrets](https://docs.github.com/en/actions/concepts/security/secrets).** Explicitly describes GitHub's ability to decrypt uploaded secrets for workflow runtime injection. Section 4.6 distinguishes these credentials from confidential repository content.
