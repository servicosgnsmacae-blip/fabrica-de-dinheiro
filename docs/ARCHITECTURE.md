# Architecture — AgencyOS v0.1

## 1. Purpose

This document decomposes the approved Master Plan without changing it. AgencyOS is the operating system of an autonomous digital-asset company, organized around a Mother Agency that governs and Asset Agencies that execute.

## 2. Architectural layers

1. **Executive Layer** — Gustavo, final owner and capital allocator.
2. **Control Plane** — Mother Agency, responsible for portfolio governance, policy, capital allocation, agency creation, incidents and global learning.
3. **Agency Runtime** — isolated Asset Agencies that operate individual digital assets.
4. **Shared Services** — reusable capabilities such as model access, media production, publishing, analytics, finance, safety, connectors and identity.
5. **Data & Memory Plane** — institutional memory, events, metrics, costs, evidence and audit trails.

## 3. Mother Agency responsibilities

- maintain the agency registry and portfolio state;
- approve or reject new agency creation based on an investment thesis;
- allocate and constrain capital;
- define governance, policies and autonomy boundaries;
- monitor health, risk and performance;
- coordinate recovery, pause and retirement;
- manage global templates and reusable knowledge;
- prevent local findings from becoming global rules without controlled validation.

The Mother Agency does not directly produce routine content.

## 4. Asset Agency responsibilities

Each Asset Agency owns the operation of one economic asset. It must have:

- unique identity;
- Agency DNA;
- budget and economic objectives;
- memory namespace;
- autonomy level;
- allowed tools and models;
- operational roles;
- lifecycle state;
- metrics and health indicators;
- kill criteria.

## 5. Core platform modules

### Portfolio Manager
Portfolio visibility across agencies: state, revenue, cost, profit, ROI, risk, health and autonomy.

### Agency Factory
Creates agencies from approved, versioned templates after a valid thesis and specification exist.

### Opportunity Engine
Finds and ranks market opportunities. It creates candidates, not production agencies directly.

### Capital Allocator
Allocates budget according to economics, evidence, risk and portfolio priorities.

### Governance Engine
Defines permissions, policies, approvals, thresholds, prohibited actions and escalation rules.

### Incident Center
Receives and manages material exceptions such as policy violations, account suspension, monetization loss, abnormal cost and credential failure.

### Identity Service
Maintains asset, account, brand, clone, voice and persona identity references.

### Model Gateway
Abstracts AI providers and models so they are replaceable.

### Tool & Connector Registry
Catalogues approved tools, APIs, MCPs, internal services and their capabilities.

### Knowledge & Memory Engine
Owns institutional memory and separates episodic, semantic and procedural knowledge.

### Experimentation Engine
Runs controlled tests and Champion/Challenger evolution.

### Finance Engine
Tracks cost, revenue, margin, ROI, budgets and unit economics.

### Observability Engine
Provides executive, agency and technical visibility into decisions, jobs, failures, cost and outcomes.

### Policy & Safety Engine
Evaluates operational, factual, platform-policy, brand and rights-related constraints before important actions.

## 6. Jobs and events

Operational work is represented as **Jobs**. A job contains at least identity, agency, type, status, priority, inputs, outputs, executor, model, version, cost, timestamps, evidence and attempt number.

The platform also emits **Events**, such as `VIDEO_PUBLISHED`, `AGENCY_PAUSED`, `BUDGET_THRESHOLD_REACHED`, `MONETIZATION_ENABLED` or `COPYRIGHT_WARNING`.

Jobs describe work; events describe facts that occurred.

## 7. Source-of-truth model

Each domain must have a canonical source. AI outputs may interpret canonical data but do not replace it. Financial facts come from the finance domain, platform metrics from the relevant analytics source, policy from governance, and agency state from the registry.

## 8. Isolation

Asset Agencies must be isolated in identity, memory, permissions, budgets and failure domains. Shared services may be centralized, but a failure in one agency must not compromise another.

## 9. Replaceability

Providers are adapters behind platform-owned contracts. Claude, OpenAI, video tools, voice tools and external platforms must remain replaceable without redesigning AgencyOS.

## 10. Current architecture boundary

Architecture v0.1 defines responsibilities and contracts conceptually. It does not yet choose frameworks, databases, cloud providers, queues, orchestration engines or external APIs.
