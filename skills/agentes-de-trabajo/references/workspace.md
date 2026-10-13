# Workspace and deployment

One repository belongs to one deploying owner or team and contains the coordinator, agent definitions, connections and memory. This is a storage convention, not isolation between repository readers. Recommend private visibility when storing business context. Do not use one customer's workspace for another customer.

## First use

Establish the owner/team, intended repository and preferred language from the conversation. Inspect existing records before creating anything. If the repository is already known, do not ask again. Read access and write access may differ.

Use [the workspace blueprint](../assets/workspace-blueprint.md) for a root `WORKSPACE.md`. It records repository identity, shared non-sensitive context, intended Work environment, source systems and approved persistence scope. Leave unknowns explicitly unconfirmed. Ask the owner to authorize the smallest useful ongoing save scope when none exists; present the actual destination and paths. Do not require blanket remote-write permission to prepare an agent.

Maintain these root-relative locations:

```text
WORKSPACE.md
skills/agentes-de-trabajo/       coordinator instructions
agents/INDEX.md                 registry; one row per managed agent
agents/<agent-id>/SKILL.md      reusable definition
agents/<agent-id>/PROCEDURE.md  approved process and required capabilities
agents/<agent-id>/MEMORY.md     confirmed facts/preferences and scoped assumptions
agents/<agent-id>/DECISIONS.md  approvals, proposals, supersessions and evidence
agents/<agent-id>/PENDING.md    unresolved work and pending saves
agents/<agent-id>/history/      short session/change records, created on first use
connections/INDEX.md            shared connection catalog
connections/<connection-id>.md setup, scope, actual checks and pending actions
```

Choose short unique lowercase IDs; confirm a collision rather than overwriting an existing agent. The owner uses friendly names. Store records in the owner's language. Keep a `schema_version: 1` frontmatter field on managed records and maintain readers for that version. A future incompatible layout needs a migration proposal and preserves existing records.

Only the coordinator package is distributed by default; examples are not active agents. New agent folders are selected and loaded by the coordinator. They do not need independent platform registration for coordinator-driven execution.

## Work availability

A standalone skill folder is an authoring artifact. The target account still needs a supported installation and access to this repository. Do not assume a local filesystem path is available in hosted Work.

For desktop use, check the Skills interface and supported local setup in the actual app. For web/mobile sharing, check current plugin packaging and workspace controls. If installation is unavailable, provide a clearly labeled draft and the exact remaining setup step. Do not describe an attached SKILL.md as an installed skill.

Repository persistence and ChatGPT conversation memory are separate. Resuming reliably means retrieving the repository records and checking pending saves. No background job or automatic scheduling exists in this package.

Official references, checked 2026-10-12: [Build skills](https://learn.chatgpt.com/docs/build-skills), [Skills and plugins](https://learn.chatgpt.com/docs/skills-and-plugins). Recheck current documentation before giving platform-specific installation commands.
