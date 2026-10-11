# Open WebUI vs Kortix: an open-source chat interface or an open-source AI Operating System

Open WebUI and Kortix are both open source and both run on infrastructure you control, but they sit at different layers. Open WebUI is a self-hosted chat platform over your models and documents. Kortix is the open-source AI Operating System, where agents run the work on their own cloud computers and land every change as a diff you review. They differ on the choices a team makes before it commits.

## The layer difference

Open WebUI is a self-hosted AI platform with support for Ollama and any OpenAI-compatible API, built to run entirely offline ([its repository](https://github.com/open-webui/open-webui)). Its center is the conversation: a chat window over models and documents, with plugins, retrieval, and web search.

Kortix is the open-source AI Operating System. Its center is the work: agents, skills, company memory, connectors, and triggers live in one git repo you own, and each session runs on its own isolated sandbox and branch. Session work reaches main through a change request, and merge is default-deny for agents.

The resemblance between the two ends at "both are open source and self-hostable." The unit of work differs. In a chat interface a person drives every turn. In Kortix a session runs an agent that can install, run, and break anything on its own machine, and only what it commits survives.

## At a glance

| What a team checks | Kortix | Open WebUI |
| --- | --- | --- |
| Unit of work | An agent session on its own sandbox and branch. | A conversation a person drives. |
| Where work lands | A change request a person reviews before merge. | The reply in the chat. |
| Setup source of truth | One git repo you own, versioned and diffable. | The application and its database. |
| Connectors | Allow, Ask, or Block per call, down to arguments. | Plugins and tool servers with approval flows. |
| Isolation | One isolated sandbox per session. | Open Terminal in chat; Terminals adds per-user isolation. |
| Pricing | Self-host free; Team $40/seat/month plus usage. | Free with branding intact; a paid enterprise plan for white-labeling. |

## Which one fits

- Choose Kortix when the job has to run: agents that use your tools, return finished deliverables, and land each change for review on the infrastructure you choose.
- Choose Open WebUI when you want a self-hosted chat and search interface over local and API models, with plugins, retrieval, and a wide model list.

Both keep data and models on hardware you control. The question is whether the output you need is an answer in a chat or a change you can read and merge.

## Sources

- Open WebUI platform description, model support, role-based access control, plugins, MCP and OpenAPI tool servers, Open Terminal, and Terminals: [Open WebUI repository](https://github.com/open-webui/open-webui).
- Open WebUI stateless architecture, database, and free-versus-enterprise split: [Open WebUI enterprise documentation](https://docs.openwebui.com/enterprise/).
- Kortix sandbox-per-session model, change-request path, connector policy, and repo-as-company: [Read the docs](https://kortix.com/docs) and [Kortix on GitHub](https://github.com/kortix-ai/suna).
- Kortix plans: [Kortix](https://kortix.com/pricing).
