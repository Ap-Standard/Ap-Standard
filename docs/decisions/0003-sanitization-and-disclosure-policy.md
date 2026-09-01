# 0003: Sanitization and disclosure policy

Status: accepted. Date: 2026-08-31.

## Context

Public writing in this portfolio draws on production experience under confidentiality. The
value is in the mechanisms; the risk is in the identifiers. One leaked hostname or client
name converts a general lesson into a targetable surface and a broken confidence, so the
boundary is written down and enforced rather than remembered.

## Decision

The following never appear in any public artifact in this portfolio:

- client, partner, or teammate names tied to the author's private ventures;
- infrastructure identifiers: hostnames, cloud project references, service URLs, and
  vendor names tied to production infrastructure;
- private repository paths, pull request numbers, or commit SHAs;
- security control names that could aid an attacker, including feature-flag and
  kill-switch environment variable names used in production systems;
- unremediated security findings;
- stories attributable to a specific employer or client, even anonymized. Exception:
  career track-record claims already published on the author's LinkedIn profile, which
  cite that provenance where they appear;
- the name of any private venture or product, or any detail whose purpose or effect is to
  connect this public content to private repositories.

Two positive rules complete the policy:

1. **Mechanism level only.** Public writing describes what a system did, how it was built,
   and what pattern it demonstrates. Incidents are described by class, never by artifact.
2. **No number without a method.** Every published figure states how it was measured or
   cites its public provenance, or it does not publish.

## Enforcement

- The author runs a checklist pass against this policy before opening any PR.
- A secret-scanning job gates every pull request: live in this repo, shipping with
  field-notes' first pull request, and extending to each flagship before its first code
  PR lands.
- field-notes and case-study content gets a second, independent model review against this
  policy before publish.
- The repository owner verifies every public artifact at PR review.

## Consequences

Some stories stay untold and others lose specificity. Accepted: the mechanisms carry the
credibility.
