# Contract — CostRecord v0.1

## Purpose
Represents an attributable economic cost incurred by AgencyOS, an Agency, Job, content item, experiment or shared service.

## Required fields
- `cost_id`
- `scope`
- `agency_id` when applicable
- `job_id` when attributable to a Job
- `cost_type`
- `amount`
- `currency`
- `provider_ref` when applicable
- `resource_ref` when applicable
- `incurred_at`
- `recorded_at`
- `allocation_method` when shared
- `source_ref`
- `status`

## Status
At minimum: `ESTIMATED`, `RECORDED`, `RECONCILED`, `ADJUSTED`, `VOIDED`.

## Invariants
- amount without currency is invalid;
- direct costs should be attributed to the narrowest useful scope;
- shared costs must retain allocation method provenance;
- adjustments do not erase the original record;
- model/provider usage cost is financial data and must not be inferred only from model memory;
- cost records survive agency retirement according to retention policy.

## Relationships
CostRecords attach to Jobs, Agencies, experiments, content or shared services and feed Finance, Audit, budget controls and capital-allocation decisions.
