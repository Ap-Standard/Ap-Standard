# Arthur Paula

Senior technical program leader. Platform and API modernization, AI/ML program delivery.

I build the machinery that turns strategy into shipped, verified change: intake, gates,
release cadence, and the evidence.

I architect and operate production AI systems, and bring that build depth to the program
office. A TPM who works in the pull request, not just the roadmap.

**Track record, as published on my LinkedIn profile:** a net-new DoorDash vertical from
$0 to $240M and 10M+ users in under 18 months. A $45M infrastructure modernization across
3,000+ sites at Chipotle, and an AI recommendation engine credited with $1B+ in
incremental digital revenue. A $14M to $26M climb and a $40M Series B at Local Kitchens.
The fastest e-commerce site in Gap Inc. history. PMP, CSM.

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
AI platform, run on a gated trunk with two-seat AI review, post-merge verification, and
recurring reliability sweeps. It averages 8B tokens a month, with peaks near 10B, at a
97.8% cache hit rate, measured by token accounting instrumented at every model call site
and reconciled against provider billing. The code stays private; the mechanisms are being
published at [field-notes](https://github.com/Ap-Standard/field-notes).

## Currently exploring

Eval-gated autonomy: how much review authority an AI seat can hold before the false-block
tax exceeds the review time it saves. Updated 2026-Q3.
