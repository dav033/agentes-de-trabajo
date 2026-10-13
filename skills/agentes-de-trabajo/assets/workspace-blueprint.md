# Workspace blueprint — schema version 1

Instantiate root `WORKSPACE.md` for the selected owner/team. Replace markers and record actual grants only. Keep deployment configuration separate from reusable coordinator instructions.

```markdown
---
schema_version: 1
---
# Workspace
- Owner/team: {{confirmed owner}}.
- Language: {{owner's language}}.
- Repository / branch: unconfirmed until selected and inspected.
- Visibility: unverified; recommend private for business memory.
- Runtime: {{actual Work environment}}.
- Shared context: {{confirmed non-sensitive facts with source and date}}.
- Source systems: {{authoritative systems and relevant connection IDs}}.

## Persistence authorization
No remote-write grant recorded. Record owner, date, source, exact repository/branch, paths, allowed operations, duration/revocation and exclusions. Record local-write authorization separately. Ongoing memory saves may include scoped agent/context/history and connection-status records; they do not approve procedure activation, new credentials, permission expansion or external business actions.

## Active work and handoff
Reference agent IDs and relevant pending saves without copying each agent's private context.
```

Initial registry headers, with no example agents activated:

```markdown
# Agents
| ID | Name | Job | State | Mode | Trial evidence | Records |
|---|---|---|---|---|---|---|
```

```markdown
# Connections
| ID | Service | Environment | State | Agents | Last verification | Record |
|---|---|---|---|---|---|---|
```
