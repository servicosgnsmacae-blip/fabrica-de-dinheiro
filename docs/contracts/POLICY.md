# Contract — Policy v0.1

## Purpose
Represents a governing rule that constrains or authorizes AgencyOS behavior.

## Required fields
- `policy_id`
- `policy_version`
- `scope`
- `policy_type`
- `rule_statement`
- `conditions`
- `allowed_actions`
- `prohibited_actions`
- `approval_requirements`
- `autonomy_constraints`
- `budget_constraints` when applicable
- `effective_from`
- `effective_until` when temporary
- `created_by`
- `status`

## Status
At minimum: `DRAFT`, `ACTIVE`, `SUSPENDED`, `SUPERSEDED`, `RETIRED`.

## Invariants
- policies are versioned and immutable once historically applied;
- material policy changes do not silently overwrite active history;
- lower-level policies cannot grant authority beyond higher-level constitutional constraints;
- policy evaluation must be reproducible against the version active at the time of action;
- policy scope must be explicit: portfolio, agency type, specific agency, job class or other approved boundary.

## Relationships
Policies govern Decisions, Jobs, autonomy, lifecycle transitions, budget use, publication authority, risk and learning promotion.
