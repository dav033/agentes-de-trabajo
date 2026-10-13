# Connection record blueprint — schema version 1

Instantiate as `connections/<connection-id>.md`. Replace markers; store no secrets, signed URLs or authentication cookies. Unknown states remain unverified. Create a registry row only for a concrete needed/known connection.

```markdown
---
schema_version: 1
id: {{connection-id}}
state: needed
---
# {{Friendly connection name}}
- Purpose / required capability: {{job this enables}}.
- Used by: {{agent IDs and operating modes}}.
- Environment: {{hosted Work, desktop/local or another verified runtime}}.
- Provider / official documentation: {{verified provider and source}}.
- Account/workspace alias: unconfirmed; use a non-sensitive alias after verification.
- Plugin ID / MCP endpoint and transport: unconfirmed until discovered from trusted sources; do not include secrets or signed query strings.
- Config/secret reference: {{safe path or variable name, never secret value}}.
- Desired operations / resource scope: {{smallest useful access}}.
- Actual observed capabilities: unverified.
- Setup authorization: none recorded; record owner, date, source, approved change and limits when given.
- Business-action authorization: separate; refer to the agent's applicable grants.
- Setup steps prepared / completed: {{specific steps and actual outcomes}}.
- Last verification: not tested; record date, operation, environment/account and non-sensitive evidence.
- Write verification: not tested unless an authorized scoped write plus readback succeeded.
- Pending action and owner: {{what is needed next}}.
- Rollback: {{scoped restoration of authorized setup, no credential copies}}.
```

Registry row: ID, service, environment, state, agents, last verified date/evidence, record link. A remembered state never replaces a current functional check.
