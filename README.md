# agent-skills

Skill sources for agent environments — Codex, Claude Code, and anything else that loads `SKILL.md` folders.

Installed skills are authoritative at their install paths on the host (`~/.agents/skills/<name>/`, `~/.codex/skills/<name>/`, `~/.claude/skills/<name>/`). This repo is the versioned source for skills authored here; promote a change by copying the skill folder to its install path.

## Skills

### `conductor`

Coordinates project state, the next consequential move, and user-visible work. Supervises; does not implement.

```
conductor/
├── SKILL.md                        # always-loaded spine
└── references/
    ├── project-health.md           # whole-project position and delivery pace
    ├── loop-discipline.md          # experiment budget, stopping rules, evidence-cost tiers
    └── routed-work.md              # handoff spec, report-back obligation, supervision
```

Install path: `~/.codex/skills/conductor/`

This is a revision of the 2026-08-25 installed version, which had the whole skill in a single 8,208-byte `SKILL.md`. Changes:

- **Split by branch.** Loop discipline and routed-work mechanics moved behind context pointers — they fire only on multi-attempt work and on runs where a task actually exists. Spine is 5,499 bytes, a 33% cut.
- **Guardrails stay inline.** Task-creation authorization, the no-hidden-subagent rule, and lifecycle-state distinctness are never disclosed behind a pointer.
- **Restored `AGENTS.md` discovery**, dropped in an earlier compression, plus the missing branch: when a needed evidence binding is absent, report the missing binding rather than inferring one.
- **Defined *frontier***, which the report format depends on.
- **Completion criteria** added to move selection, the handoff, the loop, and supervision.
- **Report scales** to the evidence depth used instead of demanding a fixed eleven elements.

`scripts/git-evidence.sh` is referenced by `SKILL.md` but is not in this repo — it was not captured by the Markdown-only snapshot this revision was derived from. Confirm it on the host before relying on that line.
