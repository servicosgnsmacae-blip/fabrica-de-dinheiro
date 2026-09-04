# Project Status — AgencyOS

## What we are building
AgencyOS is the operating system of an autonomous digital-asset company. A Mother Agency governs isolated Asset Agencies that operate individual economic assets such as YouTube channels or Instagram profiles.

This project is **not** a collection of automations.

## Current state
- Architecture version: **v0.1**
- Project phase: **FASE 0 — Constituição e arquitetura**
- Implementation status: **blocked by design**
- Repository status: founding documentation being formalized

## Last decision taken
The approved Master Plan v0.1 is the founding architecture and source of truth for the project. The Constitution is subordinate only to explicit future architectural decisions approved by Gustavo.

## Current phase objective
Preserve and formalize the approved architecture without implementing production systems, external APIs, automations or content-generation agents.

## Next step
Review the complete FASE 0 documentation with Gustavo and obtain explicit authorization before beginning FASE 1 — Fundação técnica da plataforma.

## Existing blockers
No technical blocker currently identified. The intentional blocker is governance: **do not begin FASE 1 without Gustavo's authorization**.

## Explicitly prohibited at this stage
- production agents;
- video generation;
- YouTube publication;
- Instagram publication;
- external APIs;
- automations;
- production database;
- paid integrations.

## Open architectural decisions
- technology stack and programming language;
- database technology and storage topology;
- job queue/orchestration mechanism;
- cloud/hosting provider;
- canonical schema details for audit and provenance;
- exact accounting and shared-cost allocation method;
- retention periods for audit, evidence and operational data;
- authentication/secret-management implementation;
- first production-grade YouTube integration strategy;
- criteria and statistical thresholds for Champion/Challenger promotion.

## Session handoff
A new Codex session should first read, in order:
1. `PROJECT_STATUS.md`
2. `docs/CONSTITUTION.md`
3. `docs/MASTER_PLAN.md`
4. `DECISIONS.md`
5. `docs/ROADMAP.md`

Then it must stop and confirm the current phase before making implementation changes.
