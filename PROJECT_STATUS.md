# Project Status — AgencyOS

## What we are building
AgencyOS is the operating system of an autonomous digital-asset company. A Mother Agency governs isolated Asset Agencies that operate individual economic assets such as YouTube channels or Instagram profiles.

This project is **not** a collection of automations.

## Current state
- Architecture version: **v0.1**
- Project phase: **FASE 1B — Executable Domain Core**
- FASE 0 status: **approved by Gustavo**
- FASE 1A status: **approved by Gustavo**
- Implementation status: **authorized, not yet implemented**
- Repository status: **founding architecture preserved; canonical domain contracts defined; FASE 1B specification created**
- Review status: **no material contradiction identified between the FASE 1B specification and the v0.1 architecture**

## Last decision taken
Gustavo authorized progression to the first executable AgencyOS core. The initial implementation vehicle for FASE 1B is Python with Pydantic and pytest. FastAPI is approved only as a future interface boundary and must not shape the domain core. Persistence for the First Pulse remains in-memory only.

The permanent decision record is in `DECISIONS.md` under DEC-014 through DEC-016.

## Current phase objective
Implement the minimum offline executable domain core that proves the approved contracts and governance model without any external integration.

The required acceptance flow is:

`Mother Agency → Asset Agency → AgencyDNA → Job → Evidence → Policy → Decision → CostRecord → Job completion → Event → AuditRecord → reconstructed trace`

## Current progress
- FASE 0 architecture: complete and approved;
- FASE 1A Domain Contracts: complete and approved;
- nine canonical contracts: defined;
- FASE 1B specification: `docs/PHASE_1B_EXECUTABLE_DOMAIN_CORE.md`;
- Python/Pydantic/pytest implementation vehicle: approved for FASE 1B;
- FastAPI: reserved as future interface boundary, not domain dependency;
- production code: not yet implemented;
- external integrations: none.

## Next step
Codex should implement FASE 1B exactly as specified in `docs/PHASE_1B_EXECUTABLE_DOMAIN_CORE.md`, together with offline automated tests and the deterministic `First Pulse` acceptance scenario.

After implementation, update this file with:

- files created;
- tests executed;
- test results;
- First Pulse trace evidence;
- deviations or ambiguities discovered;
- next governance gate.

Then stop. Do not advance automatically.

## Existing blockers
No technical blocker currently identified. The governance boundary is strict: implementation must remain local/offline and must not introduce production integrations, providers or infrastructure decisions beyond what FASE 1B requires.

## Explicitly prohibited in FASE 1B
- production agents;
- video generation;
- YouTube publication or API integration;
- Instagram publication or API integration;
- Claude/OpenAI/other model API integration;
- n8n workflows;
- external MCP execution;
- production database;
- production queue/event bus;
- cloud deployment;
- authentication/OAuth implementation;
- paid integrations;
- production dashboard;
- real money spending;
- vendor-specific architecture disguised as domain logic.

## Open architectural/implementation decisions
These remain intentionally unresolved:

- production database and storage topology;
- job queue/orchestration mechanism for production;
- cloud/hosting provider;
- transaction model for production;
- production ID generation policy;
- exact accounting and shared-cost allocation method;
- retention periods for audit, evidence and operational data;
- authentication/secret-management implementation;
- first production-grade YouTube integration strategy;
- criteria and statistical thresholds for Champion/Challenger promotion;
- cryptographic integrity/hash strategy for audit and evidence;
- schema migration mechanism;
- production API shape;
- dashboard/UI technology;
- distributed execution topology.

## Coherence review
The FASE 1B specification preserves the approved model:

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
- historical evidence and decisions remain append-only/superseded;
- autonomy remains progressive and reversible;
- economic evidence governs scale;
- provider neutrality is preserved;
- domain code remains independent from web framework and external infrastructure.

No material contradiction was identified.

## Session handoff
A new Codex session should first read, in order:

1. `PROJECT_STATUS.md`
2. `docs/CONSTITUTION.md`
3. `docs/MASTER_PLAN.md`
4. `DECISIONS.md`
5. `docs/DOMAIN_CONTRACTS.md`
6. `docs/contracts/`
7. `docs/PHASE_1B_EXECUTABLE_DOMAIN_CORE.md`
8. `docs/ROADMAP.md`

Then it may implement **FASE 1B — Executable Domain Core** only, run the offline tests, update `PROJECT_STATUS.md`, and stop at the next gate.
