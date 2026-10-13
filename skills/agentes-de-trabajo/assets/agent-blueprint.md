# Agent blueprint — schema version 1

Instantiate under `agents/<agent-id>/` in the selected workspace. This file is a template, not an active agent. Replace all `{{...}}` markers, use the owner's language for records and link local records. Fill unknowns as unconfirmed, never fabricate approvals or passing checks. Create history entries only when work occurs.

## SKILL.md

```markdown
---
name: {{agent-id}}
description: "{{Specific job and natural-language triggers, with a useful scope boundary}}"
metadata:
  schema_version: "1"
  version: "0.1.0"
  state: "draft"
---
# {{Friendly name}}

Purpose: {{Useful outcome and owner}}.
Read [procedure](PROCEDURE.md), [current memory](MEMORY.md) and [pending work](PENDING.md) before running. Read [decisions](DECISIONS.md) when relevant to the task or a proposed change.

Use the current owner-selected workspace's permissions and connection records. The coordinator manages lifecycle and persistence; creating this definition does not install or start an independent service. If invoked directly, verify registry state and workspace grants before acting; do not bypass paused/blocked state or approval boundaries.

Produce {{output}} from {{authoritative inputs}}. Missing facts stay explicit. Follow the approved procedure; do not invent sources or silently change rules.

Autonomy: {{Approved preparation and actions; source/date}}.
Needs approval: {{Consequential changes and external effects without an existing grant}}.
Required capabilities: {{Connection IDs and operating modes, or none}}.
Learning: preserve confirmed context within the memory-write grant. New procedures, business rules, permissions or effects stay proposals until approved. Case exceptions do not become defaults.
```

## PROCEDURE.md

```markdown
---
schema_version: 1
---
# Procedure
- Job and trigger: {{job}}.
- Inputs and source of truth: {{sources}}.
- Output and acceptance: {{output and useful checks}}.
- Operating mode and required connections: {{mode and IDs}}.
- Steps: {{actual approved steps}}.
- Missing input, exceptions and failure handling: {{behavior}}.
- Approval boundaries: {{scope and evidence}}.
- Current procedure approval: unconfirmed until the owner approves.
- Trial evidence: not tested; record input reference, checks, actual result and limitations when run.
```

## MEMORY.md

```markdown
---
schema_version: 1
---
# Current memory
## Confirmed facts and preferences
No confirmed records yet. Each entry: fact, source/date, scope, status and relevant superseded decision.
## Assumptions
Record only assumptions needed to proceed; label them explicitly.
## Case exceptions
Scope each exception to the named case and expiration if known; do not change defaults.
```

## DECISIONS.md

```markdown
---
schema_version: 1
---
# Decisions and change proposals
No decisions yet. Each entry: unique ID, date, source, proposed/approved/rejected/superseded status, scope, before/after, evidence, approval and superseded record. Store proposals separately from the active procedure. Record approval only when actually given.
```

## PENDING.md

```markdown
---
schema_version: 1
---
# Pending
- Complete/confirm agent proposal and representative trial before readiness.
- Verify required connections and persistence grant.
Each item: next action, owner, affected case/paths, blocker and actual save state.
```

## History entry, created after meaningful work

```markdown
---
schema_version: 1
---
# {{Session or change ID and date}}
- Outcome and evidence: {{actual result}}.
- Confirmed learning / approved change: {{scope and source}}.
- Changed records: {{paths and known base/result revisions}}.
- Connections: {{relevant checks, state and unresolved setup}}.
- Persistence: {{actual save state and readback evidence}}.
- Pending and next step: {{handoff}}.
```

Registry row fields: ID, friendly name, job, state, operating mode, trial evidence and record link. Keep registry and agent metadata consistent, without activating a partial write.
