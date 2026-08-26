# Loop discipline

Use these rules only when directed by `SKILL.md`.

## Set a budget before multi-attempt work

State the experiment budget and the stopping rule before the first attempt. After every attempt, ask **Did the lifecycle state advance?** and classify the result:

- **Domain signal** — the repository, target system, or live state supplied material evidence about the actual objective.
- **Tooling/process failure** — a wrapper, verifier, handoff, evidence mechanism, or coordination step failed before the target behavior was exercised.

Two consecutive attempts without lifecycle advance trigger a strategy reassessment before more work. After three failures in the same wrapper, verifier, or handoff family, retire that mechanism and use a simpler direct or manual seam, or route a decision; a fourth local correction to the same mechanism is out of budget.

**Tooling must be simpler than the task.** When coordination or evidence overhead exceeds the underlying risk or complexity, reduce the mechanism before continuing.

The loop stays within budget while every attempt either produces domain signal or retires a mechanism.

## Match evidence cost to consequence

- **Durable repository or live mutation** — use the complete project-required bindings, verification, review, and lifecycle evidence.
- **Bounded read-only diagnostic** — bind source and scope, exercise one real initialization or collector seam, record a structured result, and prove the authorized no-mutation boundary.
- **Temporary wizard or tooling correction** — run syntax and static checks, focused RED/GREEN, and one real initialization test. Test the disposable mechanism directly instead of surrounding it with another elaborate mechanism.

## Batch human interactions

Batch human interactions into one runnable handoff and one meaningful confirmation boundary whenever privilege, secrets, or human judgment permit. For retryable pre-mutation tooling, request one explicit standing authority envelope up front. Within that envelope, deterministic corrections that preserve every approved invariant and cannot reach target mutation proceed without repeated chat approval.

Seek fresh authority when a correction changes an invariant, expands scope, adds a new mutation, or follows a mutation failure.

The envelope covers retryable pre-mutation tooling only. Creating a user-visible task sits outside it and always needs its own authorization under `SKILL.md`.
