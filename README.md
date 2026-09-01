# Arthur Paula

Senior technical program leader. Platform and API modernization, AI/ML program delivery.
I build the operating system a program runs on: the intake, the gates, the release cadence,
and the evidence that turns strategy into shipped, verified change.

**Track record, as published on my LinkedIn profile:** $3B+ portfolio impact across five
companies, including DoorDash ($0 to $240M in under 18 months) and Chipotle ($45M
infrastructure program behind $1B in digital revenue). 8,000+ hours hands-on with AI
systems. PMP, CSM.

## Selected work

I run this portfolio as one governed program: four flagship repos plus this program
office. Each is honest about its state.

- **[twoseat](https://github.com/Ap-Standard/twoseat)**: AI code review as a CI gate, with
  a labeled benchmark that measures the reviewer before you trust it. Each release will
  publish catch rate, false-block rate, and cost per PR, reproducible from the repo.
  In build, v0.1 due 2026-09-30.
- **[flightdeck](https://github.com/Ap-Standard/flightdeck)**: DORA and program-health
  metrics engine. Every metric ships with its operational definition, the way it gets gamed
  in real organizations, and the cross-check that catches the gaming. It will be dogfooded
  on this portfolio: once live, its CI runs produce the numbers it reports about these
  repos. In design.
- **[leaseq](https://github.com/Ap-Standard/leaseq)**: a small Postgres job queue that will
  ship with full release governance: staged online migrations, a dark-launched feature arc,
  and a postmortem of a deliberately induced failure. The queue is the vehicle. The
  governance is the product. In design.
- **[field-notes](https://github.com/Ap-Standard/field-notes)**: the mechanisms I operate a
  production AI platform with: two-seat AI review, post-merge verification, CI gate ladders,
  migration safety. Steal them, with attribution. First notes in review.

## How I run a program

Most programs do not fail on strategy. They fail because nobody built the machine that turns
strategy into merged, verified, reversible change. My operating model: every piece of work
starts as an issue with acceptance criteria, ships through a gated pull request, lands in a
release with a changelog entry, and gets verified after merge, not assumed. This portfolio
runs on that model in public: [charter](docs/charter.md) ·
[operating model](docs/operating-model.md) · [decisions](docs/decisions/) ·
[risks](docs/risks.md).

## Production proof

The mechanisms in this portfolio run in production. I architect and operate a multi-tenant
AI platform that has processed 2.5B tokens at a 97.8% cache hit rate, measured by token
accounting instrumented at every model call site and reconciled against provider billing.
Gated trunk, two-seat AI review, post-merge verification, recurring reliability sweeps.
The code stays private; the mechanisms are being published at
[field-notes](https://github.com/Ap-Standard/field-notes).

## Currently exploring

Eval-gated autonomy: how much review authority an AI seat can hold before the false-block
tax exceeds the review time it saves. Updated 2026-Q3.
