# Curriculum 2 — Bug Bounty (MOC)

Purpose: everything required beyond PortSwigger to function as a professional bug bounty hunter. Organized around the actual bounty workflow lifecycle (see `bug_bounty_workflow.md`), not as a tool list — tools rotate every 6–12 months, methodology doesn't.

## Volatility warning

Track 04 (Automation Pipelines) is explicitly the highest-churn part of this entire project. Expect to rewrite tool-specific content there every 6–12 months as ProjectDiscovery and the wider tooling ecosystem ships new releases. Tracks 00, 02, 05, 07 are comparatively stable — methodology, not tools.

## Track list

| Track | Status | Volatility |
|---|---|---|
| [00 Program Mechanics](tracks/00-program-mechanics.md) | not-started | low |
| [01 Environment & Tooling](tracks/01-environment-tooling.md) | not-started | medium |
| [02 Recon & Asset Discovery](tracks/02-recon-asset-discovery.md) | not-started | medium |
| [03 Content & Endpoint Discovery](tracks/03-content-endpoint-discovery.md) | not-started | medium |
| [04 Automation Pipelines](tracks/04-automation-pipelines.md) | not-started | **high** |
| [05 Manual Testing & Chaining](tracks/05-manual-testing-chaining.md) | not-started | low |
| [06 Specialized Testing](tracks/06-specialized-testing.md) | not-started | medium |
| [07 Reporting & Professionalism](tracks/07-reporting-professionalism.md) | not-started | low |
| [08 Continuous Practice](tracks/08-continuous-practice.md) | not-started | low |

## Dependencies

- Track 00 (program mechanics) first — legal/scope literacy before anything else.
- Track 01 (environment) before any of 02–04.
- Tracks 02–04 (recon → content discovery → automation) roughly sequential but iterative in practice — you'll cycle back constantly.
- Track 05 (manual testing) requires most of Curriculum 1 already completed — this is where that knowledge gets applied live.
- Track 06 depends on Track 05.
- Track 07 (reporting) applies from the first valid finding onward — don't wait until "done" to read it.
- Track 08 is ongoing, not a terminal stage.

## Cross-curriculum links

- Recon findings that reveal secrets/misconfig (Track 02/03) map directly to Curriculum 3 Track 04 (secrets & data protection) — what you find here is what you'd want to prevent as an engineer.
- Manual testing (Track 05) is the live-fire application of every Curriculum 1 vulnerability class.

## Maintenance

Revisit the ProjectDiscovery GitHub org and blog monthly; that alone will keep Track 04 from going stale.
