# Contract — Event v0.1

## Purpose
Represents an immutable fact that occurred within AgencyOS or an external system relevant to AgencyOS.

## Required fields
- `event_id`
- `event_type`
- `scope`
- `agency_id` when agency-scoped
- `occurred_at`
- `recorded_at`
- `source_ref`
- `subject_ref`
- `data_refs`
- `correlation_ref`
- `causation_ref` when known
- `confidence` when externally inferred rather than directly observed

## Invariants
- Events describe facts, not requested work;
- Events are append-only; corrections create compensating or superseding events;
- an Event must identify its source;
- externally observed events may require reconciliation before triggering high-risk actions;
- local events remain local unless governance deliberately promotes their meaning.

## Relationships
Events may result from Jobs, trigger Policies or new Jobs, support learning, affect lifecycle state, and feed AuditRecords.
