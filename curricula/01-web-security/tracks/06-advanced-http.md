# Track 06 — Advanced HTTP

Purpose: assumes strong HTTP fluency (Track 01). These are protocol-level subtleties, not application logic bugs.

### HTTP Request Smuggling 🔑
**Purpose:** high-severity, protocol-level desync attack; consistently produces critical findings when front-end/back-end servers disagree on request boundaries.
**Prerequisites:** HTTP Headers Deep Dive (Track 01)
**Core concept:** CL.TE / TE.CL / TE.TE desync between front-end proxy and back-end server; why this is a *disagreement* bug, not an input-validation bug.
**Primary resource:** PortSwigger Request smuggling learning path (written by the researcher — James Kettle — who popularized it)
**Secondary resources:** PortSwigger Research blog posts on smuggling — check for newer HTTP/2-specific variants
**Practice:** PortSwigger labs; diagram the two servers' differing interpretation of the same raw request before touching Burp
**Real-world example:** search PortSwigger Research for smuggling case studies against major CDNs
**Cross-links:** offensive: Track 09 (HTTP/2-specific desync is a supplementary deep-dive) | defensive: Curriculum 3 Track 05 (API gateway design) | bounty: Curriculum 2 Track 06
**Expected outcome:** can explain CL.TE vs TE.CL from first principles and predict which is exploitable given a described front-end/back-end pair
**Notes:**
**Status:** not-started | difficulty: 5 | last-reviewed: | tags: [request-smuggling, http]

### HTTP Host Header Attacks
- Purpose: password-reset poisoning and routing-based attacks both stem from trusting the Host header
- Primary resource: PortSwigger HTTP Host header attacks topic
- Practice: PortSwigger labs; identify every place an app trusts Host without validation
- Status: not-started

### Web Cache Poisoning
- Purpose: turns a client-side-looking bug into a stored, multi-victim attack via the cache layer
- Primary resource: PortSwigger Web cache poisoning learning path
- Practice: PortSwigger labs; identify the "unkeyed input" in each lab before reading the solution
- Status: not-started

### Web Cache Deception
- Purpose: inverse failure mode from poisoning — sensitive response gets cached and served to others
- Primary resource: PortSwigger Web cache deception topic
- Practice: PortSwigger labs
- Status: not-started
