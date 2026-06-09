# Backend & Systems Engineer | AI Systems | FastAPI | PostgreSQL | Agent Infrastructure

I build automation pipelines, agent harnesses, and local-first systems where humans stay in the loop—inspectable context, explicit gates, and production-shaped backends (FastAPI, PostgreSQL, Docker, observability).

## Problem → Solution → Impact

- **Problem:** Agent workflows lose intent across sessions; untrusted content reaches LLMs; production ops lack inspectable, human-gated context.
- **Solution:** **Guard–Guide–Build** — SCP (input safety), OpenHarness (handoffs + gates), OpenGrimoire (context graph), plus production platform (CaptionPipeline / Platform API).
- **Impact:** CaptionPipeline (as-of **2025-12**): **256+** caption files, **330+** content hours, **<1%** errors across **9** production feeds ([case study](https://github.com/ManintheCrowds/media-ops-platform/blob/main/docs/portfolio/README.md)); SCP (as-of **2026-06**): **16/16** promptfoo tier probes (OWASP LLM01/LLM06); OpenHarness (as-of **2026-06**): harness pin-able by commit SHA, autoresearch Tier B **5/5** on foam-pkm + frontend-a2ui skills.

*Portfolio metrics SSOT:* [metrics.json](https://github.com/ManintheCrowds/media-ops-platform/blob/main/docs/portfolio/metrics.json) · refreshed `generated_at` via `refresh_metrics.ps1`

## How the proof set fits together

```mermaid
flowchart TB
  Intent[Human / Operator intent]
  OH[OpenHarness Guide]
  SCP[SCP Guard]
  WT[moltbook_watchtower Watch]
  AF[Arc_Forge Compounding]

  subgraph build [Build]
    MOP[media-ops-platform Platform]
    OG[OpenGrimoire Context]
  end

  Intent --> OH
  OH --> SCP
  SCP -->|gates tools| MOP
  SCP -->|gates tools| OG
  WT -.->|observe| SCP
  AF -.->|mirror| OH
  AF -.->|compound| OG
```

These six repos are the proof set—harness → watch → platform → context → compounding → safety.

## Evaluate in ~10 minutes

| Step | Repo | Command / link |
|------|------|----------------|
| 1 | [OpenHarness](https://github.com/ManintheCrowds/OpenHarness) | `python scripts/verify_script_index.py` (from repo root) |
| 2 | [SCP](https://github.com/ManintheCrowds/SCP) | `npx promptfoo eval` (see README § Testing) |
| 3 | [media-ops-platform](https://github.com/ManintheCrowds/media-ops-platform) | README Quick start — API + stack smoke |
| 4 | [OpenGrimoire](https://github.com/ManintheCrowds/OpenGrimoire) | `npm install && npm run dev` or [CI workflow](https://github.com/ManintheCrowds/OpenGrimoire/actions) |
| 5 | [Arc_Forge](https://github.com/ManintheCrowds/Arc_Forge) | `pytest` (workflow_ui suite) |

## Case studies

- **CaptionPipeline** — automated WhisperX → SCC captions across 9 feeds; as-of **2025-12**: 93.5%+ success, peaks 121 files/day → [portfolio kit](https://github.com/ManintheCrowds/media-ops-platform/tree/main/docs/portfolio/)
- **SCP guardrail** (as-of **2026-06**) — 16/16 promptfoo injection/reversal probes before LLM context → [SCP README § Impact](https://github.com/ManintheCrowds/SCP/blob/main/README.md)
- **Agent harness eval** — as-of **2026-06**: Tier B 5/5 on foam-pkm and frontend-a2ui skills → OpenHarness + MiscRepos autoresearch harness

## Stack

[![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![Next.js](https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=next.js&logoColor=white)](https://nextjs.org/)
[![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)](https://fastapi.tiangolo.com/)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)](https://www.postgresql.org/)
[![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)](https://www.docker.com/)
[![MCP](https://img.shields.io/badge/MCP-30333a?style=for-the-badge)](https://modelcontextprotocol.io/)
[![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=for-the-badge&logo=prometheus&logoColor=white)](https://prometheus.io/)

## CI (pinned proof set)

[![OpenHarness CI](https://github.com/ManintheCrowds/OpenHarness/actions/workflows/ci.yml/badge.svg)](https://github.com/ManintheCrowds/OpenHarness/actions/workflows/ci.yml)
[![SCP CI](https://github.com/ManintheCrowds/SCP/actions/workflows/ci.yml/badge.svg)](https://github.com/ManintheCrowds/SCP/actions/workflows/ci.yml)
[![media-ops tests](https://github.com/ManintheCrowds/media-ops-platform/actions/workflows/tests.yml/badge.svg)](https://github.com/ManintheCrowds/media-ops-platform/actions/workflows/tests.yml)
[![OpenGrimoire CI](https://github.com/ManintheCrowds/OpenGrimoire/actions/workflows/ci.yml/badge.svg)](https://github.com/ManintheCrowds/OpenGrimoire/actions/workflows/ci.yml)
[![Arc_Forge tests](https://github.com/ManintheCrowds/Arc_Forge/actions/workflows/workflow_ui_tests.yml/badge.svg)](https://github.com/ManintheCrowds/Arc_Forge/actions/workflows/workflow_ui_tests.yml)

## Skills

- Agent harnesses, handoffs, and intent-alignment gates
- Read-only observability and leak/injection analysis for agent networks
- Local-first context graphs and human↔agent alignment workflows
- LLM input safety (inspect, sanitize, contain, quarantine)
- FastAPI platform APIs, SSO/gateway patterns, homelab observability

## Pinned work

| Project | One line | CI |
|---------|----------|-----|
| [OpenHarness](https://github.com/ManintheCrowds/OpenHarness) | Portable harness: context engineering, handoff flow, intent alignment | [![CI](https://github.com/ManintheCrowds/OpenHarness/actions/workflows/ci.yml/badge.svg)](https://github.com/ManintheCrowds/OpenHarness/actions/workflows/ci.yml) |
| [moltbook_watchtower](https://github.com/ManintheCrowds/moltbook_watchtower) | Read-only observability for agent networks (leak / injection / behavior) | — |
| [media-ops-platform](https://github.com/ManintheCrowds/media-ops-platform) | **CaptionPipeline** + **Platform API** — video captions and homelab integration | [![tests](https://github.com/ManintheCrowds/media-ops-platform/actions/workflows/tests.yml/badge.svg)](https://github.com/ManintheCrowds/media-ops-platform/actions/workflows/tests.yml) |
| [OpenGrimoire](https://github.com/ManintheCrowds/OpenGrimoire) | Local-first context graph and Sync Session alignment workspace | [![CI](https://github.com/ManintheCrowds/OpenGrimoire/actions/workflows/ci.yml/badge.svg)](https://github.com/ManintheCrowds/OpenGrimoire/actions/workflows/ci.yml) |
| [Arc_Forge](https://github.com/ManintheCrowds/Arc_Forge) | Harness mirror + LLM-Wiki compounding in Obsidian | [![tests](https://github.com/ManintheCrowds/Arc_Forge/actions/workflows/workflow_ui_tests.yml/badge.svg)](https://github.com/ManintheCrowds/Arc_Forge/actions/workflows/workflow_ui_tests.yml) |
| [SCP](https://github.com/ManintheCrowds/SCP) | Secure Contain Protect — MCP guardrail for LLM inputs (OWASP LLM01/LLM06) | [![CI](https://github.com/ManintheCrowds/SCP/actions/workflows/ci.yml/badge.svg)](https://github.com/ManintheCrowds/SCP/actions/workflows/ci.yml) |

## Socials

Pending

Open an issue on any pinned repo for collaboration or questions.
