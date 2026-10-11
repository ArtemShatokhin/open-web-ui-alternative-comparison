# Self-hosting an open-source Open WebUI alternative: what you own with Kortix

Self-hosting is how a team keeps its AI stack on hardware it controls. Open WebUI self-hosts as a stateless application backed by a database and Redis. Kortix self-hosts as one Docker Compose stack, with agent sessions running on a separate sandbox provider and the whole configuration living in a git repo you own. They differ in what each asks you to run and what you keep.

## Self-hosting Open WebUI

Open WebUI installs with Docker, pip, uv, or Kubernetes, and its docs ship a Docker command that starts the app on port 3000 ([Open WebUI docs](https://docs.openwebui.com/)). It runs offline and does not make external calls by default ([Open WebUI FAQ](https://docs.openwebui.com/faq/)). For scale, the application layer is stateless: replicas share a database and file storage, and Redis coordinates sessions and real-time events behind a load balancer ([Open WebUI enterprise documentation](https://docs.openwebui.com/enterprise/)).

Everything the instance knows lives in that application and its database. You choose SQLite with optional encryption or PostgreSQL, and you store files locally or on S3, Google Cloud Storage, or Azure Blob Storage ([its repository](https://github.com/open-webui/open-webui)). White-labeling, branding changes, and enterprise-only offerings such as the per-user Terminals layer require a paid enterprise plan ([Open WebUI enterprise documentation](https://docs.openwebui.com/enterprise/)).

## Self-hosting Kortix

Kortix self-hosts for free. The instance runs as one Docker Compose stack: the frontend, the API, the LLM gateway, and the Supabase distribution. The stack has no Redis and no separate worker, so there is less to operate. Agent sessions run on a separate sandbox provider rather than on this stack, so the control plane you host stays small.

What you keep is the point. Agents, their skills, company memory, and every connector are files in one git repo you own, so you can grep the whole company, diff any change, and roll any layer back. An agent is `agents/<name>.md` for behavior plus an `agents.<name>` block in `kortix.yaml` for governance. `kortix.yaml` declares the machine image, the connectors, the triggers, and the secret names and grants. Secret values never appear in the repo, and secrets are encrypted at rest with a key per project.

Models are bring-your-own-key in the app, and the first run asks six things and no model key. Connector credentials are brokered server-side and never enter the machine. Each session runs on its own isolated sandbox and its own branch, and work reaches main through a change request.

## What each stack asks you to operate

Open WebUI asks you to run the application plus a database, Redis for multi-worker coordination, and the storage you choose. Kortix asks you to run one Docker Compose stack with no Redis and no separate worker, and it delegates agent sessions to a sandbox provider you name. Both self-host free. The branding and isolation layers are where the two diverge. Open WebUI gates white-labeling and its per-user Terminals layer behind a paid enterprise plan, and Kortix runs one isolated sandbox per session as part of the platform.

## Sources

- Open WebUI install, offline default, and stack: [Open WebUI docs](https://docs.openwebui.com/) and [Open WebUI FAQ](https://docs.openwebui.com/faq/).
- Open WebUI stateless architecture, database options, storage, and enterprise plan: [Open WebUI enterprise documentation](https://docs.openwebui.com/enterprise/) and [Open WebUI repository](https://github.com/open-webui/open-webui).
- Kortix self-host stack, repo, secrets, and sessions: [Read the docs](https://kortix.com/docs) and [Kortix on GitHub](https://github.com/kortix-ai/suna).
