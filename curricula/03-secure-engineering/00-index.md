# Curriculum 3 — Secure Engineering (MOC)

Purpose: connects security to backend engineering, system design, HLD, and LLD. Organized by SDLC phase / architecture layer — the way a backend engineer actually thinks, not by vulnerability class (that's Curriculum 1's job).

## Integration principle

This curriculum does not re-explain vulnerability mechanics — every track's "Foundations" links back to the canonical Curriculum 1 entry. What's unique here is the **build/design lens**: how do you architect systems that don't have these problems in the first place.

## Track list

| Track | Status |
|---|---|
| [00 Foundations for Engineers](tracks/00-foundations.md) | not-started |
| [01 Secure Design](tracks/01-secure-design.md) | not-started |
| [02 AuthN/AuthZ & Session Design](tracks/02-authn-authz-session.md) | not-started |
| [03 Secure Coding](tracks/03-secure-coding.md) | not-started |
| [04 Secrets & Data Protection](tracks/04-secrets-data-protection.md) | not-started |
| [05 API & Microservices Security](tracks/05-api-microservices-security.md) | not-started |
| [06 Logging, Monitoring & Incident Response](tracks/06-logging-monitoring-ir.md) | not-started |
| [07 Secure SDLC & DevSecOps](tracks/07-secure-sdlc-devsecops.md) | not-started |
| [08 Cloud & Infrastructure Security](tracks/08-cloud-infrastructure.md) | not-started |
| [09 System Design Integration](tracks/09-system-design-integration.md) | not-started |

## Dependencies

- Track 00 first — establishes shared vocabulary with Curriculum 1.
- Track 01 (secure design/threat modeling) before 02–06, since those are all applications of design thinking to specific domains.
- Track 07 (SDLC/DevSecOps) and Track 08 (cloud/infra) can be studied in parallel once 01–06 are underway.
- Track 09 (system design integration) is the capstone — do this last, it pulls from every other track.

## Cross-curriculum links

- Track 00 ↔ Curriculum 1's entire vuln-class catalogue (shared vocabulary)
- Track 02 ↔ Curriculum 1 Track 05 (Auth & Session) — same concept, build lens instead of exploit lens
- Track 04 ↔ Curriculum 2 Tracks 02/03 (what a hunter finds is what this track prevents)
- Track 05 ↔ Curriculum 1 Track 07 (APIs) and Curriculum 1 Track 06 (request smuggling — gateway design is the fix)
- Track 08 ↔ Curriculum 1 Track 04 (SSRF — cloud IAM/network segmentation is the fix)

## Maintenance

This track set changes at a *medium* cadence — tracks standards bodies (OWASP ASVS, NIST SSDF) rather than tool churn. Review annually against the current ASVS version and NIST SSDF guidance.
