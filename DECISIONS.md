# Architectural Decisions — AgencyOS

This file is the permanent register of material architectural decisions. New decisions must not erase old ones; superseded decisions should be marked and linked to the replacing decision.

## DEC-001 — Agency-oriented architecture
**Status:** Accepted  
**Version:** v0.1

### Decision
AgencyOS is an operating system for an autonomous digital-asset company. The system is organized around a **Mother Agency** that governs and **Asset Agencies** that execute.

### Consequence
The project must not be treated as a collection of independent automations. Shared services, governance, memory, economics and lifecycle are platform concerns.

---

## DEC-002 — One Asset Agency per economic asset
**Status:** Accepted  
**Version:** v0.1

### Decision
Each Asset Agency is responsible for one economic asset and has isolated identity, memory, budget, permissions, lifecycle state and metrics.

### Consequence
Failure and learning remain bounded unless explicitly promoted through governance.

---

## DEC-003 — Creation and approval are separated
**Status:** Accepted  
**Version:** v0.1

### Decision
The creator of a material output cannot be its sole final approver.

### Consequence
Important production flows require independent validation proportional to risk.

---

## DEC-004 — AI is not a source of truth
**Status:** Accepted  
**Version:** v0.1

### Decision
Model memory or generated text cannot serve as canonical evidence for important facts.

### Consequence
Provenance, evidence and domain-specific sources of truth are required.

---

## DEC-005 — Institutional memory belongs to the platform
**Status:** Accepted  
**Version:** v0.1

### Decision
Durable knowledge must be stored in platform-owned memory structures, not depend on model conversations or transient context.

### Consequence
Learning requires explicit episodic, semantic and procedural memory.

---

## DEC-006 — Autonomy is progressive and reversible
**Status:** Accepted  
**Version:** v0.1

### Decision
Agencies and agents earn autonomy through evidence. Authority can be reduced if reliability, economics or risk deteriorate.

### Consequence
The platform must represent autonomy levels explicitly.

---

## DEC-007 — Economics governs scale
**Status:** Accepted  
**Version:** v0.1

### Decision
Sustainable economic performance and acceptable risk, not vanity metrics, govern capital allocation and scaling.

### Consequence
Costs and outcomes must be attributable to jobs, content, agencies and the portfolio where feasible.

---

## DEC-008 — Controlled evolution through Champion/Challenger
**Status:** Accepted  
**Version:** v0.1

### Decision
Material changes do not enter production directly. Proven behavior remains Champion while alternatives run as controlled Challengers.

### Consequence
Versioning, experiment evidence and rollback are required for important changes.

---

## DEC-009 — Providers must be replaceable
**Status:** Accepted  
**Version:** v0.1

### Decision
AI, media, publishing and other external providers are replaceable implementation components, not the architecture itself.

### Consequence
Platform-owned contracts and adapters should separate AgencyOS from vendor-specific behavior.

---

## DEC-010 — Prove one asset before portfolio scale
**Status:** Accepted  
**Version:** v0.1

### Decision
AgencyOS must prove one Asset Agency operating correctly end-to-end before scaling to many agencies.

### Consequence
The roadmap explicitly delays multi-agency scale until production, analytics, economics and controlled learning are proven.

---

## DEC-011 — Domain contracts precede implementation
**Status:** Accepted  
**Version:** v0.1

### Decision
FASE 1 begins by defining technology-neutral canonical contracts for `Agency`, `AgencyDNA`, `Job`, `Event`, `Decision`, `Evidence`, `Policy`, `AuditRecord` and `CostRecord` before choosing or implementing framework, database, queue, cloud or external providers.

### Consequence
Implementation must conform to platform-owned domain meaning instead of allowing a chosen technology or vendor to redefine AgencyOS. The contracts describe business semantics and invariants, not storage schemas or API payloads.

---

## DEC-012 — Jobs and Events are different domain facts
**Status:** Accepted  
**Version:** v0.1

### Decision
A `Job` represents requested/attempted operational work. An `Event` represents an immutable fact that occurred.

### Consequence
A successful Job does not automatically prove the intended real-world outcome. Reconciliation must use Events and canonical domain state.

---

## DEC-013 — Historical governance and evidence are append-only
**Status:** Accepted  
**Version:** v0.1

### Decision
Material Events, Evidence, Decisions and AuditRecords are not silently rewritten. Corrections or changes create new records that amend, supersede or compensate while preserving history.

### Consequence
AgencyOS can reconstruct what was known, decided and executed at the time, even after policies or conclusions evolve.

---

## DEC-014 — Initial implementation language is Python
**Status:** Accepted for FASE 1B  
**Version:** v0.1

### Decision
The first executable AgencyOS domain core will use Python as the implementation language, with Pydantic for domain validation and pytest for automated testing.

### Consequence
This choice is an implementation vehicle, not an architectural dependency. Domain meaning remains defined by the canonical contracts and must stay portable.

---

## DEC-015 — FastAPI is an interface boundary, not the domain core
**Status:** Accepted for FASE 1B  
**Version:** v0.1

### Decision
FastAPI is approved as a future application/API boundary, but FASE 1B domain code must remain executable without FastAPI and must not import or depend on it.

### Consequence
The domain remains framework-independent and can later be exposed through other interfaces if needed.

---

## DEC-016 — First executable persistence is in-memory only
**Status:** Accepted for FASE 1B  
**Version:** v0.1

### Decision
The First Pulse scenario will use local in-memory repositories/stores only. No production database, event bus, queue or external service will be selected or required.

### Consequence
FASE 1B proves domain behavior before infrastructure choices can distort or prematurely constrain the architecture.

---

## Open decisions
The following are intentionally unresolved after authorizing FASE 1B:

- production database;
- cloud/hosting provider;
- orchestration/queue technology;
- secrets and authentication architecture;
- concrete provider integrations;
- transaction model for production;
- production ID-generation policy;
- data retention periods;
- accounting and shared-cost allocation method;
- Champion/Challenger statistical thresholds;
- cryptographic integrity/hash strategy;
- schema migration mechanism;
- production API shape;
- dashboard/UI technology;
- distributed execution topology.
