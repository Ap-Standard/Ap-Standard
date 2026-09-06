# 0005: Portfolio reset

Status: accepted. Date: 2026-09-05. Amends [0001](0001-portfolio-scope-account-and-pins.md).

## Context

The audience is a TPM or engineering hiring manager who gives a profile about sixty seconds
and three clicks. Under [0001](0001-portfolio-scope-account-and-pins.md) this portfolio
planned four pinned repos. Between the first commits on 2026-08-31 and 2026-09-03, when this
reset was decided, only one of them held code: twoseat had shipped its gate and its
benchmark; flightdeck and leaseq had not started; zero images and zero live links existed on
any surface.

The slowness had two causes, and neither was the portfolio's design. First, process
ceremony: test-first development plus a second review seat plus multi-agent adversarial
review on every pull request. Second, scope creep inside twoseat: at the v0.1.0 tag,
`bench/src` held 4,856 lines of TypeScript against 3,947 in `src`, counted by `wc -l` over the
tagged tree including tests. The harness that measures the gate outgrew the gate.

## Decision

1. **Freeze twoseat at v0.1.0.** No new gate features. The second seat, the enforce step,
   and severity calibration move to a v0.2 milestone dated 2026-11-30 with a written
   confidence line. The proof that the gate finds things is the benchmark audit trail, not
   a staged demonstration pull request.
2. **Build flightdeck as the visual hero.** A nightly, zero-dependency measurement of this
   portfolio's own delivery practice, published as one static page and one SVG card through
   Actions-mode GitHub Pages. Every tile carries its definition, its gaming analysis, and its
   cross-check, or it does not ship. The profile's only image is that live card.
3. **Delete leaseq.** Its design intent, preserved here so the idea survives the repo: a
   small Postgres-backed job queue used as the vehicle for full release governance, with
   staged online migrations (additive first, constraints added invalid then validated), a
   dark-launched feature arc behind a flag plus an entitlement, and a postmortem of one
   deliberately induced failure. The queue was never the point; the governance was. That
   governance now ships through twoseat's release ritual and flightdeck's verified-release
   tile, which is why the third repo is not needed.
4. **Pin three repos: twoseat, flightdeck, field-notes.** This amends 0001, item 2, which
   pinned four. Three deep pins that resolve to live artifacts beat a fourth that reads
   "in design".
5. **Delete the tutorial repos** (`skills-introduction-to-git`,
   `skills-introduction-to-github`, `skills-getting-started-with-github-copilot`). A
   hiring manager's skim should land on judgment, not on onboarding exercises.
6. **Lighter process.** Tests on core logic only, one review pass per pull request, larger
   pull requests, no multi-agent adversarial review. Every pull request description states
   its mechanism in two sentences I can repeat, or the mechanism gets simplified before
   merge.
7. **The hero is the proof or there is no hero.** One generated SVG per code repo, one
   Mermaid diagram, at most three badges each linked to what it measures. No stat cards,
   no contribution-graph engineering, no committed screenshots.

## Consequences

- The story a recruiter reads is one sentence and three clicks: every change here is
  reviewed by a benchmarked AI gate, ships in a release whose notes record post-publish
  verification, and is measured nightly by a dashboard where every number links to its
  definition, how it can be gamed, and its cross-check.
- twoseat's name promises two seats and v0.1.0 ships one. The README says so in its honesty
  strip rather than in a footnote, and the v0.2 milestone carries the second.
- The charter's scope drops from five repos to four (this repo plus three pins), and its
  measurement cadence changes from weekly to nightly.
- A portfolio that measures itself every night can go silent. [Risk R6](../risks.md)
  records how silence becomes visible without keepalive commits.
- Deleting leaseq removes a repo that was pinned and linked from the first profile README.
  Anyone holding that link gets a 404. Accepted: a dead link to an empty repo is more honest
  than a live link to one.

## Alternative rejected

Finish the plan as designed: complete twoseat's second seat, then build leaseq and
flightdeck in sequence. Rejected because the constraint that matters is my time, not the
calendar. At the observed pace the third repo would have landed months out, and the
portfolio would have shown "in design" on two of four pins the whole way. Cutting scope to
what can be live, measured, and explained cold is the same call I make on any program that
is behind: ship the part that proves the thesis, write down what was cut and why, and keep
the design where it can be picked up.
