# 0002: Solo-maintainer review policy

Status: accepted. Date: 2026-08-31.

## Context

GitHub does not allow an account to approve its own pull requests, so required approvals
on a solo account is zero by necessity. A wall of self-merged PRs with no visible review
discipline reads as no discipline at all. The credibility mechanism has to be machine
enforcement plus published policy, not a pretend approval.

## Decision

Every change to a portfolio repo merges through a pull request. Self-merge is permitted
only when all of the following hold:

1. **CI is green**: lint, tests, and coverage where the repo defines them.
2. **The AI review seat ran**: the `ai-review` check, implemented by
   [twoseat](https://github.com/Ap-Standard/twoseat) (the AI review gate), posts its
   findings as a PR comment. Findings rated must-fix block merge until resolved, or
   explicitly waived in a comment with written reasoning. Until twoseat v0.1 is live,
   this seat is marked N/A in the PR template; the clause activates the day the check
   exists.
3. **The self-review checklist is complete** in the PR description: what and why, risk and
   rollback, test evidence.

Exceptions carry the `gate-bypass` label and a justification comment. The label satisfies
the review requirement inside the check itself; branch protection and CI stay unbypassed,
so the exception is visible and countable rather than silent. The label exists so bypasses
are countable; [flightdeck](https://github.com/Ap-Standard/flightdeck) (the metrics
engine) publishes the bypass rate once its reporting is live, and until then the
`gate-bypass` label count in the PR list is the public record.

## Consequences

- Waived findings and bypasses stay on the record. Visible disagreement with my own
  tooling is evidence the gates are real, not decoration.
- Branch protection enables "do not allow bypassing", so these rules bind the
  administrator too.
- At team scale this policy changes: human review returns as the primary gate and AI
  seats become advisory. That boundary is documented rather than discovered.
