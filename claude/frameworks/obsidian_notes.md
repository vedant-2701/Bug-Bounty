# obsidian_notes.md

# Standard Obsidian Note Template

Generate notes using this exact structure unless instructed otherwise. The objective is concise, revision-friendly, interconnected, and **queryable** notes — the frontmatter block is what makes the last part possible.

---

# Frontmatter (required)

Every note starts with this block. Without it, the vault can be linked but not queried (no "show me everything overdue for review" view via Dataview or similar).

```yaml
---
title:
curriculum: web-security | bug-bounty | secure-engineering
track:
status: not-started | in-progress | done | needs-review
difficulty: 1-5
last-reviewed:
next-review:
offensive_counterpart:
defensive_counterpart:
bounty_application:
tags: []
---
```

* `curriculum` / `track` — which of the three curricula and which track this belongs to, matching its location in `/curricula/`.
* `next-review` — set per the confidence-scoring rule in `assessment_framework.md`.
* `offensive_counterpart` / `defensive_counterpart` / `bounty_application` — the cross-curriculum links. Leave blank if none exists rather than forcing a connection.

---

# Title

Topic Name

---

# Overview

* Definition
* Purpose
* Why it exists
* Why it matters

---

# Prerequisites

List prerequisite concepts (should match the topic entry's "Prerequisites" field in `/curricula/`).

---

# Core Concepts

Summarize the important ideas. Avoid unnecessary detail.

---

# Attack Flow

Step-by-step: entry point, trust assumptions, exploitation process, result. (Applicable to Curriculum 1/2 topics; for Curriculum 3 topics, replace with a "Design Considerations" section covering the equivalent build-side reasoning.)

---

# HTTP Flow

Request, response, headers, cookies, parameters, session behavior. Include simplified examples when useful. (Curriculum 1/2 topics primarily.)

---

# Tooling Workflow

Which tools are used (Burp Suite for Curriculum 1; ffuf/nuclei/httpx/etc. for Curriculum 2; threat-modeling or code-review tooling for Curriculum 3), why, and what to observe.

---

# Practical Scenarios

Realistic examples — should resemble production applications rather than toy examples.

---

# Mitigation

Secure coding practices, backend protections, security controls, defense in depth.

---

# Detection

Logging, monitoring, indicators, security testing techniques.

---

# Engineering Perspective

Secure implementation, common coding mistakes, architectural considerations.

---

# Common Mistakes

Frequent misconceptions.

---

# Related Topics

List: prerequisites, related vulnerabilities/topics, advanced concepts — including topics in the *other* curricula (use the frontmatter cross-link fields above as the source of truth, expand here in prose).

Example:

Authentication → Sessions → Cookies → OAuth → JWT

---

# Interview Questions

Conceptual and scenario-based questions.

---

# Key Takeaways

Summarize the most important ideas.

---

# References

* Primary resource (PortSwigger topic / tool docs / OWASP page / standard, matching the curriculum entry)
* RFCs (if applicable)
* Additional recommended reading

Notes should be optimized for long-term revision rather than replacing the original learning resource.

---

When generating notes, cross-reference related notes whenever appropriate — the vault should become an interconnected knowledge graph rather than isolated notes.