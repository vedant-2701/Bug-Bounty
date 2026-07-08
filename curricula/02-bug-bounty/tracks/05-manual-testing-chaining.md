# Track 05 — Manual Testing & Vulnerability Chaining

Purpose: this is where Curriculum 1's mechanics meet real, undocumented targets. Requires most of Curriculum 1 completed. Follow `bug_bounty_workflow.md` for the full methodology this track applies.

### Applying Vulnerability Knowledge to Live Targets 🔑
**Purpose:** the core translation skill — PortSwigger labs are clean and isolated; real targets are messy, and this is where that gap gets closed.
**Prerequisites:** most of Curriculum 1, Tracks 00–04 of this curriculum
**Core concept:** systematic application mapping before testing (per `bug_bounty_workflow.md` Stage 3); testing methodically per attack surface category rather than randomly trying payloads.
**Primary resource:** `bug_bounty_workflow.md` (this project's own methodology document) as the primary process guide
**Secondary resources:** public disclosed reports as pattern libraries (Hacktivity, Bugcrowd/Intigriti blogs)
**Practice:** pick one permitted target, map it fully (roles, flows, entry points) before testing a single input
**Real-world example:** any well-documented disclosed report showing the mapping-then-testing process explicitly
**Cross-links:** offensive: all of Curriculum 1 | bounty: this is the track everything else in Curriculum 2 feeds into
**Expected outcome:** given a new target, can produce an attack-surface map before writing a single payload
**Notes:**
**Status:** not-started | difficulty: 4 | last-reviewed: | tags: [manual-testing, methodology]

### Vulnerability Chaining 🔑
**Purpose:** most high-severity real-world findings are chains of individually low/medium issues, not single critical bugs.
**Prerequisites:** Applying Vulnerability Knowledge (above)
**Core concept:** how a low-severity info disclosure + an access control gap + a business logic flaw combine into a critical finding; thinking in terms of achievable *impact*, not individual bug classes.
**Primary resource:** disclosed critical-severity reports on Hacktivity — read several end-to-end specifically for the chaining logic
**Secondary resources:** conference talks on "bug chaining" (search DEF CON/BSides talks)
**Practice:** for one of your own low-severity findings, deliberately brainstorm 3 ways it could combine with something else to increase impact
**Real-world example:** search Hacktivity for "chained" or "combined with" in report titles
**Cross-links:** offensive: Access Control, Business Logic (Curriculum 1 Track 04) | bounty: Reporting (Track 07) — chained findings need careful impact articulation
**Expected outcome:** given a single low-severity finding, can reason concretely about what it would take to escalate its impact
**Notes:**
**Status:** not-started | difficulty: 5 | last-reviewed: | tags: [chaining, methodology]

### Business Logic Testing in the Wild
- Purpose: real business logic is far messier than PortSwigger's clean labs — this is deliberate additional practice
- Primary resource: no single resource — this is built from experience + disclosed reports
- Practice: for a permitted target, list every workflow assumption you can find (limits, approvals, ordering) and test each deliberately
- Status: not-started
