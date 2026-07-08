# Track 00 — Foundations for Engineers

Purpose: the explicit bridge between "I can exploit this" (Curriculum 1) and "I can prevent this" (this curriculum). Do not skip even if Curriculum 1 is complete — the framing is genuinely different.

### OWASP Top 10 as Shared Vocabulary 🔑
**Purpose:** the common language between security engineers, backend engineers, and auditors — even though you already know the mechanics from Curriculum 1, you need the *engineering-facing* framing.
**Prerequisites:** Curriculum 1 broadly
**Core concept:** the OWASP Top 10 is a risk-communication tool, not a testing checklist — understand why it's organized the way it is (by risk category, not by root cause).
**Primary resource:** OWASP Top 10 (current version)
**Secondary resources:** OWASP ASVS — the verification-standard companion
**Practice:** map every Curriculum 1 track to its corresponding OWASP Top 10 category
**Real-world example:** n/a
**Cross-links:** offensive: all of Curriculum 1 | this entry is the canonical bridge — link everything else back here
**Expected outcome:** can translate between "IDOR" (offensive term) and "Broken Access Control" (OWASP category) fluently in either direction
**Notes:**
**Status:** not-started | difficulty: 2 | last-reviewed: | tags: [owasp, foundations]

### Security Mindset for Engineers
- Purpose: distinct from the attacker mindset (Curriculum 1/2) — this is "what could go wrong with what I'm about to ship," asked proactively, not reactively
- Primary resource: OWASP's secure coding practices quick-reference guide
- Practice: for your last non-security side project, retroactively list 3 security assumptions you made without realizing it
- Status: not-started

### Defense in Depth
- Purpose: the organizing principle behind every other track in this curriculum — no single control is ever "the fix"
- Primary resource: NIST's guidance on defense-in-depth (search NIST SP 800 series)
- Practice: for one vulnerability class from Curriculum 1, list 3 independent layers that would each need to fail for exploitation to succeed
- Status: not-started
