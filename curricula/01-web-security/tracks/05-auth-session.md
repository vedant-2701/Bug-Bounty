# Track 05 — Authentication & Session Management

Purpose: depends on Cookies & Sessions (Track 00) and Access Control concepts (Track 04) being at least partially understood.

### Authentication Vulnerabilities 🔑
**Purpose:** the front door — flaws here often bypass every other control.
**Prerequisites:** Cookies & Sessions, Access Control basics
**Core concept:** username enumeration, brute-force/rate-limiting gaps, password reset flow flaws, MFA bypass patterns.
**Primary resource:** PortSwigger Authentication learning path
**Secondary resources:** OWASP Authentication Cheat Sheet
**Practice:** PortSwigger labs (wiener:peter account labs included); enumerate the wordlists provided and understand why they work
**Real-world example:** any disclosed password-reset-flow bounty report
**Cross-links:** offensive: JWT below | defensive: Curriculum 3 Track 02 (building AuthN) | bounty: Curriculum 2 Track 05
**Expected outcome:** given a login/reset flow, can list the 5 most likely failure points before testing
**Notes:**
**Status:** not-started | difficulty: 3 | last-reviewed: | tags: [authentication]

### OAuth Authentication
- Purpose: real-world OAuth is messier than the lab version — expect to supplement externally
- Primary resource: PortSwigger OAuth authentication learning path
- Secondary resources: oauth.net's own explainer for the flows PortSwigger doesn't fully dramatize (PKCE, device flow)
- Practice: PortSwigger labs; diagram the authorization code flow from memory afterward
- Status: not-started

### JWT Attacks 🔑
**Purpose:** extremely common in real APIs; a small number of misconfiguration patterns account for most findings.
**Prerequisites:** Authentication Vulnerabilities
**Core concept:** signature verification bypass (`alg: none`), algorithm confusion (RS256→HS256), key confusion via `jku`/`kid` header injection.
**Primary resource:** PortSwigger JWT attacks learning path
**Secondary resources:** jwt.io debugger (for structure inspection only, not as a payload generator you don't understand)
**Practice:** PortSwigger labs; manually construct a forged token by hand at least once before using a tool
**Real-world example:** search "JWT algorithm confusion bounty" on Hacktivity
**Cross-links:** offensive: Access Control (JWT often carries authz claims) | defensive: Curriculum 3 Track 02 (building JWT-based auth correctly) | bounty: Curriculum 2 Track 06
**Expected outcome:** given a JWT and its verification code, can identify which of the 3 classic misconfigurations (if any) applies
**Notes:**
**Status:** not-started | difficulty: 4 | last-reviewed: | tags: [jwt, authentication]
