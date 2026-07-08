# secure_engineering_workflow.md

# Secure Engineering Practice Workflow — Curriculum 3

Curriculum 1 has PortSwigger labs. Curriculum 2 has real/practice targets. Curriculum 3 had no equivalent practice loop — this file fills that gap. Practice here means design exercises, threat modeling, and code review, not labs or live targets.

---

# Guiding Principles

Always:

* Start from a concrete artifact (a design doc, a real or realistic system, a real PR) — never practice this curriculum's topics in the abstract only.
* Apply Curriculum 1's vulnerability catalogue as the checklist of "what a good design should have already precluded."
* Treat every exercise as producing a reviewable output, not just a conversation.

Never:

* Let a design exercise stay purely verbal — write it down, even briefly.
* Skip threat modeling and jump straight to "here's the secure version" — the reasoning process is the actual skill being built.

---

# Three Exercise Types

This curriculum's practice takes one of three shapes. Identify which one a given topic calls for (check the topic entry's "Practice" field in `/curricula/03-secure-engineering/`).

## Type 1 — Design Exercise

Used for: secure design, API/microservices security, cloud/infra, system design integration topics.

1. Start from a concrete system (real or a small, well-specified hypothetical — e.g., "a URL shortener," "a file-upload service").
2. Produce the requested artifact: an architecture diagram, an IAM policy, a rate-limiting strategy, a design-doc security section.
3. Self-review against Curriculum 1's relevant vulnerability classes: for each, could this design still be exploited that way? If yes, revise.
4. State explicitly what tradeoff was made and why (cost, complexity, latency vs. security gained) — a design with no stated tradeoffs hasn't been thought through.

## Type 2 — Threat Modeling Walkthrough

Used for: Track 01 (secure design) and any topic where STRIDE/DREAD/PASTA applies.

1. Pick the system under study.
2. Enumerate trust boundaries and data flows first, before enumerating threats — threats without boundaries drawn first tend to be generic and unhelpful.
3. Walk each STRIDE category against each boundary/flow systematically. Don't stop at the first plausible threat per category — a real threat model finds several per system.
4. For each identified threat, state the specific mitigating control, not a vague "add validation."

## Type 3 — Secure Code Review Walkthrough

Used for: Track 03 (secure coding) and any hands-on review practice.

1. Use a real piece of code — a real open-source PR is better practice than a toy snippet, because real code has ambiguity a toy snippet doesn't.
2. Review specifically for the vulnerability classes relevant to the current topic (don't try to review for everything at once — that produces shallow review).
3. For anything flagged, explain *why* it's a risk (root cause) before proposing the fix.
4. Compare notes against the PR's actual review comments (if available) afterward — this is the feedback loop that improves review instinct over time.

---

# Progressive Hint Structure (mirrors lab_workflow.md)

When stuck on any of the three exercise types:

Level 1 — ask what threat models / patterns have already been considered.
Level 2 — point toward which OWASP ASVS or NIST SSDF section is relevant.
Level 3 — suggest which specific control category to investigate.
Level 4 — walk through the reasoning for one example threat/flaw in detail.
Level 5 — only if explicitly requested, provide a complete worked design/threat-model/review.

---

# Completion Criteria

An exercise is complete only when there is a written artifact (not just a verbal exchange), the artifact has been explicitly self-reviewed against the relevant Curriculum 1 vulnerability classes, tradeoffs are stated, and the reasoning process — not just the final answer — can be explained.

---

After completing an exercise: recommend invoking `assessment_framework.md`.
After assessment: recommend generating notes using `obsidian_notes.md`.