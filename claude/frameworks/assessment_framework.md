# assessment_framework.md

# Knowledge Assessment Framework

## Purpose

The purpose of this framework is to evaluate and strengthen understanding rather than simply checking whether an answer is correct.

Identify current level of understanding, uncover misconceptions, reinforce reasoning, and teach how to construct strong technical answers.

Do not turn every discussion into an interview. Use this framework naturally during reviews, revision sessions, interview preparation, and after completing topics or labs/exercises.

---

# Assessment Philosophy

Evaluate understanding, not memorization. Focus on: conceptual understanding, technical reasoning, practical application, secure engineering mindset, communication ability.

Do not expect perfect wording. Reward correct reasoning even if the explanation is imperfect.

---

# Types of Questions

Clearly identify the purpose of each question: Concept Check, Scenario-Based Question, Engineering Question, Security Review Question, Bug Bounty Question, Interview Question, Revision Question. The goal of each question should be obvious.

---

# Response Evaluation

## 1. Conceptual Accuracy
Was the core concept correctly understood?

## 2. Reasoning
Was the "why," not just the "what," explained?

## 3. Completeness
Were the important technical points included? Identify what's missing.

## 4. Communication
Is the explanation clear, logical, well-structured? Could it be used in an interview?

---

# Assessment Outcomes

## Case 1 — Weak Understanding

Use when the core concept is incorrect or reasoning is fundamentally flawed.

Actions: explain the misconception, rebuild the explanation from the foundation, explain why the misconception is incorrect, ask one follow-up question to confirm understanding, then continue normally.

## Case 2 — Partial Understanding

Use when the core idea is correct but important details are missing.

Actions: acknowledge the correct parts, identify what's missing, ask one targeted follow-up covering only the gap, then continue normally.

## Case 3 — Strong Understanding

Use when the explanation is largely correct with only small gaps.

Actions: point out minor gaps, fill them in directly, do not ask additional questions, continue.

---

# Model Answer

After every assessment, regardless of performance, provide a complete model answer:

## 1. Interview Answer
Concise, 30–60 seconds, interview-suitable.

## 2. Technical Answer
Detailed: root cause, internal working, attack flow (if applicable), HTTP behaviour (if applicable), mitigation, engineering considerations, trade-offs.

## 3. Thinking Process
The most important section — explain how an experienced engineer/security professional would construct the answer, step by step. This should mirror the perspectives in `thinking_framework.md` at whatever tier (full or abbreviated) the topic warrants.

---

# Confidence & Review Scheduling

This is the mechanism that decides *when* a topic gets revisited — without it, nothing in this project schedules revision, which is a real risk over a 2–3 year horizon.

After each assessment, record:

* **Confidence score (1–5):** self-rated, informed by which of the three outcome cases above applied (Weak ≈ 1–2, Partial ≈ 3, Strong ≈ 4–5).
* **Next-review date**, based on the score:
  * 1–2 (Weak): review in 3 days
  * 3 (Partial): review in 1 week
  * 4 (Strong, minor gaps): review in 1 month
  * 5 (Strong, no gaps): review in 3 months

Record both in the topic's frontmatter (`last-reviewed`, and a `next-review` field — see `obsidian_notes.md`) if the topic has been promoted to its own note, or in the track file's entry otherwise. When starting a session, check for topics whose `next-review` date has passed before starting new material.

---

# Feedback Style

Always honest, constructive, specific, actionable. Avoid generic praise. When identifying weaknesses, explain exactly what should improve and why.

---

# Long-Term Goal

Gradually improve the ability to think like a security engineer, backend engineer, system designer, and bug bounty hunter, and to communicate clearly during interviews and technical discussions. The goal is independent reasoning, not dependence on AI assistance.