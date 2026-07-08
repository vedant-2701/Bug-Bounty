# bug_bounty_workflow.md

# Bug Bounty & Security Assessment Workflow — Curriculum 2

This is the practice-loop workflow for **Curriculum 2 (Bug Bounty) specifically**, and the methodology reference that Curriculum 2's Track 05 (Manual Testing & Chaining) points to. It complements `learning_workflow.md` and should be used only after gaining sufficient understanding of the relevant Curriculum 1 concepts.

---

# Guiding Principles

Always:

* Understand the application before testing it.
* Think like both an attacker and a defender.
* Follow a structured methodology.
* Respect the program's scope and rules (`curricula/02-bug-bounty/tracks/00-program-mechanics.md`).
* Prioritize understanding over automation.
* Document findings throughout the assessment.

Never:

* Test outside the authorized scope.
* Use destructive techniques without permission.
* Skip reconnaissance.
* Jump directly to payloads without understanding the application.

---

# Standard Assessment Workflow

## Stage 1 — Scope & Rules

Read the program policy, understand scope and out-of-scope assets, identify prohibited techniques, understand reporting requirements. Never proceed without this.

## Stage 2 — Reconnaissance

Build an understanding of the target: domains, subdomains, APIs, technologies, frameworks, authentication mechanisms, third-party integrations, static assets, public documentation. See `curricula/02-bug-bounty/tracks/02-recon-asset-discovery.md` and `03-content-endpoint-discovery.md` for technique detail.

**Stage 2.5 — Continuous Monitoring (ongoing, not one-off):** for a target you return to repeatedly, set up diffed/scheduled recon so new subdomains, endpoints, or changes surface automatically rather than requiring a full re-scan each time. See `curricula/02-bug-bounty/tracks/04-automation-pipelines.md`.

## Stage 3 — Application Mapping

Identify user roles, authentication flows, authorization boundaries, business workflows, API endpoints, file uploads, search functionality, administrative features, hidden functionality, input points. Think like a developer who built the application.

## Stage 4 — Attack Surface Analysis

Identify every place user-controlled input reaches the application: query parameters, path parameters, POST bodies, JSON, XML, headers, cookies, multipart forms, WebSockets, GraphQL, file uploads. Document each entry point.

## Stage 5 — Security Testing

Test methodically rather than randomly, applying Curriculum 1's mechanics: Authentication, Authorization, Input Validation, File Handling, Business Logic, API Testing, Client-Side Security. Business logic flaws often require creativity more than payloads.

---

# During Testing

Whenever a potential issue is found, don't immediately classify it as a vulnerability. Ask: is this expected behaviour? Can it be reproduced? Can it be exploited? What assumptions are required? What is the security and business impact? Think critically before reporting.

---

# Documentation

Record throughout: endpoint, request, response, observation, hypothesis, test performed, result, impact, evidence.

---

# Reporting

Document: summary, severity, root cause, steps to reproduce, HTTP requests/responses, proof of concept, business impact, security impact, mitigation, references. See `curricula/02-bug-bounty/tracks/07-reporting-professionalism.md` for report-craft depth.

**Platform-specific note:** report format expectations differ meaningfully between HackerOne, Bugcrowd, and Intigriti (duplicate handling, severity self-rating norms, triage SLAs). Check the specific program's platform before assuming a report template that worked elsewhere will fit.

---

# Post-Assessment Review

Reflect on: what vulnerabilities were found, which assumptions proved incorrect, which testing techniques were effective, which areas were overlooked, what should improve next time.

---

# Claude's Role

Act as mentor, security reviewer, technical discussion partner, methodology guide. Do not encourage testing outside authorized scope or jump directly to exploit payloads without discussing methodology first. Instead: encourage structured testing, ask questions that improve reasoning, suggest additional attack paths, recommend relevant Curriculum 1 topics when knowledge gaps appear, connect findings to Curriculum 3's mitigation practices.

---

# Completion Criteria

An assessment is complete only when the application has been systematically mapped, all major attack surfaces evaluated, findings validated and documented with evidence, mitigation strategies considered, and lessons learned recorded.