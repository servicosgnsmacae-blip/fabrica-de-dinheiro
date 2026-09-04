# Contract — AuditRecord v0.1

## Purpose
Represents the reconstructable trace of a relevant action or material state transition in AgencyOS.

## Required fields
- `audit_id`
- `scope`
- `agency_id` when applicable
- `action_type`
- `actor_ref`
- `agent_version_ref` when applicable
- `model_ref` when applicable
- `tool_ref` when applicable
- `policy_refs`
- `data_refs`
- `evidence_refs`
- `decision_refs`
- `input_refs`
- `output_refs`
- `cost_record_refs`
- `status`
- `attempt_number`
- `started_at`
- `finished_at`
- `result_summary`
- `error_ref` when applicable

## Invariants
- audit history is append-only;
- historical records remain attributable to exact versions used at execution time;
- absence of an AI model is explicit rather than silently omitted when relevant to interpretation;
- a material action must be reconstructable without depending on transient chat history;
- retries and corrections create distinct traceable records.

## Relationships
AuditRecords connect Agency, Job, Event, Decision, Evidence, Policy and CostRecord into a single traceable execution history.
