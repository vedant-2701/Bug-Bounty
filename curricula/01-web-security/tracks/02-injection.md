# Track 02 — Injection

Purpose: the oldest, still-most-damaging vulnerability class. Deliberately placed early because it's the easiest place to build the "root cause, not payload" habit that everything else depends on.

### SQL Injection 🔑
**Purpose:** old-but-gold — still responsible for major breaches; teaches the core injection mental model that transfers to every other injection type.
**Prerequisites:** HTTP Fundamentals, Burp Repeater/Intruder
**Core concept:** unsanitized input reaching a query interpreter; UNION-based, error-based, blind/time-based extraction; how prepared statements actually fix it (not just "escape quotes").
**Primary resource:** PortSwigger SQL injection learning path
**Secondary resources:** OWASP SQL Injection cheat sheet
**Practice:** all PortSwigger SQLi labs, then reproduce blind extraction manually before using sqlmap
**Real-world example:** any major SQLi-driven breach write-up (search "SQL injection data breach post-mortem")
**Cross-links:** offensive: NoSQLi, Command Injection below | defensive: Curriculum 3 Track 03 (input validation) | bounty: Curriculum 2 Track 05
**Expected outcome:** can explain why parameterized queries work at the interpreter level, not just recite "use prepared statements"
**Notes:**
**Status:** not-started | difficulty: 3 | last-reviewed: | tags: [injection, sqli]

### Command Injection 🔑
**Purpose:** highest-severity common injection class — direct RCE.
**Prerequisites:** SQL Injection (shares the mental model)
**Core concept:** user input reaching a shell interpreter; injection operators (`;`, `|`, `&&`); blind command injection via out-of-band techniques.
**Primary resource:** PortSwigger Command injection topic
**Secondary resources:** OWASP Command Injection cheat sheet
**Practice:** PortSwigger labs, then explain why allow-listing beats blocklisting here
**Real-world example:** Shellshock (CVE-2014-6271) as a case study — good candidate for `incident_analysis.md`
**Cross-links:** offensive: SSTI below | defensive: Curriculum 3 Track 03 | bounty: Curriculum 2 Track 05
**Expected outcome:** can explain the difference between in-band and blind/out-of-band command injection and when each detection method applies
**Notes:**
**Status:** not-started | difficulty: 3 | last-reviewed: | tags: [injection, rce]

### Server-Side Template Injection (SSTI)
- Purpose: bridges injection thinking into modern templating engines (Jinja2, FreeMarker, etc.)
- Primary resource: PortSwigger SSTI topic
- Practice: PortSwigger labs; identify the templating engine from error output before trying payloads
- Status: not-started

### NoSQL Injection
- Purpose: same root cause, different query language — good test of whether the mental model actually transferred
- Primary resource: PortSwigger NoSQL injection topic
- Practice: PortSwigger labs; explicitly write down how the injection differs syntactically from SQLi
- Status: not-started
