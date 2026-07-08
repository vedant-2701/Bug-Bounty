# learning_workflow.md

# Web Security, Bug Bounty & Secure Engineering — Learning Workflow

## Purpose

This document defines the overall session lifecycle. It does not contain the detailed logic for any individual stage — that logic lives in the file that owns each stage. This file's only job is philosophy plus the map between stages and owning files.

The objective is not merely to complete PortSwigger Academy, but to develop the skills of a:

* Security Engineer
* Backend Engineer
* System Designer
* Penetration Tester
* Professional Bug Bounty Hunter

Every topic — whichever of the three curricula it belongs to — should improve understanding from both the offensive and defensive perspective where that's applicable.

---

# Learning Philosophy

Always prioritize:

* Deep understanding over memorization
* Reasoning over payload memorization
* Practical skills over passive reading
* Security engineering over exploitation alone
* Consistency over speed

The goal is to understand:

* Why a vulnerability exists
* How attackers discover and exploit it
* How defenders prevent it
* How engineers should design systems to avoid it

---

# The Standard Topic Lifecycle

Every topic, regardless of which curriculum it comes from, follows the same nine stages. **The detail for each stage lives in its owning file — do not re-derive it here.**

| Stage | Owning file |
|---|---|
| 1. Topic Preparation | `workflows/topic_workflow.md` |
| 2. Study the primary resource | (the topic entry's own "Primary resource" field in `/curricula/`) |
| 3. Deep Understanding & Discussion | `frameworks/thinking_framework.md`, triggered via `prompts/deep_understanding.md` |
| 4. Practice (labs / live targets / design exercises) | `workflows/lab_workflow.md` (Curriculum 1), `workflows/bug_bounty_workflow.md` (Curriculum 2), `workflows/secure_engineering_workflow.md` (Curriculum 3) |
| 5. Knowledge Review | `frameworks/assessment_framework.md`, triggered via `prompts/post_lab_review.md` |
| 6. Additional Practice | the topic entry's own "Practice" / external-resource fields |
| 7. Note Generation | `frameworks/obsidian_notes.md`, triggered via `prompts/notes_generation.md` |
| 8. Interview & Revision | `frameworks/assessment_framework.md` |
| 9. Move to the next topic | the owning curriculum's `00-index.md` dependency map |

Never skip a stage. Never re-implement a stage's logic in this file — if you notice this table drifting from what the owning files actually say, fix the owning file, not this table.

---

# Curriculum-Specific Notes

The lifecycle is the same across all three curricula, but stage 4 (practice) and the completion definition look different by curriculum:

* **Curriculum 1 (Web Security):** practice = PortSwigger labs, completion requires the lab being solved and Burp Suite usage demonstrated.
* **Curriculum 2 (Bug Bounty):** practice = applying methodology to a real or intentionally-vulnerable target within scope, completion requires a documented finding or a documented negative result (not every session produces a bug, and that's fine).
* **Curriculum 3 (Secure Engineering):** practice = a design exercise, threat model, or code review, completion requires a reviewable artifact (a design doc section, a completed threat model, review notes on a real PR) — there is no "lab" to solve.

Do not force Curriculum 2 or 3 topics through Curriculum 1's Burp/lab-shaped completion criteria — that's a category error that breaks the workflow for two-thirds of the project's content.

---

# Continuous Improvement

If you discover missing prerequisites, missing concepts, useful practice resources, or better explanations, add them to the relevant curriculum topic entry during the discussion instead of waiting until the end.

---

# Maintenance Rituals

* **Quarterly:** audit each curriculum's track list against its upstream source — PortSwigger's current topic list for Curriculum 1, the current bounty tooling landscape (ProjectDiscovery especially) for Curriculum 2, current OWASP ASVS / NIST SSDF guidance for Curriculum 3. Log any changes in `meta/changelog.md`.
* **Never delete** a topic entry or note that's gone stale (an old tool, a superseded technique) — mark it archived instead, so learning history is preserved.
* **Review scheduling:** a topic's next-review date, set during assessment (see `frameworks/assessment_framework.md`), is the mechanism for revisiting completed material over time. Don't rely on memory to know what needs revision.