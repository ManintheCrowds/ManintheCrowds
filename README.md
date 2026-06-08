# Python Backend Engineer | AI Systems | FastAPI | PostgreSQL | Agent Infrastructure

I build automation pipelines, agent harnesses, and local-first systems where humans stay in the loop—inspectable context, explicit gates, and production-shaped backends (FastAPI, PostgreSQL, Docker, observability).

## Problem → Solution → Impact

- **Problem:** Agent workflows lose intent across sessions; untrusted content reaches LLMs; production ops lack inspectable, human-gated context.
- **Solution:** Guard–Guide–Build stack — SCP (input safety), OpenHarness (handoffs + gates), OpenGrimoire (context graph), plus production platform (CaptionPipeline / Platform API).
- **Impact:** CaptionPipeline: 256+ caption files, 330+ content hours, <1% errors across 9 production feeds; SCP: 16/16 promptfoo tier probes; OpenHarness: reusable harness pin-able by commit SHA.

## Stack

[![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)](https://fastapi.tiangolo.com/)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)](https://www.postgresql.org/)
[![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)](https://www.docker.com/)
[![MCP](https://img.shields.io/badge/MCP-30333a?style=for-the-badge)](https://modelcontextprotocol.io/)
[![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=for-the-badge&logo=prometheus&logoColor=white)](https://prometheus.io/)

## Skills

- Agent harnesses, handoffs, and intent-alignment gates
- Read-only observability and leak/injection analysis for agent networks
- Local-first context graphs and human↔agent alignment workflows
- LLM input safety (inspect, sanitize, contain, quarantine)
- FastAPI platform APIs, SSO/gateway patterns, homelab observability

## Pinned work

These six repos are the proof set—harness → watch → platform → context → compounding → safety.

| Project | One line |
|---------|----------|
| [OpenHarness](https://github.com/ManintheCrowds/OpenHarness) | Portable harness: context engineering, handoff flow, intent alignment |
| [moltbook_watchtower](https://github.com/ManintheCrowds/moltbook_watchtower) | Read-only observability for agent networks (leak / injection / behavior) |
| [media-ops-platform](https://github.com/ManintheCrowds/media-ops-platform) | **CaptionPipeline** + **Platform API** — video captions and homelab integration |
| [OpenGrimoire](https://github.com/ManintheCrowds/OpenGrimoire) | Local-first context graph and Sync Session alignment workspace |
| [Arc_Forge](https://github.com/ManintheCrowds/Arc_Forge) | Harness mirror + LLM-Wiki compounding in Obsidian |
| [SCP](https://github.com/ManintheCrowds/SCP) | Secure Contain Protect — MCP guardrail for LLM inputs (OWASP LLM01/LLM06) |

Portfolio case studies and audit artifacts: [media-ops-platform/docs/portfolio/](https://github.com/ManintheCrowds/media-ops-platform/tree/main/docs/portfolio/). SCP red-team evals: `npx promptfoo eval` in the SCP repo.

## Socials

Pending

Open an issue on any pinned repo for collaboration or questions.
