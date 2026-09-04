# Observability — AgencyOS v0.1

## 1. Goal

AgencyOS must make important work reconstructable. Observability is required for trust, economics, debugging, governance and learning.

## 2. Three views

### Executive view
Shows portfolio-level revenue, cost, profit, active agencies, risk, scaling candidates, recovery candidates and material exceptions.

### Agency view
Shows output volume, growth, economics, content performance, experiments, incidents, autonomy and health for one Asset Agency.

### Technical view
Shows jobs, events, errors, retries, model use, tool use, latency, token/API consumption, costs and integration health.

## 3. Minimum action record

Every relevant action must be able to record:

- `action_id` or `job_id`;
- `agency_id`;
- actor/agent role;
- model/provider;
- agent/model/policy version;
- inputs and data references;
- evidence references;
- decision;
- output/result;
- cost;
- timestamps;
- status;
- retry/attempt data when applicable.

## 4. Decision trace

For a material output, the platform should be able to answer:

- who proposed it;
- what evidence was used;
- who validated it;
- which policy allowed it;
- which tools/models executed it;
- what it cost;
- what happened afterward.

## 5. Events

Important events must be explicit and queryable, including lifecycle changes, budget thresholds, publication outcomes, policy incidents, monetization changes and failures.

## 6. Reconciliation

After external actions, the system should verify actual state against intended state. A successful API call is not automatically proof that the desired business outcome occurred.

## 7. Retention

Audit, financial, learning and lifecycle records must survive agency retirement according to future retention policies. Exact retention periods remain an open implementation decision.
