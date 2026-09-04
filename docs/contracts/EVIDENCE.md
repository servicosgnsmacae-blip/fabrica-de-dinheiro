# Contract — Evidence v0.1

## Purpose
Represents the provenance-bearing support used to justify facts, decisions, learning, policy changes and material outputs.

## Required fields
- `evidence_id`
- `evidence_type`
- `source_ref`
- `source_class`
- `retrieved_at`
- `captured_by`
- `content_or_data_ref`
- `claim_refs` when evidence supports explicit claims
- `agency_id` when scoped
- `confidence`
- `verification_status`
- `verified_by` when reviewed
- `validity_window` when time-sensitive

## Verification status
At minimum: `UNVERIFIED`, `VERIFIED`, `QUESTIONABLE`, `REJECTED`, `EXPIRED`.

## Invariants
- AI-generated text is not self-authenticating evidence;
- important factual claims must resolve to evidence or canonical domain data;
- evidence keeps provenance even after the agency is retired;
- evidence may become stale or expire without being deleted from history;
- local evidence does not automatically justify portfolio-wide rules.

## Relationships
Evidence supports Decisions, Jobs, learning hypotheses, experiments, factual claims and policy changes. AuditRecords reference the evidence used at execution time.
