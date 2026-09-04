# Learning System — AgencyOS v0.1

## 1. Principle

AgencyOS learns through controlled experimentation, not by letting a model rewrite production behavior after every observation.

## 2. Memory classes

### Episodic memory
Records what happened: jobs, outcomes, metrics, incidents and decisions.

### Semantic memory
Stores validated conclusions derived from evidence, such as patterns, relationships and reusable insights.

### Procedural memory
Stores approved operating rules: how the platform or an agency should act.

## 3. Learning pipeline

`event → data → analysis → hypothesis → experiment → evidence → learning → policy candidate → approval → production policy`

No step may be skipped for material changes.

## 4. Evidence requirements

Learning must remain linked to the data, time window, experiment design, agency context and confidence that produced it. Local correlation must not automatically become portfolio-wide policy.

## 5. Champion / Challenger

- **Champion**: current proven production version.
- **Challenger**: alternative under controlled test.
- **Candidate**: unproven proposed change.
- **Production**: currently deployed behavior.

A Challenger replaces a Champion only after meeting predefined quality, economic and risk criteria. Rollback must remain possible.

## 6. Knowledge promotion

Agency-level knowledge can be promoted to platform-level knowledge only after governance validates that it is reusable beyond the original context.

## 7. Memory ownership

Institutional memory belongs to AgencyOS. Model conversations and temporary context are not canonical memory.

## 8. Prohibited learning behavior

The platform must not:

- silently change prompts or policies from one bad result;
- convert unsupported model opinions into facts;
- overwrite historical evidence;
- propagate one agency's finding to all agencies without validation;
- remove rollback capability for important changes.
