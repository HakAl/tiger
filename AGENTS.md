# Working toward a goal

Use the smallest process that gets the requested outcome implemented, verified,
and reviewed. Keep moving within the user's authorized scope; ask only when a
missing answer blocks progress or a consequential choice needs the user.

## Choose a path

- **Defect / broken expected behavior:** reproduce → root cause → TDD →
  review the work.
- **Feature / open-ended problem:** scout → plan → review the plan →
  implement and verify → review the work.

Route by whether the expected behavior is established, not whether the cause is
already known. If investigation reveals a product or design decision, switch to
the planning path and reuse what you learned.

## Do the work

- Start with the requested outcome and an observable completion check. Infer
  these from context when possible.
- **Root cause:** reproduce the failure and trace the responsible behavior.
  Identify the cause before changing behavior.
- **TDD:** add a regression test, confirm it fails for the expected reason,
  make the smallest correct fix addressing the cause, then refactor if useful.
  If automated testing is impractical, record why and use a concrete reproduction
  and verification.
- **Scout:** inspect relevant code, conventions, and constraints. Stop when
  there is enough evidence to choose an approach.
- **Plan:** write a few bullets covering the outcome, approach, affected areas,
  and verification. Give the reviewer a concrete plan file; a temporary file
  outside the repo is enough. Resolve substantive findings before implementation.
- **Implement and verify:** follow the plan, adjusting to evidence. Re-review
  the plan only if its scope or approach materially changes. Run relevant checks;
  use meaningful behavior tests for code and direct checks for simple docs or
  configuration changes.
- **Review the work:** review the complete task change, including new files.
  Assess findings against evidence, fix valid issues, and recheck affected
  behavior. Review substantive fixes again; explain rejected findings briefly.
  Reviewers inspect and report only; they do not execute this workflow or
  launch further reviews.

## Review

- Use a reviewer from a **different model family** than the one doing the work,
  through whatever review tool or CLI you have for it. Same-family review shares
  the implementer's blind spots.
- If no other family is available, use your own CLI's review command or skill,
  and report the review as same-family.

## Keep overhead low

- No mandatory tickets, ceremony, task database, or separate planning framework.
  Keep context in the conversation. If work needs a durable handoff, save only
  the goal, current evidence, and next step in a short local note.
- If review is unavailable, continue independent work and report the missing
  review as a completion blocker; never claim it passed.
- Finish when the outcome is met, relevant checks pass, and review findings are
  resolved or explicitly accounted for. Report the result, verification, and
  any remaining limits concisely.
