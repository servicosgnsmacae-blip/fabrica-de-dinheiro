# Contract — Decision v0.1

## Purpose
Represents a material choice, approval, rejection, escalation or authorization made under AgencyOS governance.

## Required fields
- `decision_id`
- `scope`
- `agency_id` when applicable
- `decision_type`
- `decision_status`
- `proposed_by`
- `approved_by` or `rejected_by` when applicable
- `policy_refs`
- `evidence_refs`
- `data_refs`
- `options_considered`
- `selected_option`
- `rationale`
- `expected_outcome`
- `created_at`
- `effective_at`
- `review_at` when temporary or experimental

## Decision status
At minimum: `PROPOSED`, `APPROVED`, `REJECTED`, `EXPIRED`, `SUPERSEDED`.

## Invariants
- material approval must be explicit;
- creator and sole final approver cannot be the same actor when separation of duties applies;
- decisions must cite governing policy and supporting evidence/data;
- decisions are not silently edited; later changes supersede prior decisions;
- a decision can authorize execution but cannot falsify the actual outcome.

## Relationships
Decisions authorize Jobs, lifecycle transitions, policy changes, capital allocation, learning promotion and retirement actions. Their realized outcomes are later observed through Events and metrics.
