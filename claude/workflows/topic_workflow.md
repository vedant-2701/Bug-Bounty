# topic_workflow.md

# Standard Topic Workflow

This document defines the workflow followed whenever a new topic is started, from any of the three curricula in `/curricula/`. It replaces the old PortSwigger-only version — several sections below explicitly branch by curriculum type, and none of the completion criteria assume Burp Suite or PortSwigger labs by default.

---

# Stage 0 — Identify the Curriculum

Before anything else, identify which curriculum the topic belongs to:

* **Curriculum 1 — Web Security** (`curricula/01-web-security/`): PortSwigger-backboned, vulnerability mechanics
* **Curriculum 2 — Bug Bounty** (`curricula/02-bug-bounty/`): methodology, recon, tooling
* **Curriculum 3 — Secure Engineering** (`curricula/03-secure-engineering/`): design, architecture, backend implementation

This determines which practice/completion branch applies in Stages 5 and 9 below. If unclear, check the topic entry's location in `/curricula/` — it's already filed under the right curriculum and track.

---

# Stage 1 — Topic Preparation

When a topic name or resource is provided, do NOT immediately start teaching it. Prepare first.

## 1. Topic Overview

* What is this topic?
* Why is it important?
* Where is it used in real-world applications?
* Why should backend engineers, system designers, and bug bounty hunters understand it?

## 2. Prerequisites

Pull from the topic entry's own "Prerequisites" field in `/curricula/`. Classify each as Required / Recommended / Optional. If prerequisites are missing, recommend learning them first before proceeding.

## 3. Learning Objectives

Pull from the topic entry's "Expected outcome" field — practical, can-do objectives, not memorization targets.

## 4. Topic Breakdown

If the topic entry is a flagship (🔑, full template), break it into logical subtopics with purpose, difficulty, importance, and common misconceptions for each. If it's a lightweight entry, this stage can be brief — don't manufacture subtopic structure that isn't there.

## 5. Practice Format (branches by curriculum)

* **Curriculum 1:** explain which Burp tools will be used, why, and what to observe. Without spoilers, describe lab count/progression if known.
* **Curriculum 2:** explain which tools/targets apply, what a valid vs. out-of-scope test looks like for this topic, and what "done" looks like even without a finding.
* **Curriculum 3:** explain what design artifact or review exercise this topic produces (a threat model, a design-doc section, code review notes) — there is no lab to spoil here, so this stage can be more directly explained upfront.

## 6. Additional Concepts

Identify concepts that are closely related, frequently confused, common interview topics, or important but not deeply covered by the primary resource. Check the topic entry's "Cross-links" field in `/curricula/` for concepts already flagged in the other two curricula.

## 7. Practical Applications

Explain where this concept appears in production applications, APIs, cloud systems, enterprise software, and microservices.

## 8. Completion Criteria (branches by curriculum)

Completion always requires: understanding, practical ability, ability to explain the concept, interview readiness. Additionally:

* **Curriculum 1:** the relevant PortSwigger lab(s) solved, Burp Suite usage demonstrated.
* **Curriculum 2:** a documented test against a real or intentionally-vulnerable target — a finding or a documented negative result, either is fine.
* **Curriculum 3:** a reviewable artifact — completed threat model, design-doc section, or code review notes.

Reading alone is never sufficient, regardless of curriculum.

## 9. Suggested Learning Strategy

Recommend the best order for the subtopics if there are any. Highlight areas deserving extra attention. Do not provide deep explanations yet — wait until the person begins studying or asks questions.

---

# During Theory Study

Fill knowledge gaps, clarify confusing ideas, explain terminology, connect concepts together, compare similar vulnerabilities/patterns, explain trade-offs. Provide intuition rather than repeating the primary resource. Avoid duplicating the lesson unless explicitly requested.

---

# After Topic Completion

Update the topic's status in its curriculum track file and in the curriculum's `00-index.md` if the dependency map is affected. If new dependencies, gaps, or related topics were discovered during the discussion, add them to the relevant topic entries directly rather than waiting.

Then proceed per the standard lifecycle in `learning_workflow.md`: knowledge review (`assessment_framework.md`), note generation (`obsidian_notes.md`).