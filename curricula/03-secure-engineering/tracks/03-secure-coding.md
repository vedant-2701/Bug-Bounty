# Track 03 — Secure Coding

Purpose: depends on Track 00. This is the day-to-day discipline layer — the practices that prevent most of Curriculum 1's vuln classes from ever existing in your own code.

### Input Validation & Output Encoding 🔑
**Purpose:** the actual fix behind SQLi, XSS, command injection, and SSTI — not "sanitize input" (too vague to implement correctly) but validation at the boundary + context-aware encoding at the output.
**Prerequisites:** Curriculum 1 Tracks 02 and 03 (injection, XSS)
**Core concept:** allow-listing over block-listing; the fact that a single "sanitize" function can never be correct for all output contexts — encoding must be context-specific (HTML body vs. attribute vs. JS string vs. URL).
**Primary resource:** OWASP Input Validation Cheat Sheet + OWASP XSS Prevention Cheat Sheet
**Secondary resources:** your language/framework's own escaping utilities documentation (e.g., a template engine's auto-escaping behavior)
**Practice:** take one Curriculum 1 XSS lab and write the actual defensive fix in real code, not just describe it
**Real-world example:** n/a
**Cross-links:** offensive: Curriculum 1 Tracks 02, 03 | this is the canonical defensive counterpart of both
**Expected outcome:** given a code snippet with a vuln, can write the correct context-aware fix, not just identify that a fix is needed
**Notes:**
**Status:** not-started | difficulty: 3 | last-reviewed: | tags: [secure-coding, input-validation]

### Secure Defaults & Framework-Specific Pitfalls
- Purpose: most frameworks are secure by default until a specific footgun is used — knowing your stack's footguns matters more than generic advice
- Primary resource: your primary backend framework's own security documentation section
- Practice: list 3 known footguns in the framework you actually use for backend work
- Status: not-started

### Secure Code Review Practices
- Purpose: a distinct skill from writing your own secure code — reviewing someone else's PR for security issues
- Primary resource: OWASP Code Review Guide
- Practice: review a real open-source PR (not your own code) specifically for security issues before checking if any were flagged in review
- Status: not-started
