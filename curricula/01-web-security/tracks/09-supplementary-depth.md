# Track 09 — Supplementary Depth (Not on PortSwigger)

Purpose: this track exists specifically because PortSwigger doesn't cover it, or covers it too shallowly for professional-level understanding. Dip into these as they become relevant to other tracks rather than working through sequentially.

### Cryptography Fundamentals for AppSec 🔑
**Purpose:** without this, padding oracle attacks, weak JWT signing, and TLS misconfig all stay "magic."
**Prerequisites:** none specific, but most useful after Track 05 (JWT)
**Core concept:** symmetric vs. asymmetric crypto, what a padding oracle actually reveals, HMAC vs. signature verification, why key length/algorithm choice matters.
**Primary resource:** "Crypto 101" (free, crypto101.io) or an equivalent applied-crypto primer — NOT a full cryptography course, just enough to reason about misuse
**Secondary resources:** PortSwigger's own coverage of padding oracle/JWT as the applied case studies
**Practice:** explain, in your own words, why reusing a JWT's HMAC secret as an RSA public key breaks alg-confusion defenses
**Real-world example:** any documented padding-oracle CBC attack write-up
**Cross-links:** offensive: JWT (Track 05) | defensive: Curriculum 3 Track 04 (secrets & data protection)
**Expected outcome:** can explain 3 common cryptographic misuse patterns without needing to derive the math
**Notes:**
**Status:** not-started | difficulty: 4 | last-reviewed: | tags: [cryptography, supplementary]

### HTTP/2 and HTTP/3 Attack Surface
- Purpose: request smuggling techniques diverge meaningfully with H2 downgrades; not deeply covered by PortSwigger's H1-centric labs
- Primary resource: PortSwigger Research blog — search for H2-specific desync posts
- Practice: read 2–3 research write-ups and summarize the H2-specific mechanism in your own words
- Status: not-started

### Browser Security Model Deep Dive
- Purpose: COOP/COEP, Site Isolation, fetch metadata headers — newer isolation primitives PortSwigger's CORS/clickjacking content doesn't cover
- Primary resource: web.dev's security section (Google) on cross-origin isolation
- Practice: identify which of these headers a real site sets and why
- Status: not-started

### CSP Authoring (vs. Bypass)
- Purpose: PortSwigger teaches bypassing CSP well; authoring a strong one is a different (and more directly Curriculum-3-relevant) skill
- Primary resource: OWASP CSP Cheat Sheet
- Practice: write a strict CSP for a small app and try to bypass your own policy
- Cross-links: defensive: Curriculum 3 Track 03 (secure coding) — this entry is a deliberate bridge topic
- Status: not-started
