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

## Open decisions
The following are intentionally unresolved and must not be guessed during FASE 0:

- implementation language and frameworks;
- production database;
- cloud/hosting provider;
- orchestration/queue technology;
- secrets and authentication architecture;
- concrete provider integrations;
- detailed audit/provenance schema;
- data retention periods;
- accounting allocation method;
- Champion/Challenger statistical thresholds.
