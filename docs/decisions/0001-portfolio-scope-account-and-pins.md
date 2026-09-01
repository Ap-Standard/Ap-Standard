# 0001: Portfolio scope, account, and pins

Status: accepted. Date: 2026-08-31.

## Context

This portfolio exists to demonstrate program leadership with verifiable artifacts, aimed at
TPM and engineering hiring managers. Two account options existed: create a new,
person-named account for the portfolio, or use the existing account. GitHub shows at most
six pinned repositories, and each pin must survive a hiring manager's two-minute skim:
four deep pins beat six shallow ones.

## Decision

1. Host the portfolio on the existing account. Operating two GitHub identities costs more
   in day-to-day friction than the org-style handle costs in branding.
2. Pin exactly four repositories: `twoseat`, `flightdeck`, `leaseq`, `field-notes`. The
   profile repo is shown automatically and carries the personal identity.
3. Run the five repos as one program: charter, operating model, decisions, and risks live
   in this repo; the flagships implement and measure the model.

## Consequences

- The handle reads as an organization, not a person. Accepted as a branding cost; the
  profile README leads with the person. Revisit if the handle demonstrably costs an
  opportunity.
- The disclosure policy ([0003](0003-sanitization-and-disclosure-policy.md)) is
  load-bearing here, not precautionary.

## Alternative rejected

A standalone portfolio-operations repository for the program layer. At solo scale a repo
about governing four other repos reads as ceremony, and pinning it would dilute the
four-pin depth strategy with a repo about process rather than outcomes. The program layer
lives here, one click from the profile, under the falsifiability rule in the
[charter](../charter.md).
