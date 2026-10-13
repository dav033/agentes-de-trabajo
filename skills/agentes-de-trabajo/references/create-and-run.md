# Discover, create and run

## Discover a recurring job

Read relevant existing context and look for an agent that already owns the job. Improve it instead of duplicating its responsibilities when appropriate. Reflect the user's desired outcome in plain language and distinguish their statements from your assumptions.

Clarify only what changes the solution: who uses/approves it; what starts the work; actual input and authoritative sources; desired output with a good example; current steps and exceptions; actions it can take alone; and how the owner will recognize a useful result. Use small rounds with recommendations, not a technical questionnaire. If the owner says to proceed, take reasonable explicit assumptions except where money, authority or irreversible effects require a specific answer.

Prepare a short proposal: friendly name, job, inputs, output, steps, approval boundaries and first trial. The user's approval can be conversational; record its actual scope rather than asking twice. The initial trial may run as preparation without external effects. Invoice drafting does not imply invoice issuance, tax submission, customer email or accounting write access.

## Build the first version

Read [agent blueprint](../assets/agent-blueprint.md), instantiate only needed records and remove template markers. Write one agent per distinct job; do not split steps into multiple agents without a real need. Agent instructions must link their own procedure and relevant memory rather than duplicate business rules.

Update the registry with ID, friendly name, job, lifecycle state and latest evidence. Default a new agent to `draft`. Check required capabilities using [connections](connections.md) proactively. An initial useful draft does not require every future integration to be connected.

Use a representative owner-supplied or synthetic case. Check the result against the agreed inputs, source rules, arithmetic/units when relevant, output and approval boundaries. Record actual evidence and missing capabilities. A simulated trial proves only the tested mode. Do not label a live integration tested because a synthetic run passed.

## Lifecycle

Use explicit states in the registry and agent metadata:

| State | Meaning and transition |
|---|---|
| `draft` | Definition/proposal or trial incomplete. Move to `ready` only after owner acceptance and a passing representative trial; otherwise remain draft. |
| `ready` | Approved and tested for its recorded operating mode. A missing required capability moves it to `blocked` before that mode runs. |
| `blocked` | A specific prerequisite is missing or failed. Record prior state and blocker; after verifying resolution, return to that prior state. |
| `paused` | Owner paused execution. Save prior state and handoff; resume only on owner request, checking prerequisites first. |
| `retired` | Owner ended this agent's use. Preserve records; reactivation requires an explicit owner request and a fresh readiness check. |

Pausing a definition does not stop external schedules/services. If such a service exists, explain what must be stopped and act only with the required authorization and real tool support; verify before reporting it stopped. Do not implicitly run paused or retired agents.

## Run and resume

Choose an unambiguous registry entry. Read its SKILL.md, approved procedure, current memory and pending handoff; fetch only decisions/history relevant to the task. If the registry and definition conflict, reconcile the current authoritative revision before executing.

Identify operating mode and required tools. Check real access and existing grants; prepare a connection fix when needed. Run reversible preparation autonomously within the approved scope. Separate draft output from any external effect and verify the authorized effect's result.

Missing input: ask for the material missing fact or return a useful partial draft with the gap explicit. Never invent customers, amounts, tax rates, identifiers or source-system availability. On an uncertain external result, reconcile before retry. On repeated failure, keep the work and report the cause instead of accumulating unverified changes.

At close, maintain memory and handoff under [improvement](memory-and-improvement.md), then persist with [save-state checks](persistence.md). For status, give the agent's job, current readiness, recent useful learning and next pending action without exposing file mechanics unless needed.
