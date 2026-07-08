# Track 06 — Specialized Testing

Purpose: depends on Track 05. These are testing contexts that need extra domain-specific technique beyond general manual testing.

### API & GraphQL Testing in Bounty Context
- Purpose: applies Curriculum 1 Track 07 mechanics using Curriculum 2's discovery techniques (Track 03) on real, often-undocumented APIs
- Primary resource: OWASP API Security Top 10 as a testing checklist
- Practice: for a permitted API target, test each OWASP API Top 10 category explicitly and document results even when negative
- Status: not-started

### Business Logic Edge Cases
- Purpose: deeper version of Track 05's business logic entry — specifically the edge cases that generic checklists miss
- Primary resource: n/a — pattern-matching skill built from your own findings log
- Practice: maintain a running list of "assumption categories" (ordering, timing, quantity limits, state transitions) and test each systematically
- Status: not-started

### Rate-Limit & WAF Bypass Techniques
- Purpose: often the actual blocker preventing you from confirming a suspected finding
- Primary resource: PortSwigger Research and disclosed write-ups on WAF bypass patterns
- Practice: identify the WAF/rate-limiter in front of a permitted target and document its detectable behavior (without necessarily bypassing it)
- Status: not-started
