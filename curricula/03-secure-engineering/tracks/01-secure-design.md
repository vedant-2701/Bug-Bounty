# Track 01 — Secure Design

Purpose: depends on Track 00. This is where "defense in depth" becomes an actual process rather than a slogan.

### Threat Modeling Frameworks 🔑
**Purpose:** the single highest-leverage secure-design skill — done well, it prevents entire classes of vulnerability before a line of code is written.
**Prerequisites:** Track 00
**Core concept:** STRIDE (Spoofing, Tampering, Repudiation, Info Disclosure, DoS, Elevation of Privilege) as a systematic enumeration technique; DREAD for rough risk scoring; PASTA for a more process-heavy, business-aligned approach; attack trees as a visualization tool.
**Primary resource:** OWASP Threat Modeling guidance + Adam Shostack's "Threat Modeling: Designing for Security" (book — the standard reference)
**Secondary resources:** Microsoft's STRIDE documentation (where it originated)
**Practice:** threat-model one system you've actually built (even a toy project) using STRIDE, end to end
**Real-world example:** find a public post-mortem where the root cause maps cleanly to a threat-modeling gap
**Cross-links:** defensive: feeds every other track in this curriculum | this is the track's flagship, the rest of this curriculum is largely "STRIDE applied to a specific domain"
**Expected outcome:** given a new system design, can produce a STRIDE-based threat model without a template to copy from
**Notes:**
**Status:** not-started | difficulty: 4 | last-reviewed: | tags: [threat-modeling, stride]

### Secure Architecture Patterns
- Purpose: recurring, reusable design shapes (e.g., API gateway as a chokepoint, sidecar pattern for enforcing policy) that reduce risk by construction
- Primary resource: Google's or Cloudflare's engineering blogs on architecture (see resources.md)
- Practice: identify which secure architecture pattern would have prevented a Curriculum 1 vulnerability class, per class
- Status: not-started

### Zero Trust Architecture
- Purpose: the modern default assumption for anything crossing a network boundary — "never trust, always verify," including internal traffic
- Primary resource: NIST SP 800-207 (Zero Trust Architecture)
- Practice: explain why zero trust changes the calculus for SSRF's impact (Curriculum 1 Track 04)
- Status: not-started
