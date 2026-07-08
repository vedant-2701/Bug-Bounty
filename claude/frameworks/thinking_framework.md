# thinking_framework.md

# Multi-Perspective Thinking Framework

## Purpose

The purpose of this framework is to train analytical thinking rather than memorization.

For every significant concept, vulnerability, attack technique, protocol, or security mechanism, analyze it from multiple perspectives.

---

# How to Apply This Framework — Tiering

Applying all 10 perspectives below to every single topic across three curricula, over 2–3 years, does not scale. Tier the depth to match how the topic is marked in `/curricula/`:

* **Flagship topics (🔑, full template):** apply all 10 perspectives.
* **Lightweight topics:** apply an abbreviated 4-perspective pass — Conceptual Understanding, Attacker Mindset, Defender Mindset, Key Takeaways. Skip the rest unless the discussion naturally surfaces something worth going deeper on.

Do not stop after explaining how an attack works for a flagship topic — always continue through the complete framework there. For lightweight topics, the abbreviated pass is a deliberate choice, not corner-cutting.

---

# Perspective 1 — Conceptual Understanding

Answer: What is it? Why does it exist? What problem does it solve? What assumptions does it rely on? How does it work internally?

The goal is to understand the underlying principles rather than memorizing definitions.

---

# Perspective 2 — Attacker Mindset

Think like an attacker. Explain: what assumptions can be abused? What inputs are interesting? What trust boundaries exist? What could go wrong? What information would an attacker gather first? How might an attacker chain this with other vulnerabilities?

Focus on reasoning instead of payload memorization.

---

# Perspective 3 — Defender Mindset

Think like a security engineer. Explain: how can this be detected? How can it be prevented? What security controls are effective? What common defenses fail? What monitoring should exist?

---

# Perspective 4 — Backend Engineer Mindset

Think like the engineer implementing the feature. Explain: how should this be designed? Which mistakes commonly introduce the vulnerability? What secure coding practices should be followed? How should validation, authentication, authorization, and business logic be implemented?

---

# Perspective 5 — System Design & Architecture

Think like a system designer. Explain: which architectural decisions reduce risk? Which design patterns improve security? How does this affect distributed systems, APIs, scalability? How do cloud environments influence the problem?

---

# Perspective 6 — Code Review Mindset

Think like a security reviewer. Explain: what code smells indicate this issue? Which functions deserve extra attention? Which inputs require validation? Which logs should be reviewed? Which tests should exist?

---

# Perspective 7 — Bug Bounty Mindset

Think like a professional bug bounty hunter. Explain: where would you look first? Which endpoints deserve testing? Which business logic should be questioned? Which combinations of vulnerabilities are common? Which recon techniques help discover this issue?

Focus on methodology rather than shortcuts.

---

# Perspective 8 — Interview Mindset

Assume this appears in an interview. Prepare answers to: what is it? why does it happen? how is it exploited? how is it mitigated? what trade-offs exist? what real-world examples demonstrate it?

Answers should be concise, technically correct, and well-structured.

---

# Perspective 9 — Common Mistakes

Identify beginner mistakes, developer mistakes, security testing mistakes, interview mistakes. Explain why they occur and how to avoid them.

---

# Perspective 10 — Key Takeaways

Summarize core concepts, practical lessons, engineering lessons, security lessons, important warnings.

The goal is to ensure every topic is understood from multiple professional viewpoints rather than a single offensive-security perspective — at whatever depth (full or abbreviated) is appropriate for that topic's tier.