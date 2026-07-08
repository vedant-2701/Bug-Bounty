# Track 07 — Secure SDLC & DevSecOps

Purpose: can be studied in parallel with Track 08. This is where security becomes a pipeline concern, not just a design concern.

### SAST/DAST/SCA in CI/CD 🔑
**Purpose:** automating security checks in the pipeline catches issues before they reach production — the practical, tooling-side implementation of "shift left."
**Prerequisites:** Track 00, basic CI/CD familiarity
**Core concept:** SAST (static analysis, source code) vs. DAST (dynamic analysis, running application) vs. SCA (software composition analysis, dependency vulnerabilities) — each catches a different class of issue and none replaces the others.
**Primary resource:** OWASP DevSecOps guideline
**Secondary resources:** your CI platform's own security-scanning integration docs (GitHub Advanced Security, GitLab, etc.)
**Practice:** add one SAST tool and one SCA tool to a real CI pipeline for a toy project
**Real-world example:** n/a
**Cross-links:** defensive: this is the automated-enforcement layer for every practice in Track 03 (secure coding)
**Expected outcome:** can explain which class of vulnerability each tool type would and wouldn't catch
**Notes:**
**Status:** not-started | difficulty: 3 | last-reviewed: | tags: [devsecops, sast-dast-sca]

### Supply Chain Security
- Purpose: dependency confusion, malicious packages, and unsigned artifacts are now a top-tier risk category — not optional in a 2024+ curriculum
- Primary resource: SLSA framework docs (supply-chain levels for software artifacts); Sigstore docs for artifact signing
- Practice: generate an SBOM (software bill of materials) for a real project using an open-source SBOM tool
- Status: not-started

### Secure SDLC Process
- Purpose: where in the development lifecycle each security activity (threat modeling, code review, testing) should happen
- Primary resource: NIST SP 800-218 (Secure Software Development Framework, SSDF)
- Practice: map Track 01 (threat modeling), Track 03 (secure coding), and this track's CI/CD checks onto a concrete SDLC timeline
- Status: not-started
