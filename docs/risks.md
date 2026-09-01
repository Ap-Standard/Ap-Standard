# Risk register

Live register for the portfolio program. Small and honest by design: a risk appears here
because it is real, has an owner (me), and has a mitigation someone can audit. Reviewed
quarterly per the [operating model](operating-model.md).

Scoring rubric: likelihood over the next four quarters, High above 50%, Medium 10 to 50%,
Low under 10%. Impact High means a core portfolio claim breaks in public. Scored by the
owner at quarterly review.

| ID | Risk | Likelihood | Impact | Mitigation | Status |
| --- | --- | --- | --- | --- | --- |
| R1 | Solo maintainer: the portfolio goes stale during work crunches | High | High | Weekly cadence capped at 45 minutes so it survives busy weeks; quarterly note is the floor; bit-rot canary CI (planned, flightdeck milestone) opens issues when quickstarts break | Open |
| R2 | Self-merged PRs read as undisciplined | Medium | Medium | Live today: branch protection binding the admin on the four flagship repos, published review policy ([decision 0002](decisions/0002-solo-maintainer-review-policy.md)), countable `gate-bypass` labels. Planned: protection on this repo (owner task, pre-merge), the `ai-review` required check (twoseat v0.1), and published bypass rate (flightdeck milestone) | Partially mitigated |
| R3 | Sanitization failure links public content to private work | Low | High | Disclosure policy ([decision 0003](decisions/0003-sanitization-and-disclosure-policy.md)); a secret-scanning gate in CI (live in this repo, shipping with field-notes' first PR, extending to each flagship before its first code PR); second-model review on field-notes before publish; owner verification at review | Mitigated, residual accepted |
| R4 | Model API pricing or behavior change breaks twoseat budgets and benchmark validity | Medium | Medium | Specified in twoseat's v0.1 design (planned): a per-PR cost ceiling that fails to comment-only, and benchmark re-runs pinned to model version changes | Open |
| R5 | Org-style handle confuses reviewers looking for a person | Low | Low | Profile README leads with the person; accepted per [decision 0001](decisions/0001-portfolio-scope-account-and-pins.md); revisit on evidence it costs an opportunity | Accepted |
