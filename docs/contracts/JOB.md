# Contract — Job v0.1

## Purpose
Represents one unit of operational work executed or attempted by AgencyOS.

## Required fields
- `job_id`
- `agency_id`
- `job_type`
- `status`
- `priority`
- `input_refs`
- `output_refs`
- `policy_refs`
- `evidence_refs`
- `executor_actor_ref`
- `model_ref` when applicable
- `tool_ref` when applicable
- `agent_version_ref`
- `attempt_number`
- `created_at`
- `started_at`
- `finished_at`
- `cost_record_refs`
- `decision_refs` when approval is required
- `error_ref` when failed

## Status semantics
At minimum: `QUEUED`, `RUNNING`, `SUCCEEDED`, `FAILED`, `CANCELLED`, `BLOCKED`.

## Invariants
- every Job belongs to exactly one scope, normally one Agency;
- retries increment attempt number and do not erase prior attempts;
- material Jobs requiring approval cannot become executable without the required Decision;
- Job success means execution completed, not necessarily that the intended business outcome occurred;
- external outcomes require reconciliation through Events and/or canonical domain state.

## Relationships
Jobs consume data and Evidence, obey Policies, may require Decisions, incur CostRecords, emit Events and produce AuditRecords.
