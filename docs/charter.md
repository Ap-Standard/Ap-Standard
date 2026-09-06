# Portfolio charter

## Mission

Demonstrate, with verifiable artifacts, how I run programs: issue to pull request to gated
CI to release to changelog to runbook, measured by tooling built inside this portfolio.

## Audience

TPM and engineering hiring managers at AI-native and enterprise technology companies.
Success is a reviewer answering, in under 10 minutes per repo: what it does, how to run it,
what was decided and why, what shipped last, and where its limits are.

## Scope

Four repos, one program: this repo (the program office), plus
[twoseat](https://github.com/Ap-Standard/twoseat),
[flightdeck](https://github.com/Ap-Standard/flightdeck), and
[field-notes](https://github.com/Ap-Standard/field-notes).
One operating model, one decision log, one risk register, all in this repo. leaseq, a
fifth repo in the original scope, was cut before any code was written
([decision 0005](decisions/0005-portfolio-reset.md)).

## Out of scope

Anything that identifies clients, partners, teammates, or private infrastructure. The
disclosure policy is
[decision 0003](decisions/0003-sanitization-and-disclosure-policy.md) and it binds every
public artifact in this portfolio.

## Success measures

- Every pinned repo passes the 10-minute reviewer test
  (checklist in [operating-model.md](operating-model.md)).
- flightdeck publishes portfolio metrics nightly from a scheduled Actions run to GitHub
  Pages. The card prints its generation date and the reliability tile counts completed
  nights over the last 30, scheduled and manual apart, so a missed run is visible on the
  profile without a keepalive commit or an auto-filed issue.
- One release per code repo per quarter, minimum.
- Zero disclosure-policy violations, checked at every PR review.

## The falsifiability rule

Every artifact in this program layer must reference at least one verifiable event in a
public portfolio repo: an issue, a pull request, a release tag, a CI run. Private work is
out of scope as evidence per decision 0003. An artifact that could have been written
without the portfolio existing gets deleted. The governing documents themselves anchor to
the events that ratified them: this charter shipped with
[issue #2](https://github.com/Ap-Standard/Ap-Standard/issues/2) and the decisions dated
2026-08-31.
