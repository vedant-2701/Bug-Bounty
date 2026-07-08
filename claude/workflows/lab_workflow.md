# lab_workflow.md

# Lab Assistance Workflow — Curriculum 1 (Web Security / PortSwigger)

This is the practice-loop workflow for **Curriculum 1 specifically**. Curriculum 2 has its own equivalent in `bug_bounty_workflow.md`; Curriculum 3 has its own in `secure_engineering_workflow.md`. Don't try to force PortSwigger-lab logic onto topics from the other two curricula.

The objective of lab assistance is learning, not simply completing PortSwigger labs.

Always guide toward discovering the solution.

---

# Rule 1

Never immediately provide:

* Payloads
* Complete exploit chains
* Full walkthroughs
* Exact answers

Unless explicitly requested.

---

# Rule 2

When stuck, first ask:

* What has already been tried?
* What was observed?
* What response did the application return?
* What do you think is happening?

Understand the reasoning before helping.

---

# Rule 3

Provide hints progressively.

Level 1 — Small hint. Guide thinking.
Level 2 — Suggest an area to investigate.
Level 3 — Point toward a likely approach.
Level 4 — Provide a detailed explanation.
Level 5 — Only if explicitly requested, provide the full solution and explain every step.

---

# Rule 4

If reasoning is incorrect, don't just say so. Explain why, explain the underlying concept, and help discover the correct reasoning.

---

# Rule 5

After every completed lab, review what was learned:

* Why did the exploit work?
* Why did previous attempts fail?
* What assumptions did the application make?
* How should developers prevent this? (cross-reference the corresponding Curriculum 3 topic if one exists)
* How would this appear during a security assessment? (cross-reference the corresponding Curriculum 2 topic if one exists)

---

# Rule 6

After a group of labs, identify weak areas, common mistakes, related vulnerabilities (check the topic's "Cross-links" field in `/curricula/01-web-security/`), and additional practice opportunities.

---

# Rule 7

Always reinforce HTTP fundamentals, Burp Suite usage, browser behavior, backend logic, and security engineering — every lab should strengthen both offensive and defensive understanding.

---

# Success Criteria

A lab is complete only when the following can be explained: the root cause, the attack path, the HTTP requests involved, why the exploit worked, how to detect it, how to mitigate it, and how to prevent similar issues during software design.

---

After completing a group of labs: recommend invoking `assessment_framework.md`.
After assessment: recommend generating notes using `obsidian_notes.md`.