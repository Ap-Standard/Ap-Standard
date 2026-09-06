# 0007: Visual scope

Status: accepted. Date: 2026-09-06. Extends [0005](0005-portfolio-reset.md), item 7.

## Context

Item 7 of [0005](0005-portfolio-reset.md) capped this profile at one generated image per code repo,
one diagram, and three linked badges. On 2026-09-05 I asked whether to break it for an interactive
arcade-style page, and whether colored badges and certification images would make the profile less
plain. The only controlled experiment on creative application formats (BI Norwegian Business
School, 90 evaluators, identical content) halved interview odds, 41% to 27%, and a Robert Half
survey of 600 senior managers ranked cartoon imagery and colorful backgrounds at the top of what
hurts a candidate. Documented game-resume successes belong to creatives whose game was the work
sample, inverting the thesis here: the judgment is mine, the typing is not. PMI also restricts the
PMP logo to business cards and signature blocks.

## Decision

1. **The live flightdeck card stays the only image on this profile.** No screenshot, GIF, animated
   SVG, stat card, trophy, streak, or visitor counter.
2. **Badges stay at three per code repo**, each linked to the thing it measures. No decorative or
   tech-stack badges.
3. **Certifications stay plain text.** `PMP, CSM.` is the whole line. No certification image,
   verification link, or badge service.
4. **One text link to a trace page is permitted**, to `loop.html` on flightdeck's Pages, under the
   Mermaid fence, once flightdeck reports 14 measured nights. Linking "1 of 1" advertises thin data.

## Consequences

- This profile will not produce an arcade reaction. That is the intended outcome, not a compromise:
  it is built for a hiring manager's ninety-second read late in the funnel.
- The restraint is on the record with its evidence, so "why is it so plain" now has an answer that
  is a decision rather than an omission.

## Alternative rejected

Build the visual layer as an interactive artifact: a platformer-style mini-game, a cart-racing
arcade variant, or a judgment game dealing out twoseat's benchmark corpus on a fourth repo, plus
decorative badges, a stat card, certification images, and an animated SVG. Rejected on three
counts. It maps to zero dimensions of a TPM interview rubric, which scores execution, technical
judgment, influence, and risk, never shipped code. A published takedown record shows rights holders
enforcing against arcade clones under the account name hosting them, and enforcement follows
visibility, which was the entire goal. And the ADR permitting it could only state its Context as
"wanted it to look impressive", beside the ADR that cut a repo for not proving the thesis.
