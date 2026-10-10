# tiger

A small working agreement for coding agents: the smallest process that gets a
task implemented, verified, and reviewed by a different model.

It is one file, `AGENTS.md`. Codex and other agents that read `AGENTS.md` pick
it up directly.

## What it does

- Routes each task: a defect goes reproduce → root cause → TDD → review; a
  feature goes scout → plan → review the plan → build → review the work.
- Requires an observable completion check and real verification.
- Requires review by a different model family, and never lets a missing review
  be reported as passed.
- Adds no tickets, task database, or planning framework.

## Reviewer

Any reviewer from a different model family works. If your agent is not Gemini,
I recommend [agy-review](https://github.com/HakAl/agy-review): it runs Google's
Antigravity CLI as the reviewer, which is cheap (about $5/month as of October
2026, and the plan upgrades your whole Google account) and catches things the
implementing model misses in its own work.

## Use

Put `AGENTS.md` in the directory your agent works from, and give it a goal.
