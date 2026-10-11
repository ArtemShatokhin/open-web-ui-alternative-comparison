# Open WebUI FAQ: open-source self-hosting, roles, and the Kortix alternative

Teams comparing Open WebUI with Kortix, the open-source AI Operating System, ask a short set of questions. Each answer stands on its own. Open WebUI facts quote Open WebUI's own repository and documentation, and Kortix facts quote Kortix's own material.

## Is Open WebUI open source?

Yes. Open WebUI is a self-hosted AI platform whose source is public on GitHub, and the project describes itself as built for open-source AI ([its repository](https://github.com/open-webui/open-webui)). Kortix is also open source: read it, fork it, audit it. Both can run on hardware you control.

## Can Open WebUI run without internet access?

Yes. Open WebUI is designed to run offline and in air-gapped networks, and it does not send data to external services by default. If you connect an external model provider, prompts and responses go to that provider, while everything else runs and is stored locally ([Open WebUI FAQ](https://docs.openwebui.com/faq/)).

## Does Open WebUI support multiple users and roles?

Yes. Administrators define roles, groups, and permissions, and each group gets its own experience. Identity integrations cover LDAP, Active Directory, SSO, and SCIM 2.0 provisioning ([its repository](https://github.com/open-webui/open-webui)). Kortix adds per-resource permissions for people and agents, alongside roles, groups, and an audit trail.

## How much does Open WebUI cost?

Open WebUI is free to use self-hosted, as long as the original branding stays intact. White-labeling, rebranding, and enterprise-only offerings such as the Terminals layer require a paid enterprise plan. Open WebUI does not publish its enterprise pricing; it is arranged with its sales team, and it is available only to registered organizations ([Open WebUI enterprise documentation](https://docs.openwebui.com/enterprise/)).

## How does Kortix pricing compare?

Kortix self-hosts for free. Its Team plan is $40/seat/month with 2,500 pooled credits per seat, and usage beyond the pool is topped up as needed ([Kortix](https://kortix.com/pricing)). Free includes 200 credits each month for sandbox compute and 1 project.

## What does Kortix add beyond an Open WebUI chat interface?

Kortix runs agents on their own cloud computers, takes real actions in your tools, and returns finished work such as decks, reports, code, and replies. Each session gets its own isolated sandbox and branch, and work reaches main through a change request with merge default-deny for agents ([Read the docs](https://kortix.com/docs)).

## Where can I read more?

- [Open WebUI vs Kortix](open-web-ui-vs-kortix.md)
- [Self-hosting an open-source Open WebUI alternative](self-hosting-an-open-web-ui-alternative.md)
- [Open WebUI for teams](open-web-ui-for-teams.md)
