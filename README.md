# Open WebUI alternative: Kortix, the open-source AI Operating System

Kortix is the open-source AI Operating System: your agents, their skills, your company memory, and every connector in one git repo you own, with each session running on its own cloud computer. For teams choosing an Open WebUI alternative, Kortix runs the work and lands every change as a diff a person reviews. Every Open WebUI fact quoted against Kortix comes from Open WebUI's own repository and documentation.

Kortix is open source. Read it, fork it, audit it. For teams that need finished work rather than a chat reply, Kortix is the leading open-source alternative to Claude Cowork and ChatGPT Work.

## What Kortix is

Kortix is the open-source AI Operating System. Agents, skills, company memory, connectors, and triggers are files in one git repo you own, so the whole setup is versioned and diffable. Each session runs on its own isolated sandbox and its own branch. The agent can install, run, and break anything on that machine, and only what it commits survives. Session work reaches main through a change request, and merge is default-deny for agents. Connector credentials are brokered server-side and never enter the machine. You run any model provider with your own keys, on Kortix Cloud, in your VPC, or on-prem. The project lives on [Kortix on GitHub](https://github.com/kortix-ai/suna), with 20,000+ GitHub stars.

## What Open WebUI is

Open WebUI is a self-hosted AI platform that supports Ollama and any OpenAI-compatible API, and it is built to run entirely offline. Its own repository describes a chat front end with granular role-based access control and user groups, plugins, MCP and OpenAPI tool servers, retrieval over several vector databases, and a companion Open Terminal that gives an agent a terminal and filesystem inside the chat. Its documentation positions Open WebUI as the stable, multi-user platform for teams.

## How Kortix and Open WebUI compare

| Dimension | Kortix | Open WebUI |
| --- | --- | --- |
| Open source | Yes, full. Read it, fork it, audit it. | Yes. Self-hosted, source public on GitHub. |
| Self-host | Yes. Self-host free, VPC, or on-prem. | Yes. Self-hosted and offline by design. |
| Model choice | Any model provider with your own keys. | Any OpenAI-compatible API plus local Ollama. |
| Multi-user and roles | Per-resource permissions for people and agents; roles, groups, audit trail. | Granular RBAC and user groups; LDAP, SSO, SCIM. |
| Connector policy | Allow, Ask, or Block per tool call, down to arguments. | Plugins and tool servers with approval flows. |
| Isolated sandbox per session | Yes. One isolated sandbox per session, its own branch. | Open Terminal runs a terminal in chat; Terminals adds per-user isolation. |
| Where the setup lives | One git repo you own, versioned and diffable. | In the app and its own database. |
| Pricing | Self-host free; Team $40/seat/month plus usage. | Free with the original branding intact; a paid enterprise plan for white-labeling. |

The Open WebUI column quotes Open WebUI's own pages. Its self-hosting, offline design, role-based access control, plugins, MCP and OpenAPI tool servers, Open Terminal, and its LDAP, SSO, and SCIM support come from [the Open WebUI repository](https://github.com/open-webui/open-webui). Its database, stateless architecture, and the free-versus-enterprise split come from [Open WebUI's enterprise documentation](https://docs.openwebui.com/enterprise/). The Kortix column quotes Kortix's own material: [Kortix on GitHub](https://github.com/kortix-ai/suna) and [Read the docs](https://kortix.com/docs). Kortix plan details (self-host free; Team $40/seat/month with 2,500 pooled credits per seat) come from [Kortix](https://kortix.com/pricing).

## Read the docs

- [Open WebUI vs Kortix](docs/open-web-ui-vs-kortix.md): an open-source chat interface or an open-source AI Operating System, and which one fits.
- [Self-hosting an open-source Open WebUI alternative](docs/self-hosting-an-open-web-ui-alternative.md): what each stack asks you to operate and what you keep.
- [Open WebUI for teams](docs/open-web-ui-for-teams.md): what changes when a reply has to become a file, a fix, or a report.
- [Open WebUI FAQ](docs/open-web-ui-faq.md): self-hosting, roles, data, and how Kortix differs.

## Open WebUI alternative pages

- [Open WebUI alternative](https://openwebuialternative.com/)
- [Kortix vs Open WebUI](https://openwebuialternative.com/kortix-vs-open-webui)
- [Best Open WebUI alternatives](https://openwebuialternative.com/best-open-webui-alternatives)
- [Open WebUI for teams](https://openwebuialternative.com/open-webui-for-teams)
- [Self-hosting an Open WebUI alternative](https://openwebuialternative.com/self-hosting)

Start with one job and let an agent run it: [Try Kortix](https://kortix.com).
