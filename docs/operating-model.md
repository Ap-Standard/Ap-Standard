# Operating model

How work moves through this portfolio, and the cadence that keeps it alive. The rules here
are commitments, not aspirations; flightdeck will report against them once its reporting
lands.

## How work moves

1. Nontrivial work starts as an issue with acceptance criteria. Trivial fixes may skip the
   issue; that norm is written here so nobody has to fake ceremony.
2. Every change to `main` moves through a pull request with the repo template filled in:
   what and why, risk and rollback, test evidence, AI-review disposition.
3. Merge requires green required checks. The review policy for a solo maintainer is
   [decision 0002](decisions/0002-solo-maintainer-review-policy.md).
4. User-visible changes land in a release with a changelog entry.
5. For repos with a deployed or runnable surface, merged means verified: after merge, the
   change is confirmed live per that repo's runbook, not assumed from green CI.

## Definition of done

An item is done when it meets its acceptance criteria, clears the merge gates, appears in
the changelog if user-visible, passes post-merge verification, and carries its doc updates
in the same PR.

## The 10-minute reviewer test

Run quarterly against every pinned repo, timed by the maintainer from a cold clone with no
warm caches, result recorded in the quarterly note. A repo passes when a stranger can:

- clone it and complete the quickstart, with the documented expected output, in under
  10 minutes;
- find the architecture and the key decisions from the README;
- see tests that fail meaningfully, not just exist;
- identify the latest release and its changelog entry;
- regenerate the headline numbers with a documented command;
- find at least one honestly documented limitation.

Failures become `prio:p1` issues.

## Cadence

- **Weekly, 45 minutes:** triage new issues and dependency PRs; one meaningful PR anywhere
  in the portfolio. A field-notes edit counts.
- **Monthly, 90 minutes:** milestone grooming (slipped dates move with a one-line comment,
  never silently); one new or revised field-note; review the bit-rot canary results once it
  exists.
- **Quarterly, half a day:** a quarterly note in `docs/quarterly/` covering shipped,
  slipped, learned, and next, with links to PRs and tags in the public portfolio repos
  only (private work is out of scope per decision 0003); the 10-minute reviewer test per
  pin; risk register review; rotate the "Currently exploring" line in the profile README.

Write the first quarterly note after a full real quarter, not retroactively.

## Automation boundary

Automation may open issues and pull requests. Only gated pull requests change `main`.
