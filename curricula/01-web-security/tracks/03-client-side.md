# Track 03 — Client-Side

Purpose: everything that lives in the browser's trust model. Depends on Same-Origin Policy (Track 01) — do not start XSS before that's solid.

### Cross-Site Scripting (XSS) 🔑
**Purpose:** still the most common web vuln class in the wild; foundational for DOM-based and prototype pollution later in this track.
**Prerequisites:** Same-Origin Policy, HTTP Fundamentals
**Core concept:** reflected vs. stored vs. DOM-based; context-aware output encoding as the actual fix (not "sanitize input").
**Primary resource:** PortSwigger XSS learning path
**Secondary resources:** OWASP XSS Prevention Cheat Sheet
**Practice:** all PortSwigger XSS labs across all three subtypes; write your own vulnerable-and-fixed toy page
**Real-world example:** any disclosed stored-XSS bounty report on HackerOne Hacktivity
**Cross-links:** offensive: CORS, DOM-based below | defensive: Curriculum 3 Track 03 (output encoding) | bounty: Curriculum 2 Track 05
**Expected outcome:** given a code snippet, can identify *which* output context it renders into and what encoding that context requires
**Notes:**
**Status:** not-started | difficulty: 3 | last-reviewed: | tags: [xss, client-side]

### Cross-Origin Resource Sharing (CORS) 🔑
**Purpose:** the most commonly *misconfigured* browser security mechanism, and a frequent bounty finding.
**Prerequisites:** Same-Origin Policy
**Core concept:** what CORS actually relaxes (not "the fix for CORS errors"); dangerous configs (reflected origin + credentials).
**Primary resource:** PortSwigger CORS learning path
**Secondary resources:** MDN CORS docs
**Practice:** PortSwigger labs; then find and document (don't exploit) a real CORS misconfig on a permitted test target
**Real-world example:** search Hacktivity for "CORS misconfiguration"
**Cross-links:** offensive: SSRF (Track 04) uses similar trust-boundary reasoning | defensive: Curriculum 3 Track 05 (API security) | bounty: Curriculum 2 Track 05/06
**Expected outcome:** can explain, precisely, why `Access-Control-Allow-Origin: *` combined with credentials is disallowed by browsers and why some sites still get this wrong
**Notes:**
**Status:** not-started | difficulty: 3 | last-reviewed: | tags: [cors, client-side]

### CSRF
- Purpose: classic trust-boundary abuse of the "browser automatically attaches cookies" behavior
- Primary resource: PortSwigger CSRF learning path
- Practice: PortSwigger labs; explain why SameSite cookies changed the threat landscape
- Status: not-started

### Clickjacking
- Purpose: short track, but a common low/medium bounty finding
- Primary resource: PortSwigger Clickjacking topic
- Practice: PortSwigger labs; identify X-Frame-Options vs CSP frame-ancestors as competing defenses
- Status: not-started

### DOM-Based Vulnerabilities
- Purpose: client-side-only version of injection — no server round-trip
- Primary resource: PortSwigger DOM-based topic
- Practice: PortSwigger labs; trace a source→sink manually in DevTools before checking the payload
- Status: not-started

### Prototype Pollution
- Purpose: JS-specific vuln class with both client- and server-side (Node.js) impact
- Primary resource: PortSwigger Prototype pollution topic
- Practice: PortSwigger labs; explain client-side vs server-side impact difference explicitly
- Status: not-started
