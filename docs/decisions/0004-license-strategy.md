# 0004: License strategy

Status: accepted. Date: 2026-08-31.

## Context

The portfolio contains two kinds of material: runnable code (`twoseat`, `flightdeck`,
`leaseq`) and prose meant for reuse (`field-notes`). The audience is enterprise
engineering organizations, where license familiarity and patent language matter.

## Decision

- **Code repos: Apache-2.0.** The explicit patent grant and enterprise familiarity match
  the audience. I selected it in the repository creation flow, so the license predates the
  first line of code.
- **field-notes prose: CC BY 4.0.** The repo's stated purpose is to be reused with
  attribution; a code license is the wrong instrument for prose. GitHub's creation flow
  does not offer CC BY 4.0, so the license ships in the repo's first pull request as
  `LICENSE`, alongside `LICENSE-CODE` (Apache-2.0) covering code snippets embedded in
  notes, so a copied checklist script never needs a legal review.
- **This repo:** no license file. Profile and program-office content is personal record,
  not reusable material.

## Consequences

- Anyone republishing field-notes content owes attribution and nothing else, which is the
  point.
- Contributions to code repos arrive under Apache-2.0 terms via the license's own section
  5 (contributions submitted for inclusion fall under the same license absent a separate
  agreement), so the repos need no CLA at this scale. Revisit if outside contributions
  become routine.
