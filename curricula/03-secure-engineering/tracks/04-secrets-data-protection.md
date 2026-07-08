# Track 04 — Secrets & Data Protection

Purpose: what Curriculum 2's recon tracks (subdomain/JS/GitHub recon) find is very often exactly what this track is meant to prevent. Read those tracks' entries for the attacker-side mirror.

### Secrets Management 🔑
**Purpose:** leaked secrets (API keys, credentials, tokens) are among the most common and most damaging findings in real bug bounty recon — this is the direct defensive counterpart.
**Prerequisites:** Track 00
**Core concept:** never commit secrets to source control; centralized secret stores (Vault, cloud KMS/Secrets Manager) over environment-variable sprawl; rotation as a first-class operational requirement, not an afterthought.
**Primary resource:** HashiCorp Vault docs (concepts section) or your cloud provider's secrets manager docs
**Secondary resources:** `git-secrets` / `trufflehog` docs — read defensively, as scanning tools you'd run in CI
**Practice:** set up a basic secrets store (even locally) and migrate one hardcoded credential from a toy project into it
**Real-world example:** any disclosed "secret in public repo" bounty report, read from the "how should this have been prevented" angle
**Cross-links:** offensive: Curriculum 2 Track 02 (OSINT/GitHub dorking), Track 03 (JS recon) | this track is what those tracks' findings should motivate you to prevent
**Expected outcome:** can explain the operational argument for centralized secrets management beyond "don't commit secrets"
**Notes:**
**Status:** not-started | difficulty: 3 | last-reviewed: | tags: [secrets, data-protection]

### Encryption at Rest & In Transit
- Purpose: baseline data protection controls, correctly applied rather than checkbox-applied
- Primary resource: OWASP Cryptographic Storage Cheat Sheet
- Practice: for a hypothetical system, specify what's encrypted at rest, in transit, and explicitly what is NOT (and why)
- Status: not-started

### Key Management
- Purpose: encryption is only as strong as key management — this is where most crypto implementations actually fail
- Primary resource: NIST SP 800-57 (key management guidance) — read the practical sections, not the full spec
- Practice: explain key rotation and its operational cost tradeoffs for a system you've designed
- Status: not-started

### Data Classification
- Purpose: you can't protect data appropriately without first classifying its sensitivity
- Primary resource: any standard data classification framework (public/internal/confidential/restricted is common)
- Practice: classify the data types in a hypothetical app you've designed
- Status: not-started
