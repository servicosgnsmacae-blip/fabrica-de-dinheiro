# Domain Contracts — AgencyOS v0.1

**Status:** Draft for architectural approval  
**Workstream:** FASE 1A — Domain Contracts  
**Nature:** technology-neutral, storage-neutral, provider-neutral

## 1. Purpose

This document turns the approved AgencyOS architecture into explicit domain contracts before implementation begins. These contracts define the meaning, minimum fields, invariants and relationships of the core objects that the future platform must understand.

They are **not database schemas, API payloads or programming-language classes**. Implementation must conform to these contracts rather than redefining the business model around a chosen technology.

## 2. Constitutional constraints

All contracts inherit the rules in `CONSTITUTION.md`, especially:

- the Mother Agency governs and Asset Agencies execute;
- creation and approval are separated for material work;
- AI is not a source of truth;
- important facts require provenance;
- relevant actions are auditable;
- institutional memory belongs to AgencyOS;
- blast radius is limited by agency boundaries;
- providers are replaceable;
- autonomy is explicit, progressive and reversible;
- economics governs scale;
- material evolution uses controlled experimentation and Champion/Challenger.

## 3. Canonical contracts

FASE 1A defines nine canonical contracts:

1. `Agency`
2. `AgencyDNA`
3. `Job`
4. `Event`
5. `Decision`
6. `Evidence`
7. `Policy`
8. `AuditRecord`
9. `CostRecord`

Detailed definitions live in `docs/contracts/`.

## 4. Common primitives

The contracts use conceptual primitives so they remain independent of language, framework and storage technology.

### Identifier
Opaque, globally unique and immutable identity. Business meaning must not be encoded into the identifier.

### Version
Immutable semantic identity of a specification or behavior. Material changes create a new version rather than silently overwriting the old one.

### Timestamp
An unambiguous point in time. Implementation format remains open, but ordering and timezone interpretation must never be ambiguous.

### Reference
A stable reference to another platform object, external source or evidence item. References must be resolvable through the owning domain.

### Money
Amount plus currency. A bare numeric value is not a valid money value.

### ActorRef
Identity of the human, agent, service or system component that performed or approved an action.

### ModelRef
Provider-neutral reference to an AI model invocation identity, including model/provider and version where applicable. Non-AI actions explicitly use `not_applicable` rather than omitting auditability.

### DataRef
Reference to data used in a decision or action. Canonical data should be referenced rather than copied into every record.

## 5. Global invariants

### 5.1 Immutability of history
Past evidence, decisions, audit records and events are not silently rewritten. Corrections create new records that supersede or amend prior records while preserving history.

### 5.2 Explicit scope
Every operational record must state whether it belongs to a specific Asset Agency, the Mother Agency or the portfolio.

### 5.3 Explicit versioning
Materially governing specifications must be versioned. Active behavior must be attributable to the exact version that governed it.

### 5.4 Separation of duties
For material outputs, the actor that creates the output cannot be its sole final approver. Approval must be represented explicitly through a `Decision` or equivalent governed record.

### 5.5 Provenance
Claims that materially affect publication, finance, policy, lifecycle, learning or capital allocation must be traceable to `Evidence` and/or canonical domain data.

### 5.6 Audit completeness
A relevant action must be reconstructable from platform records. At minimum, AgencyOS must be able to determine:

- who/what acted;
- which agent/model/tool version was involved, if any;
- which data and evidence were used;
- which policies governed the action;
- what decision authorized it where required;
- what it cost;
- what result occurred;
- when it happened;
- whether retries, failures or corrections occurred.

### 5.7 Provider neutrality
Provider names may appear as runtime metadata, but no core contract may depend on one provider being permanently present.

### 5.8 Bounded failure
Agency-scoped jobs, events, costs, policies and memory must preserve the agency boundary unless a deliberately governed portfolio action promotes or shares them.

## 6. Relationship map

```text
Mother Agency / Portfolio
        │
        ├── governs ─────────────── Policy
        │                              │
        │                              ▼
        └── creates/governs ─────── Agency
                                      │
                                      ├── governed by ─── AgencyDNA
                                      │
                                      ├── owns ────────── Job
                                      │                    │
                                      │                    ├── uses ───── Evidence
                                      │                    ├── authorized by Decision
                                      │                    ├── incurs ─── CostRecord
                                      │                    ├── emits ──── Event
                                      │                    └── traced by AuditRecord
                                      │
                                      └── accumulates governed memory from
                                           Events + Decisions + Evidence + Outcomes
```

## 7. Source-of-truth boundaries

The contracts distinguish interpretation from canonical truth:

- agency lifecycle state belongs to the Agency Registry domain;
- governing rules belong to the Policy/Governance domain;
- costs belong to the Finance domain;
- execution state belongs to the Job domain;
- facts that occurred belong to the Event domain;
- external or experimental support belongs to Evidence;
- material approvals and choices belong to Decision;
- reconstructability belongs to AuditRecord.

Models may analyze these objects but must not replace them as canonical records.

## 8. FASE 1A completion gate

FASE 1A is ready for approval when:

- all nine contracts exist;
- each has purpose, required fields, invariants, lifecycle/status semantics where applicable and relationships;
- the contracts do not choose database, framework, queue, cloud or external provider;
- the contracts are mutually coherent with the Master Plan, Constitution and existing architecture;
- open implementation choices remain explicitly open;
- `PROJECT_STATUS.md` and `DECISIONS.md` reflect the new workstream.

Approval of these documents authorizes later implementation work inside FASE 1, but **does not authorize external APIs, content production, publication, production databases or paid integrations**.

## 9. Open implementation questions intentionally deferred

- concrete data types and serialization format;
- database technology;
- event bus or queue technology;
- transaction model;
- ID generation algorithm;
- storage topology;
- exact retention periods;
- cryptographic integrity/hash strategy;
- schema migration mechanism;
- service boundaries and deployment topology.

These are implementation decisions, not domain-contract decisions.
