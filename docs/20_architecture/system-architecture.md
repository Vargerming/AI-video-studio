# Efficient Studio — System Architecture (MVP Baseline)

## Goal
A modular pipeline to produce short-form videos with multilingual support, with strict QC gates and auditability.

## Core principles
- Source of truth: Sacred JSON (docs/50_sacred/sacred_master.json)
- Decisions are append-only: docs/40_decisions/Decision_Log_v1_0.md
- QC is mandatory: docs/30_qc/ (30s fragments + final review)
- No secrets in repo (public).

## System levels
- Level 1: manual pipeline + checklists
- Level 2: semi-automation (scripts, templates, repeatable steps)
- Level 3: orchestration + QC dashboards + multilingual workflow + analytics integration

## High-level modules
1) Generation Layer
   - video generation, image generation, audio/voice generation, subtitles
2) Orchestration & Agents
   - task planning, queueing, retries, state tracking
3) Production Control Layer
   - segment QC (≤30s) + final combined review, operator notes
4) Multilingual Support
   - language routing, translation, subtitles/captions, voice layer, multilingual UI
5) Storage & Versioning
   - repo docs, artifacts archive, cloud/local storage separation
6) Analytics
   - performance dashboards, workflow metrics, QC metrics

## Data flow (MVP)
Input -> Script/Brief -> Assets generation -> Segment assembly (≤30s) -> Fragment QC -> Batch merge -> Final QC -> Publish package -> Analytics

## Interfaces (what talks to what)
- Orchestrator reads Sacred JSON + templates
- QC layer reads pass/fail matrix + operator notes rules
- Multilingual module consumes the same script and emits localized audio/subtitles
- Storage keeps artifacts separate from source docs

## What is in the repo vs outside
In repo:
- docs/* (architecture, qc, roadmap, decisions, sacred)
Outside repo (or in docs/90_artifacts only):
- large media files, datasets, renders, secrets, credentials

## Open items
- [UNRESOLVED] exact toolchain versions (to be locked later)
- [UNRESOLVED] MVP scope boundaries per platform (YT/TikTok/etc.)