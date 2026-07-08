# Track 07 — APIs

Purpose: modern attack surface — most real targets you'll encounter in bug bounty (Curriculum 2) are API-first.

### API Testing 🔑
**Purpose:** APIs are now the primary attack surface for most bounty targets; this track is the direct bridge into Curriculum 2's methodology.
**Prerequisites:** Access Control, Authentication, Injection tracks
**Core concept:** BOLA (broken object-level authorization), mass assignment, excessive data exposure, rate-limiting gaps — mechanics only; discovery/recon technique lives in Curriculum 2.
**Primary resource:** PortSwigger API testing learning path
**Secondary resources:** OWASP API Security Top 10
**Practice:** PortSwigger labs; then find a public API's OpenAPI/Swagger doc and map its authz model on paper
**Real-world example:** any disclosed BOLA report on Hacktivity — extremely common in 2020s API-first apps
**Cross-links:** offensive: Access Control (BOLA is API-flavored IDOR) | defensive: Curriculum 3 Track 05 (API/microservices security) | bounty: Curriculum 2 Track 03 (endpoint discovery) and Track 06 (specialized testing)
**Expected outcome:** given an API spec, can identify the 3 most likely BOLA/mass-assignment candidates before testing
**Notes:**
**Status:** not-started | difficulty: 4 | last-reviewed: | tags: [api, bola]

### GraphQL API Vulnerabilities
- Purpose: distinct discovery and exploitation patterns from REST — introspection, batching/DoS, injection through resolvers
- Primary resource: PortSwigger GraphQL API vulnerabilities learning path
- Practice: PortSwigger labs; enumerate the schema via introspection before checking the walkthrough
- Cross-links: bounty: Curriculum 2 Track 06
- Status: not-started

### Web LLM Attacks
- Purpose: newest PortSwigger addition — prompt injection against AI-powered application features (scanners, chatbots, agents embedded in web apps)
- Primary resource: PortSwigger Web LLM attacks learning path
- Practice: PortSwigger labs
- Notes: this is a fast-moving area — expect this entry to need real revision within a year of writing
- Status: not-started
