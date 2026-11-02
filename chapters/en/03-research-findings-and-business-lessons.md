## 3. Research Findings and Business Lessons

The earlier research identified several ways a business can lose control of information when using AI. This chapter brings the OpenAI-related findings together as a basis for the governance analysis that follows. Employee disclosure, provider failure and suspected reuse of know-how require different evidence and controls. They should not be presented as interchangeable examples of data theft.

**Research status:** Sources rechecked on 2 November 2026. The account below distinguishes press reporting, statements by participants, provider findings and a court decision. The business requirements are proposed conclusions from this analysis.

### 3.1 Reported employee disclosure: Samsung, 2023

Cybersecurity Dive reported that Samsung employees submitted sensitive code and meeting material to ChatGPT. Its account relies on Korean press reporting; Samsung did not respond to its request for comment. This supports a reported disclosure through employee use, not a finding that OpenAI reused the material or disclosed it to other customers. [Incident reporting, 10 April 2023](https://www.cybersecuritydive.com/news/Samsung-Electronics-ChatGPT-leak-data-privacy/647219/).

**Business lesson:** An employee's authority to read a file should be assessed separately from permission to send it to an external AI service. Approval should identify the permitted information, task and access route.

### 3.2 Provider failure: ChatGPT, March 2023

OpenAI reported that a bug allowed some users to see other users' conversation titles and possibly a first message. Payment-related information was potentially exposed for 1.2% of Plus subscribers active during a specific nine-hour window. Full card numbers were not exposed. This was a provider-reported isolation failure, not evidence of model training on leaked data. [OpenAI incident report, 24 March 2023](https://openai.com/index/march-20-chatgpt-outage/).

**Business lesson:** Correct employee behaviour does not eliminate provider risk. Supplier assessment should include incident notification, investigation support and the sensitivity of information entrusted to the service.

### 3.3 Unpublished research: what the mathematics dispute establishes

The preceding chapter introduces the dispute. The primary accounts support this narrower evidence summary:

| Evidence | What it establishes | What it does not establish |
| --- | --- | --- |
| Buckmaster's statement | He describes a personal collaboration with Alpöge, drafts entered into Codex, and uncertainty about their use | Institutional action by Anthropic or proven appropriation |
| OpenAI's 10 September 2026 update | OpenAI states that its investigation excluded influence from Buckmaster's Codex prompts in the preceding two months, including through training | An independent audit or a finding about every user's data |

Sources: [Buckmaster's statement](https://cims.nyu.edu/~tristanb/statement.pdf), [OpenAI's account and update](https://openai.com/index/navier-stokes-solution/).

**Business lesson:** Similarity and timing can raise questions but do not establish causation. A company needs dated work records and a record of what it submitted, under which account, settings and contractual terms. Personal information is only one concern: an unpublished method may retain its commercial value even after names are removed.

### 3.4 Legal proceedings: distinguish allegations from the operative decision

Italy's Garante announced a €15 million penalty concerning ChatGPT in 2024. Its updated notice records the successful challenge in March 2026. [Regulator's notice and update](https://www.garanteprivacy.it/home/docweb/-/docweb-display/docweb/10085432).

On 18 March 2026, the Rome court annulled the decision on grounds concerning the regulator's competence under the GDPR cooperation framework. The other grounds were not determined. The penalty should therefore not be presented as still operative, nor the annulment as a merits finding clearing every alleged practice. This proceeding is distinct from the mathematics dispute. [Judgment, especially concluding reasons and operative part](https://dei.web.uniroma1.it/sites/default/files/allegati/2026-05/Trib_Roma_OpenAI_Garante_2026.pdf).

**Business lesson:** A case register should record the procedural stage, decision date, outcome and scope. An allegation, a regulatory decision and a court judgment carry different evidential weight.

### 3.5 Requirements carried into the governance analysis

The following are proposed company requirements derived from the cases, rather than findings about existing product capabilities:

| Business concern | Proposed requirement | Evidence for approval |
| --- | --- | --- |
| Unapproved submission | Information-owner approval and minimum necessary disclosure | Classification, permitted task and approved route |
| Provider failure | Defined incident responsibilities and acceptable exposure | Notification terms, contacts and response procedure |
| Possible secondary use | Review permitted processing purposes beyond training | Applicable agreement, account settings and unresolved questions |
| Loss of research priority | Preserve provenance without creating unnecessary copies | Dated drafts, version identifiers and restricted submission records |
| Inability to investigate | Define evidence access and retention before use | Request identifiers, access records and supplier escalation route |

Do not copy confidential prompts into unrestricted logs merely to improve traceability. Record identifiers and metadata where sufficient; any necessary content archive needs its own access and retention rules.

**Output:** An evidence-based risk register feeding Chapter 4's governance decisions. For each use case, record the information at risk, failure scenario, proposed control, supporting evidence, remaining uncertainty and person authorized to accept that uncertainty.
