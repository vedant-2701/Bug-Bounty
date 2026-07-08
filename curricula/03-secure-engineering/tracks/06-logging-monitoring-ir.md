# Track 06 — Logging, Monitoring & Incident Response

Purpose: depends on Track 00. This is the "detect what prevention missed" layer — defense in depth in practice.

### Audit Logging Design 🔑
**Purpose:** without good logging, every other track in this curriculum is unverifiable after the fact — you can't detect what you didn't log.
**Prerequisites:** Track 00
**Core concept:** what to log (auth events, access-control decisions, admin actions) vs. what NOT to log (secrets, full request bodies with PII) — logging itself can become a data-protection liability if done carelessly.
**Primary resource:** OWASP Logging Cheat Sheet
**Secondary resources:** your cloud provider's audit logging service docs (CloudTrail, Cloud Audit Logs, etc.)
**Practice:** design the audit log schema for an authentication system, explicitly deciding what's excluded and why
**Real-world example:** any breach post-mortem where "we had no logs" or "logs didn't include the needed field" was cited as a root cause
**Cross-links:** offensive: connects to every Curriculum 1 track — this is the detection counterpart of exploitation
**Expected outcome:** given a system, can specify a logging schema that supports incident investigation without itself becoming a sensitive-data liability
**Notes:**
**Status:** not-started | difficulty: 3 | last-reviewed: | tags: [logging, detection]

### SIEM Basics & Alerting
- Purpose: logs are only useful if someone/something is watching them
- Primary resource: any major SIEM vendor's conceptual documentation (concepts transfer even if you don't use that specific product)
- Practice: define 3 alert rules you'd want for the audit log schema you designed above
- Status: not-started

### Incident Response Fundamentals
- Purpose: even as an engineer (not a dedicated IR role), understanding IR shapes how you design logging/monitoring
- Primary resource: NIST SP 800-61 (Computer Security Incident Handling Guide)
- Practice: walk through the NIST IR lifecycle (prepare, detect/analyze, contain/eradicate/recover, post-incident) for a hypothetical breach scenario
- Status: not-started
