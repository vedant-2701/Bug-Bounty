# Track 09 — System Design Integration (Capstone)

Purpose: capstone track — do this last. Pulls from every other track in this curriculum and connects security explicitly to HLD/LLD practice, which is the core integration goal of this entire project.

### Security in HLD/LLD Documents 🔑
**Purpose:** this is the direct, practical fulfillment of "integrate security with system design" rather than treating it as a separate discipline — the actual skill of writing security considerations into a design doc as a first-class section, not an afterthought.
**Prerequisites:** all other tracks in this curriculum, ideally
**Core concept:** a security section in an HLD should cover: trust boundaries, threat model summary (Track 01), authn/authz approach (Track 02), data classification and protection (Track 04), and logging/monitoring plan (Track 06) — as standard sections, not optional extras.
**Primary resource:** find and study 2–3 public engineering design-doc templates that include a security section (several large tech companies publish theirs)
**Secondary resources:** your own past design docs, retroactively reviewed for what's missing
**Practice:** write a full HLD for a small system (e.g., a URL shortener, a file-upload service) with a complete security section
**Real-world example:** n/a — this is the synthesis exercise
**Cross-links:** defensive: every track in this curriculum feeds this one | offensive: Curriculum 1 (the vuln classes a good HLD should have already precluded)
**Expected outcome:** can produce a design doc where the security section would catch a reviewer's "what about X" questions before they're asked
**Notes:**
**Status:** not-started | difficulty: 5 | last-reviewed: | tags: [system-design, hld, capstone]

### Security Review Checklists
- Purpose: a practical artifact — a repeatable checklist you personally trust for reviewing your own or others' designs
- Primary resource: build this yourself from the OWASP ASVS, adapted to your own stack
- Practice: create your own checklist, then use it to review a real design doc
- Status: not-started

### Breach Case Studies Mapped to Design Flaws
- Purpose: the most concrete way to internalize why design-level security matters — trace a real breach back to a specific design decision, not just a coding bug
- Primary resource: use `incident_analysis.md` on 3–5 well-documented breaches (Capital One/SSRF, a supply-chain incident, an IAM misconfiguration incident)
- Practice: for each, identify the exact design-doc section that, if it had existed, would likely have caught the flaw
- Status: not-started
