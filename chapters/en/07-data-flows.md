## 7. Data Flows in ChatGPT and Codex

A confidentiality decision requires a complete picture of what leaves the business environment. Relevant content includes the prompt as well as attachments, retrieved documents, code fragments and tool results added to the model's context. Running an agent on a company laptop does not by itself establish that inference occurs locally.

**Chapter sketch**

- Map ChatGPT messages, files, projects, memory, shared conversations and connected services where enabled.
- Map Codex instructions, selected files, command output, repository content and screenshots where applicable.
- Separate local execution, model inference, cloud task execution and third-party tool activity.
- Inventory data stored by the client, company chat interface, gateway, scanners, OpenAI and connected services.
- Define the boundary between a model request and auxiliary traffic such as authentication, plugins and MCP calls.

OpenAI's gateway documentation explicitly notes that a configured gateway route covers model-provider requests, while sign-in and other features can use separate paths. This distinction will drive the data-flow inventory. [OpenAI gateway documentation](https://learn.chatgpt.com/docs/enterprise/connect-to-a-gateway).

**Planned output:** Data-flow diagrams with recipients, processing locations and storage points for each approved workflow.

### 7.1 Configuration scopes and instructions

Codex supports system, user and project configuration. This is a hierarchy of settings, not evidence of three equivalent cache stores. For an assessment, record both the scope of a setting and the physical location of the data it controls.

| Scope | Examples | Confidentiality question |
| --- | --- | --- |
| System / organization | `/etc/codex/config.toml` and `/etc/codex/requirements.toml` on Unix; supported managed policies | Is this an overridable default or an enforced restriction? |
| User | `$CODEX_HOME/config.toml`, normally `~/.codex/config.toml` | Which projects inherit this user's providers, integrations and settings? |
| Project | Trusted repository `.codex/config.toml` files, including nested scopes | Which overrides apply to the current working directory? |
| Session | CLI flags and runtime overrides | Can the effective settings differ from the reviewed file? |

Configuration precedence and enforced requirements are separate mechanisms: placing a value in a system configuration file does not by itself make it immutable. Project layers are subject to trust and key-specific restrictions. [Configuration basics](https://learn.chatgpt.com/docs/config-file/config-basic), [configuration reference](https://learn.chatgpt.com/docs/config-file/config-reference).

Instruction files form another layer. User-level and project-level `AGENTS.md` files can contribute text to model context; they are guidance, not a replacement for sandbox or network enforcement. [Instruction discovery](https://learn.chatgpt.com/docs/agent-configuration/agents-md).

### 7.2 Local state, caches and project artefacts

`CODEX_HOME` defaults to `~/.codex` and is a root for user state. SQLite-backed state can be relocated through `sqlite_home` or `CODEX_SQLITE_HOME`. Actual paths must therefore be resolved for the selected client and host. [Environment variables](https://learn.chatgpt.com/docs/config-file/environment-variables).

| Data category | Location or example to inventory | Treatment in the assessment |
| --- | --- | --- |
| Credentials | File-based `auth.json` or OS credential storage | Authentication secrets, not disposable cache |
| Sessions and history | `$CODEX_HOME/sessions`, `archived_sessions`; `history.jsonl` where enabled | Potentially sensitive records, distinct from project source files |
| Runtime state and caches | Configured SQLite location and client-specific cache directories | Classify by actual contents; avoid assuming every cache contains prompts |
| Local memory, if enabled | `$CODEX_HOME/memories` | Derived information that may be reused in later chats |
| Project and tool artefacts | Repository changes, worktrees, generated files, test output and temporary files | Review retention, access and Git or backup replication |
| Application diagnostics | Client-specific log locations, potentially outside `CODEX_HOME` | Review before export or support submission |

Credential storage and user-state examples are described in [advanced configuration](https://learn.chatgpt.com/docs/config-file/config-advanced); session and application-log locations are documented in [troubleshooting](https://learn.chatgpt.com/docs/reference/troubleshooting). A project's conversation can be stored in user-level state: logical project association does not imply physical storage inside that repository.

ChatGPT web project context and local Codex state must be mapped separately. ChatGPT projects can share files and instructions across their chats. Codex local memories use a separate store from ChatGPT web memory; when enabled, useful information from eligible chats can become memory files. A cross-project confidentiality review must therefore check whether material can reappear through shared user-level instructions or memory. [Projects and chats](https://learn.chatgpt.com/docs/projects), [memory behaviour](https://learn.chatgpt.com/docs/customization/memories).

**Inventory requirement:** For each location, record owner, contents, permissions, encryption, backup or sync destinations, possible inclusion in model context, and deletion procedure. Include browser and OS-managed application storage where applicable. A local-storage label does not establish that content is never transmitted later, and remote retention controls do not remove local copies.

