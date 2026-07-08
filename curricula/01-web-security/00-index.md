# Curriculum 1 — Web Security (MOC)

Backbone: PortSwigger Web Security Academy. This curriculum is *not* a copy of PortSwigger's own path order — it's reorganized around actual concept dependency, and it adds prerequisites, depth, and real-world grounding that PortSwigger doesn't provide.

## Why the order differs from PortSwigger's own learning paths

PortSwigger's paths are organized to be approachable for a first-time learner. This ordering optimizes instead for dependency: you shouldn't hit Auth/JWT before you understand cookies and sessions; Business Logic labs assume you can already do basic exploitation; Advanced HTTP topics assume core HTTP fluency.

## Track list & dependency map

```
00 Prerequisites
   └─→ 01 Core HTTP Mechanics
         ├─→ 02 Injection
         ├─→ 03 Client-Side
         │      └─→ 04 Access & Server Logic
         │             └─→ 05 Auth & Session
         │                    └─→ 06 Advanced HTTP
         │                           └─→ 07 APIs
         └─→ 08 Serialization & File Handling
   09 Supplementary Depth (crypto, HTTP/2-3, browser isolation) — dip in as needed, not strictly sequential
   10 Capstone — after everything above
```

| Track | Status | Notes |
|---|---|---|
| [00 Prerequisites](tracks/00-prerequisites.md) | not-started | HTTP, cookies, Burp, CLI, JS basics |
| [01 Core HTTP Mechanics](tracks/01-core-http-mechanics.md) | not-started | Same-origin policy, HTTP semantics |
| [02 Injection](tracks/02-injection.md) | not-started | SQLi, command injection, SSTI, NoSQLi |
| [03 Client-Side](tracks/03-client-side.md) | not-started | XSS, CSRF, clickjacking, CORS, DOM, prototype pollution |
| [04 Access & Server Logic](tracks/04-access-server-logic.md) | not-started | Access control, business logic, SSRF, race conditions |
| [05 Auth & Session](tracks/05-auth-session.md) | not-started | Authentication, OAuth, JWT |
| [06 Advanced HTTP](tracks/06-advanced-http.md) | not-started | Request smuggling, host header, cache poisoning/deception |
| [07 APIs](tracks/07-apis.md) | not-started | API testing, GraphQL, Web LLM attacks |
| [08 Serialization & File Handling](tracks/08-serialization-file-handling.md) | not-started | Deserialization, file upload, path traversal, XXE |
| [09 Supplementary Depth](tracks/09-supplementary-depth.md) | not-started | Crypto, HTTP/2-3, browser isolation, CSP authoring — **not on PortSwigger**, supplement externally |
| [10 Capstone](tracks/10-capstone.md) | not-started | Chained labs, mystery labs, Practitioner-exam prep |

## Not covered in depth by PortSwigger (verified against their live topic list)

PortSwigger currently covers, well: SQLi, XSS, CSRF, clickjacking, CORS, XXE, SSRF, request smuggling, command injection, SSTI, deserialization, path traversal, access control, authentication, OAuth, business logic, WebSockets, DOM-based, cache poisoning/deception, host header attacks, information disclosure, file upload, JWT, prototype pollution, GraphQL, race conditions, NoSQLi, API testing, and Web LLM attacks. That's broader than it gets credit for.

Genuine gaps → live in Track 09:
- Cryptography fundamentals (enough to actually understand padding oracle / weak JWT signing / TLS misconfig, not just complete the lab)
- HTTP/2 and HTTP/3-specific attack surface (desync techniques diverge from HTTP/1.1 smuggling)
- Browser security model depth: COOP/COEP, Site Isolation, fetch metadata
- CSP **authoring** (PortSwigger covers bypass well, not defensive authoring — this is also a bridge into Curriculum 3)

## Cross-curriculum links

- Curriculum 2 (Bug Bounty) applies everything here to live, undocumented targets — see its Track 05 (Manual Testing & Chaining).
- Curriculum 3 (Secure Engineering) covers the defensive-design counterpart of most tracks here — see its Track 00 (Foundations) for the explicit vocabulary bridge.

## Maintenance

Audit quarterly against https://portswigger.net/web-security/all-topics — new labs get added a few times a year (Web LLM attacks and race conditions are both fairly recent additions, GraphQL testing too).
