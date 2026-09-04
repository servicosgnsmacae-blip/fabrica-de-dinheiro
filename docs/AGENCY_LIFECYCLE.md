# Agency Lifecycle — AgencyOS v0.1

## 1. Purpose

An Asset Agency moves through explicit states. State changes are governed decisions and must be auditable.

## 2. States

### CANDIDATE
An opportunity exists, but no operating agency exists yet.

### THESIS
The Mother Agency formulates an investment thesis covering opportunity, market, competition, monetization, expected cost, risk, content supply and economic hypothesis.

### SPECIFIED
Agency DNA has been defined and the operating specification is complete enough for a controlled test.

### SANDBOX
The agency exists in a non-production environment. It may research and produce test artifacts but must not perform real publication or unrestricted spending.

### PILOT
The agency receives limited production authority, budget and scope to validate the thesis.

### ACTIVE
The agency has demonstrated minimum operational viability and can operate under its approved autonomy level.

### SCALE
The agency has demonstrated repeatable economic viability and may receive more capital or throughput.

### MATURE
The agency operates predictably with low routine intervention.

### RECOVERY
Performance, risk or reliability has degraded and a controlled recovery plan is active.

### PAUSED
New production and discretionary spend are stopped while data and knowledge are preserved.

### RETIRING
The agency is executing its shutdown procedure.

### RETIRED
Operations have ended. Knowledge, analytics and audit history remain preserved.

## 3. Allowed progression

Normal progression:

`CANDIDATE → THESIS → SPECIFIED → SANDBOX → PILOT → ACTIVE → SCALE → MATURE`

Recovery paths may move an active agency to `RECOVERY`, `PAUSED`, `RETIRING` or back to a lower-risk state according to governance.

No agency may jump directly from candidate status to scale.

## 4. Birth gate

An agency may enter `SPECIFIED` only when a thesis exists and its DNA defines at least identity, objective, economics, permissions, autonomy, risk policy and kill criteria.

## 5. Sandbox gate

Before `PILOT`, the agency must demonstrate that its workflow can complete under test conditions with acceptable quality, traceability, cost visibility and failure handling.

## 6. Pilot gate

A pilot must have explicit limits, including budget, output volume, duration or evaluation window, allowed actions and success/failure thresholds.

## 7. Active gate

Activation requires evidence of operational viability and acceptable quality/risk. Economic proof may still be incomplete, but there must be a credible path to it.

## 8. Scale gate

Scale requires repeatable evidence: improving or acceptable unit economics, operational stability, risk within policy and a clear reason additional capital should produce additional value.

## 9. Recovery

Recovery is not indefinite. It must define cause, intervention, evaluation window and exit criteria. Failure to recover should lead to pause or retirement.

## 10. Retirement procedure

Retirement must:

1. stop new jobs;
2. stop discretionary spending;
3. finish or cancel queued work safely;
4. revoke unnecessary credentials;
5. archive assets and configuration;
6. preserve analytics and financial history;
7. extract reusable learnings;
8. transfer approved knowledge to platform memory;
9. create a post-mortem;
10. set state to `RETIRED`.

The agency may end; its validated knowledge must remain available to the platform.
