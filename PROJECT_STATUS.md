# Project Status — AgencyOS

## What we are building
AgencyOS is the operating system of an autonomous digital-asset company. A Mother Agency governs isolated Asset Agencies that operate individual economic assets such as YouTube channels or Instagram profiles.

This project is **not** a collection of automations.

## Current state
- Architecture version: **v0.1**
- Project phase: **FASE 1A — Domain Contracts**
- FASE 0 status: **approved by Gustavo**
- Implementation status: **not started**
- Repository status: **founding architecture preserved; canonical domain contracts drafted**
- Review status: **no material contradiction identified between contracts and the v0.1 architecture**

## Last decision taken
Gustavo explicitly authorized advancement beyond FASE 0 and requested execution of the next step. FASE 1 begins with a technology-neutral contract layer before any executable platform code is implemented.

The canonical v0.1 domain contracts are:

1. `Agency`
2. `AgencyDNA`
3. `Job`
4. `Event`
5. `Decision`
6. `Evidence`
7. `Policy`
8. `AuditRecord`
9. `CostRecord`

The overview is in `docs/DOMAIN_CONTRACTS.md` and detailed contracts are in `docs/contracts/`.

## Current phase objective
Freeze the meaning, required fields, invariants and relationships of the core AgencyOS domain objects without choosing framework, database, cloud, queue, external APIs or paid providers.

## Current progress
- FASE 0 architecture: complete and approved;
- Domain Contract overview: created;
- nine canonical contracts: created;
- implementation technology: intentionally undecided;
- production code: none;
- external integrations: none.

## Next step
Architectural review of the Domain Contracts v0.1. After approval, continue inside FASE 1 with the minimum executable domain core and tests that demonstrate the contracts without external integrations.

## Existing blockers
No technical blocker currently identified. The intentional governance gate is: **do not implement external APIs, production agents, publication, content generation or paid integrations during FASE 1A**.

## Explicitly prohibited at this stage
- production agents;
- video generation;
- YouTube publication;
- Instagram publication;
- external APIs;
- automations;
- production database;
- paid integrations;
- vendor-specific architecture decisions disguised as domain rules.

## Open architectural/implementation decisions
These remain intentionally unresolved:

- technology stack and programming language;
- database technology and storage topology;
- job queue/orchestration mechanism;
- cloud/hosting provider;
- concrete serialization/data types;
- transaction model;
- ID generation algorithm;
- exact accounting and shared-cost allocation method;
- retention periods for audit, evidence and operational data;
- authentication/secret-management implementation;
- first production-grade YouTube integration strategy;
- criteria and statistical thresholds for Champion/Challenger promotion;
- cryptographic integrity/hash strategy for audit and evidence;
- schema migration mechanism.

## Coherence review
The Domain Contracts preserve the approved model:

- Mother Agency governs; Asset Agencies execute;
- one Asset Agency owns one economic asset;
- AgencyDNA is versioned and governs the agency;
- Jobs represent requested work; Events represent facts that occurred;
- Decisions represent governed choices and approvals;
- Evidence carries provenance;
- Policies represent explicit governing rules;
- AuditRecords reconstruct relevant actions;
- CostRecords make economics attributable;
- creation and approval remain separated;
- AI remains non-canonical as a source of truth;
- historical evidence and decisions are append-only/superseded, not silently rewritten;
- autonomy remains progressive and reversible;
- economic evidence governs scale;
- provider neutrality is preserved.

No material contradiction was identified. The contracts refine concepts already present in the Master Plan and architecture; they do not introduce a new operating model.

## Session handoff
A new Codex session should first read, in order:

1. `PROJECT_STATUS.md`
2. `docs/CONSTITUTION.md`
3. `docs/MASTER_PLAN.md`
4. `DECISIONS.md`
5. `docs/DOMAIN_CONTRACTS.md`
6. `docs/contracts/`
7. `docs/ROADMAP.md`

Then it must confirm that the active workstream is **FASE 1A — Domain Contracts** before making implementation changes.
