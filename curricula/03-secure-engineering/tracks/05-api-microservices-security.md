# Track 05 — API & Microservices Security

Purpose: the design-side counterpart of Curriculum 1 Track 07 (APIs) and Track 06 (request smuggling — gateway design is part of the fix there too).

### Rate Limiting & Abuse Prevention 🔑
**Purpose:** the most commonly missing control in real APIs — directly prevents brute force, scraping, and a chunk of business logic abuse.
**Prerequisites:** Track 00
**Core concept:** rate limiting by IP vs. by account vs. by API key — each has different bypass risks; the distinction between rate limiting (throughput) and abuse prevention (behavioral/pattern-based) more broadly.
**Primary resource:** OWASP API Security Top 10 (rate limiting category) + your API gateway's own rate-limiting documentation
**Secondary resources:** Cloudflare's blog on rate limiting architecture (see resources.md)
**Practice:** design a rate-limiting strategy for a login endpoint, explicitly stating what each layer defends against
**Real-world example:** n/a
**Cross-links:** offensive: Curriculum 1 Track 05 (Authentication — brute force), Curriculum 2 Track 06 (rate-limit bypass techniques, attacker side)
**Expected outcome:** given an endpoint, can design a layered rate-limiting approach and explain why single-layer IP-based limiting is insufficient
**Notes:**
**Status:** not-started | difficulty: 3 | last-reviewed: | tags: [rate-limiting, api-security]

### API Gateway Design
- Purpose: centralizes auth, rate limiting, and request validation — also the architectural fix for the front-end/back-end disagreement that enables request smuggling (Curriculum 1 Track 06)
- Primary resource: your chosen API gateway's (Kong, Envoy, AWS API Gateway, etc.) architecture documentation
- Practice: diagram where auth, rate limiting, and input validation each happen in a gateway-fronted architecture
- Status: not-started

### Service-to-Service Auth / mTLS
- Purpose: internal service traffic needs authentication too — a common zero-trust (Track 01) application
- Primary resource: your service mesh's (if any) mTLS documentation, or a general mTLS primer
- Practice: explain why mTLS matters even "inside" a private network
- Status: not-started
