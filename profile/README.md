# Hi, this is Oximy 👋
Oximy is the company behind **OISP** and **OISP Sensor**.

We’re building the open foundation for **AI and agent activity observability**—so teams can understand what AI tools are running, what data is being sent to providers, and what actions agents take after responses.

Our approach starts at the lowest layer that still preserves meaning: the **system boundary** (process, file, and network), not per-app SDK hooks and not a proxy that you have to wedge into every workflow.

## What we build
### OISP (Open Inference Standard Protocol)
An open, OpenTelemetry-style specification for AI/agent activity.

OISP defines:
- a common event model for AI requests/responses and agent actions
- semantic conventions for providers, models, apps, and environments
- a portable format so capture once, export anywhere

### OISP Sensor (Open Source)
A system-boundary sensor that captures AI/agent activity with **zero application instrumentation**.

It discovers AI usage across real tools—browsers, IDEs, CLIs, local runtimes, and scripts—and emits OISP events that can be stored, queried, and exported.

OISP Sensor focuses on what matters for agents: not just “an API call happened,” but the chain of activity around it:
- AI request/response reconstruction (provider-aware where possible)
- tool invocations and results (when observable)
- process exec/exit
- file reads/writes
- network connects/DNS


## Why system-boundary capture
AI usage doesn’t live in one codebase anymore.

A single workflow can involve:
- a browser session using a hosted chat product
- an IDE agent reading and writing a repo
- a CLI agent running commands
- local model runtimes and custom scripts
- multiple providers and multiple identities

Per-app instrumentation can’t keep up with that. Network-only logging misses what agents do after a response. OISP Sensor is designed to see the full picture where it actually happens: at the OS boundary.


## Open source goals
We’re opinionated about keeping the foundation open:
- the event standard should be portable and vendor-neutral
- capture should be inspectable and verifiable
- exports should work with existing telemetry pipelines

If you’re building tooling around AI activity—security, governance, compliance, developer tooling, or analytics—OISP is meant to be the common language.

## The commercial layer
OISP and OISP Sensor are the foundation. Oximy is also building a commercial platform on top for teams that need:
- fleet management for sensors
- long-term storage and searchable traces across machines/servers
- detections and alerting
- policy and approvals for high-impact actions
- audit evidence and buyer-facing assurance

## Learn more
- OISP specification and documentation: https://oisp.dev
- OISP Sensor documentation: https://sensor.oisp.dev
- Oximy (commercial platform built on OISP): https://oximy.com


The design goal is simple: you can adopt the open source stack without lock-in, and add the platform when you need centralized control.
