# Contract — AgencyDNA v0.1

## Purpose
Defines the constitutional specification of an Asset Agency: identity, purpose, economics, policies, permissions, autonomy, learning, scaling and retirement conditions.

## Required fields
- `agency_id`
- `dna_version`
- `agency_type`
- `asset_id`
- `platform`
- `market`
- `language`
- `niche`
- `audience`
- `business_model`
- `primary_goal`
- `north_star_metric`
- `brand_identity`
- `content_policy`
- `risk_policy`
- `budget`
- `autonomy_level`
- `tools_allowed`
- `sources_allowed`
- `publishing_rules`
- `learning_policy`
- `scaling_rules`
- `kill_criteria`
- `effective_from`
- `created_by`

## Invariants
- material changes create a new immutable version;
- successful prior behavior does not grant implicit permissions;
- kill criteria exist before scale;
- tools/capabilities and permissions remain distinct;
- provider-specific settings must not redefine the business contract;
- only one AgencyDNA version may govern an agency at a given point in time.

## Relationships
AgencyDNA governs an Agency and references Policies, budgets, capabilities and approved operational rules.

## Change rule
A new AgencyDNA version that materially changes production behavior must pass governed change control and, where applicable, Champion/Challenger validation before becoming active.
