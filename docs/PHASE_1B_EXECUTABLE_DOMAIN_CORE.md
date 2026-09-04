# FASE 1B — Executable Domain Core

**Status:** Authorized by Gustavo  
**Architecture:** AgencyOS v0.1  
**Scope:** minimum executable core, local-only, no external integrations

## 1. Mission

Transform the canonical Domain Contracts v0.1 into the first executable core of AgencyOS without changing the founding architecture and without connecting any external provider.

The purpose of this phase is not to build the final platform. It is to prove that the operating model can exist as software and preserve governance, evidence, economics and auditability from the first executable scenario.

## 2. Success statement

FASE 1B is successful when AgencyOS can execute a local demonstration in which:

```text
Mother Agency
→ creates a test Asset Agency
→ loads AgencyDNA v0.1
→ creates a Job
→ attaches Evidence
→ evaluates Policy
→ records a governed Decision when required
→ records CostRecord
→ transitions the Job to completion
→ emits Event
→ creates AuditRecord
→ reconstructs the complete execution trace
```

The demonstration must use only local/in-memory components.

## 3. Technical foundation approved for this phase

The initial implementation foundation is:

- **Python** as the primary language;
- **Pydantic** for validation of domain models and contracts;
- **pytest** for automated tests;
- **FastAPI** is approved as the future application/API boundary, but must not be allowed to shape the domain core in FASE 1B.

The domain layer must remain usable without FastAPI.

No database, queue, cloud or external API is selected in this phase.

## 4. Architectural boundaries

The executable core must preserve these boundaries:

### Domain
Owns canonical concepts, invariants and state-transition rules.

### Application
Coordinates use cases and scenarios using domain objects.

### Infrastructure
Contains replaceable local adapters, initially in-memory only.

### Interfaces
May contain a minimal local demonstration entrypoint. No public production API is required.

Dependencies must point inward. Domain code must not import infrastructure, FastAPI, YouTube, OpenAI, Anthropic, n8n or any external business provider.

## 5. Proposed repository structure

```text
platform/
├── README.md
├── pyproject.toml
├── src/
│   └── agencyos/
│       ├── __init__.py
│       ├── domain/
│       │   ├── __init__.py
│       │   ├── enums.py
│       │   ├── errors.py
│       │   ├── models/
│       │   │   ├── agency.py
│       │   │   ├── agency_dna.py
│       │   │   ├── job.py
│       │   │   ├── event.py
│       │   │   ├── decision.py
│       │   │   ├── evidence.py
│       │   │   ├── policy.py
│       │   │   ├── audit_record.py
│       │   │   └── cost_record.py
│       │   └── services/
│       │       ├── lifecycle.py
│       │       ├── governance.py
│       │       └── audit.py
│       ├── application/
│       │   ├── __init__.py
│       │   └── scenarios/
│       │       └── first_pulse.py
│       └── infrastructure/
│           ├── __init__.py
│           └── in_memory/
│               ├── agency_repository.py
│               ├── job_repository.py
│               ├── event_store.py
│               └── audit_store.py
└── tests/
    ├── unit/
    ├── integration/
    └── acceptance/
        └── test_first_pulse.py
```

Exact file grouping may be simplified if needed, but the separation of domain, application and infrastructure must remain.

## 6. Minimum executable domain objects

The code must implement the semantics defined in `docs/DOMAIN_CONTRACTS.md` and `docs/contracts/` for:

- `Agency`
- `AgencyDNA`
- `Job`
- `Event`
- `Decision`
- `Evidence`
- `Policy`
- `AuditRecord`
- `CostRecord`

Implementation may add internal value objects such as identifiers, money and references, provided they do not change the approved domain meaning.

## 7. Required invariants

At minimum, automated tests must prove:

