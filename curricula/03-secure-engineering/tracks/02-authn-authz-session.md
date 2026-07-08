# Track 02 — AuthN/AuthZ & Session Design

Purpose: the build-side counterpart of Curriculum 1 Track 05. Same domain, opposite lens — designing systems resistant to what you learned to exploit there.

### Building OAuth/OIDC Correctly 🔑
**Purpose:** OAuth misconfigurations are common precisely because implementing it correctly is genuinely harder than it looks.
**Prerequisites:** Curriculum 1 Track 05 (OAuth authentication, exploit side)
**Core concept:** authorization code flow with PKCE as the current best-practice default; why implicit flow is now discouraged; redirect URI validation as the most commonly botched control.
**Primary resource:** oauth.net's own best-practices documentation
**Secondary resources:** IETF OAuth 2.0 Security Best Current Practice RFC
**Practice:** diagram a full PKCE-based auth code flow from memory, labeling every point an attacker would target
**Real-world example:** any disclosed OAuth redirect_uri bypass report, read from the defender's "what would have prevented this" angle
**Cross-links:** offensive: Curriculum 1 Track 05 | this entry is the canonical defensive counterpart of that track's OAuth entry
**Expected outcome:** given an OAuth implementation, can identify whether it follows current best-practice flow selection and redirect validation
**Notes:**
**Status:** not-started | difficulty: 4 | last-reviewed: | tags: [oauth, authn]

### RBAC/ABAC Design
- Purpose: the design-side counterpart of Curriculum 1's Access Control track — how do you build authorization that doesn't produce IDORs
- Primary resource: OWASP Authorization Cheat Sheet
- Practice: design a role/attribute model for a small multi-tenant app on paper, then find the gaps yourself
- Status: not-started

### Session Architecture
- Purpose: server-side vs. stateless (JWT) session tradeoffs, done deliberately rather than by default
- Primary resource: OWASP Session Management Cheat Sheet
- Practice: for a hypothetical app, justify a session strategy choice (server-side vs JWT) with explicit tradeoffs, not just familiarity
- Status: not-started
