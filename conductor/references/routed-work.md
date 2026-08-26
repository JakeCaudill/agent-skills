# Routed work

Use this reference when a user-visible task is authorized, running, or complete. The authorization rule and the visibility rule stay in `SKILL.md`.

## Build the handoff

An audit-ready handoff states:

- the objective and terminal condition;
- verified state and immutable evidence;
- scope, owner, and exclusions;
- approvals and already-granted authority;
- the project and domain skills to invoke by name;
- required artifacts, verification gates, and reporting.

The handoff is complete when an agent with no access to the originating conversation could execute it to the terminal condition.

## Bind the report-back obligation

Every task Conductor creates or adopts carries its originating Conductor task ID and a standing report-back instruction: before stopping, report progress, blockers, user-decision boundaries, terminal results, immutable evidence, and follow-on handoffs through user-visible task messaging.

Each report states the lifecycle state, whether it advanced, verification evidence, the remaining authority boundary, and exactly one next action. Exactly one next action is a reporting constraint, not a bias toward another retry: it may be to stop, reframe, simplify, change the seam, or seek a decision.

When a complete unchanged handoff is already recorded, confirm the obligation locally instead of duplicating it.

## Supervise without taking ownership

Monitor an authorized task until completion, a blocker, or a user decision. During long waits, report only meaningful changes.

- Use host-reported status, blockers, results, and immutable identifiers. Inspect mutable work only with explicit authorization.
- Preserve canonical and dirty worktrees and unrelated changes. Stay read-only unless the routed workflow grants mutation authority.
- Stop at scope and approval boundaries; surface the decision needed to proceed.

After completion, verify the immutable evidence required to establish the claimed lifecycle transition. Verification establishes the state and returns the work to its owner.

Publish state only when authorized and through project procedure. Record the achieved state, evidence, remaining boundary, and next owner.

Supervision is complete when the claimed lifecycle transition is backed by immutable evidence and the next owner is named.
