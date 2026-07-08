# Track 01 — Core HTTP Mechanics

Purpose: the mechanics that CORS, CSRF, request smuggling, and cache poisoning all secretly depend on. Skipping this track is the most common reason those later topics feel like magic.

### Same-Origin Policy 🔑
**Purpose:** the single most important trust boundary in the browser — nearly every client-side vuln is a bypass of this.
**Prerequisites:** HTTP Fundamentals
**Core concept:** origin = scheme + host + port; why the browser enforces this; what it does and doesn't protect.
**Primary resource:** MDN "Same-origin policy"
**Secondary resources:** PortSwigger CORS learning path (as the applied case)
**Practice:** predict, before checking, whether two given URLs are same-origin
**Real-world example:** any disclosed CORS misconfig bounty report (search HackerOne Hacktivity for "CORS")
**Cross-links:** offensive: Track 03 (CORS, CSRF, DOM-based) | defensive: Curriculum 3 Track 02 | bounty: Curriculum 2 Track 05
**Expected outcome:** can explain, from first principles, why a `<script>` tag can load cross-origin but `fetch()` can't read the response
**Notes:**
**Status:** not-started | difficulty: 3 | last-reviewed: | tags: [sop, browser-security]

### HTTP Headers Deep Dive
- Purpose: needed before host-header attacks, cache poisoning, and CORS bypasses
- Primary resource: MDN HTTP headers reference
- Practice: identify security-relevant headers (CSP, HSTS, X-Frame-Options, Set-Cookie flags) on 5 real sites
- Status: not-started

### Statelessness & How Sessions Fake State
- Purpose: bridges into Track 05
- Primary resource: PortSwigger "Essential skills" learning path intro material
- Practice: trace a session cookie across 3 requests and explain what the server does with it
- Status: not-started
