# Track 04 — Access Control & Server-Side Logic

Purpose: server-side trust-boundary failures. Depends on Track 03 conceptually (same "trust assumption gets violated" pattern, now server-side).

### Access Control / IDOR 🔑
**Purpose:** among the highest-frequency real-world findings in bug bounty; deceptively simple, easy to underestimate.
**Prerequisites:** HTTP Fundamentals, Authentication basics (can be studied in parallel with Track 05)
**Core concept:** horizontal vs. vertical privilege escalation; the difference between authentication ("who are you") and authorization ("what can you do") — the root cause of nearly every access control bug is confusing the two.
**Primary resource:** PortSwigger Access control learning path
**Secondary resources:** OWASP Access Control Cheat Sheet
**Practice:** PortSwigger labs; then manually enumerate object IDs on a permitted test target and predict which will be vulnerable before testing
**Real-world example:** search Hacktivity for "IDOR" — extremely common report type, good pattern library
**Cross-links:** offensive: Business Logic below | defensive: Curriculum 3 Track 02 (RBAC/ABAC design) | bounty: Curriculum 2 Track 05 (flagship chaining target)
**Expected outcome:** given an endpoint and a role model, can predict likely horizontal and vertical access control failures before testing
**Notes:**
**Status:** not-started | difficulty: 3 | last-reviewed: | tags: [access-control, idor]

### Server-Side Request Forgery (SSRF) 🔑
**Purpose:** one of the highest-impact vuln classes in cloud environments — frequently the pivot into internal infrastructure.
**Prerequisites:** Same-Origin Policy, HTTP Fundamentals
**Core concept:** the server itself becomes the attacker's proxy; cloud metadata endpoints (169.254.169.254) as the classic high-impact target; blind vs. non-blind SSRF.
**Primary resource:** PortSwigger SSRF learning path
**Secondary resources:** cloud provider docs on their metadata service (AWS IMDS, GCP metadata server) — read defensively, not offensively
**Practice:** PortSwigger labs; explain why IMDSv2 was introduced as a mitigation
**Real-world example:** the 2019 Capital One breach (SSRF → IMDS → S3 access) — strong candidate for `incident_analysis.md`
**Cross-links:** offensive: chains into Access Control findings | defensive: Curriculum 3 Track 08 (cloud/infra security) | bounty: Curriculum 2 Track 02 (cloud recon)
**Expected outcome:** can explain why SSRF is disproportionately dangerous in cloud environments specifically, not just "server makes a request it shouldn't"
**Notes:**
**Status:** not-started | difficulty: 4 | last-reviewed: | tags: [ssrf, cloud]

### Business Logic Vulnerabilities
- Purpose: requires creativity more than payloads — a different testing muscle than injection/XSS
- Primary resource: PortSwigger Business logic vulnerabilities learning path
- Practice: PortSwigger labs; for each lab, write down the *assumption* the developer made that turned out false
- Cross-links: bounty: Curriculum 2 Track 05/06 (this is where business logic really pays off)
- Status: not-started

### Race Conditions
- Purpose: relatively recent PortSwigger addition, increasingly common in bounty reports (limit-overrun races especially)
- Primary resource: PortSwigger Race conditions learning path
- Practice: PortSwigger labs; explain the difference between limit-overrun and single-endpoint races
- Status: not-started
