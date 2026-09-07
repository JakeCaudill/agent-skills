# Routed work

Use this reference after `SKILL.md` selects a subagent or user-visible task. The input-likelihood gate stays in `SKILL.md`.

## Delegate autonomous work

Give each subagent a bounded objective and terminal condition; verified inputs and raw evidence; scope and exclusions; granted authority; required skills, artifacts, and verification. Keep unrelated thread history out of the dispatch.

Use the inherited model and reasoning effort unless a supported override materially improves the task's risk, complexity, or cost. Record a material override when consolidating the result.

Supervise the subagent from the current task. Check its claimed terminal state against the evidence required by the project, integrate compatible results, and route any newly discovered Jake-input boundary through the gate in `SKILL.md`.

Delegation is complete when the terminal condition is verified or a concrete blocker or Jake-input boundary is identified.

## Create the user-visible task

Conductor creates the task with the user-visible task tools in the correct project and workspace. Give Jake the created task link or task marker; give him no task-creation chore.

An audit-ready handoff states:

- the objective and terminal condition;
- verified state and immutable evidence;
- scope, owner, and exclusions;
- approvals and already-granted authority;
- the project and domain skills to invoke by name;
- required artifacts, verification gates, and reporting.

The handoff is complete when an agent with no access to the originating conversation could execute it to the terminal condition and knows what input Jake is expected to provide.

## Bind the report-back obligation

Every user-visible task Conductor creates or adopts carries its originating Conductor task ID and a standing report-back instruction: before stopping, report progress, blockers, user-decision boundaries, terminal results, immutable evidence, and follow-on handoffs through user-visible task messaging.

Each report states the lifecycle state, whether it advanced, verification evidence, the remaining authority boundary, and exactly one next action. Exactly one next action is a reporting constraint, not a bias toward another retry: it may be to stop, reframe, simplify, change the seam, or seek a decision.

When a complete unchanged handoff is already recorded, confirm the obligation locally instead of duplicating it.

## Supervise user-visible work without taking ownership

Monitor an authorized task until completion, a blocker, or a user decision. During long waits, report only meaningful changes.

- Use host-reported status, blockers, results, and immutable identifiers. Inspect mutable work only with explicit authorization.
- Preserve canonical and dirty worktrees and unrelated changes. Stay read-only unless the routed workflow grants mutation authority.
- Stop at scope and approval boundaries; surface the decision needed to proceed.

After completion, verify the immutable evidence required to establish the claimed lifecycle transition. Verification establishes the state and returns the work to its owner.

Publish state only when authorized and through project procedure. Record the achieved state, evidence, remaining boundary, and next owner.

Supervision is complete when the claimed lifecycle transition is backed by immutable evidence and the next owner is named.