1. an Asset Agency cannot exist without a valid AgencyDNA reference;
2. lifecycle state changes are explicit and validated;
3. a Job belongs to an explicit scope/agency;
4. Event represents a fact that occurred and is immutable after creation;
5. material approval cannot be performed solely by the creator of the governed output;
6. Evidence carries provenance and cannot be treated as canonical truth merely because a model generated it;
7. CostRecord always includes amount and currency and is attributable to scope;
8. AuditRecord can reference actor, versions, evidence/data, decision, cost and result;
9. historical Event/Evidence/Decision/AuditRecord corrections preserve prior history rather than silently replacing it;
10. an agency cannot exceed its explicit autonomy/permission boundary in the demonstration scenario.

## 8. First Pulse acceptance scenario

The acceptance test must create a deterministic example with synthetic data only.

Suggested narrative:

1. Mother Agency authorizes creation of `youtube_test_001`.
2. A valid AgencyDNA v0.1 is loaded with autonomy `L1` and a zero/fictional test budget.
3. The agency enters a non-production state.
4. A Job `research_opportunity` is created.
5. Synthetic Evidence is attached with explicit provenance `test_fixture`.
6. A Policy marks the next material action as requiring approval.
7. Actor A creates/proposes the result.
8. Actor B, distinct from Actor A, records the approval Decision.
9. A fictional CostRecord is created (for example BRL 0.00 or a deterministic test amount).
10. The Job completes.
11. `JOB_COMPLETED` Event is emitted.
12. AuditRecord is generated.
13. The scenario outputs/reconstructs a trace proving the whole chain.

No network call is allowed.

## 9. Test strategy

### Unit tests
Validate model invariants and state transitions in isolation.

### Integration tests
Validate application use cases against in-memory repositories/stores.

### Acceptance test
Validate the complete First Pulse scenario from agency creation to audit reconstruction.

Tests must be deterministic and run offline.

## 10. Definition of Done

FASE 1B is complete when all of the following are true:

- the minimum Python project can be installed/run locally;
- all nine canonical contracts have executable representations;
- domain logic is independent from external providers and web frameworks;
- in-memory adapters are sufficient to run the demonstration;
- automated tests pass offline;
- the First Pulse acceptance scenario passes;
- the audit trace demonstrates who/what acted, which version, which data/evidence, which decision, cost and result;
- prohibited scope remains absent;
- `PROJECT_STATUS.md` is updated with test evidence and next gate.

## 11. Explicitly prohibited in FASE 1B

Do **not** build:

- YouTube integration;
- Instagram integration;
- Claude/OpenAI/other model API integration;
- video, voice, image or thumbnail generation;
- n8n workflows;
- external MCP execution;
- production database;
- Redis/Kafka/RabbitMQ or another production queue;
- cloud deployment;
- authentication/OAuth implementation;
- secrets vault;
- paid integrations;
- production web dashboard;
- autonomous production agents;
- publishing;
- real money spending.

Do not add abstractions solely because they may be useful someday. Build only what is required to prove the First Pulse.

## 12. Codex execution rules

When Codex implements this phase it must:

1. read `PROJECT_STATUS.md` first;
2. read `docs/CONSTITUTION.md`;
3. read `docs/MASTER_PLAN.md`;
4. read `docs/DOMAIN_CONTRACTS.md` and every file under `docs/contracts/`;
5. read this specification;
6. preserve the architecture instead of redesigning it;
7. keep changes inside the authorized FASE 1B boundary;
8. write tests together with implementation;
9. never silently relax an invariant just to make tests pass;
10. document any conflict or ambiguity before choosing a behavior not already defined;
11. update `PROJECT_STATUS.md` when the implementation is complete;
12. stop at the FASE 1B gate and not advance automatically.

## 13. Decisions intentionally deferred

The following remain open after FASE 1B:

- production database;
- production event bus/queue;
- hosting/cloud;
- API authentication;
- secrets management;
- external model gateway providers;
- publishing integrations;
- media generation providers;
- UI/dashboard technology;
- production observability stack;
- distributed execution topology.

These must not be smuggled into the domain core through premature dependencies.
