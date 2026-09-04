# Contract — Agency v0.1

## Purpose
Represents one governed Asset Agency or the Mother Agency as an organizational unit inside AgencyOS.

## Required fields
- `agency_id`
- `agency_type`
- `asset_id` when applicable
- `scope` (`mother`, `asset`, or future approved scope)
- `lifecycle_state`
- `dna_version_ref`
- `autonomy_level`
- `budget_ref`
- `policy_refs`
- `memory_namespace_ref`
- `created_at`
- `created_by`
- `status_reason`

## Invariants
- one Asset Agency governs one economic asset;
- `agency_id` is immutable;
- lifecycle state must follow `AGENCY_LIFECYCLE.md`;
- autonomy must be explicit and reversible;
- an Asset Agency cannot operate without an active AgencyDNA version;
- agency boundaries isolate permissions, memory, budget and failure domain;
- retirement preserves audit, economics and validated learning.

## Relationships
An Agency owns Jobs, emits Events, incurs Costs, is governed by Policies, uses Evidence and Decisions, and is traceable through AuditRecords.

## Lifecycle authority
Lifecycle transitions are governed actions. The transition itself must be represented as a Decision and Event where material.
