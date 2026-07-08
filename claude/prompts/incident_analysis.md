# incident_analysis_prompt.md

## Purpose

Use this prompt whenever studying a real-world vulnerability, CVE, exploit chain, supply chain attack, browser vulnerability, cloud security incident, ransomware campaign, or security research.

---

I want to study the following real-world security topic:

Topic: [Name]

Do not provide only a summary. Use `thinking_framework.md` throughout, at full depth — incident analysis always warrants the full treatment regardless of the topic's tier elsewhere.

Cover the topic in this order:

## 1. Overview
What is it? Why is it important? Why should security engineers and backend engineers understand it?

## 2. Historical Context
When it happened, who discovered it, who was affected, why it became significant, what made it different from previous attacks.

## 3. Technical Background
The technology involved, before the attack.

## 4. Root Cause
The fundamental design or implementation mistake — not just the exploit description.

## 5. Attack Flow
Initial assumptions, entry point, exploitation steps, privilege gained, final impact.

## 6. Attacker Thinking
Using `thinking_framework.md`: how an attacker would approach this, what clues they'd look for, why it worked, which assumptions were exploited.

## 7. Defender Thinking
Detection, prevention, monitoring, logging, security controls, defense in depth.

## 8. Backend Engineering Perspective
Which coding mistakes enabled the issue, how it should have been implemented, secure engineering practices, design improvements.

## 9. System Design Perspective
Architectural implications, trust boundaries, security trade-offs, scaling considerations, cloud implications.

## 10. Mitigation
Immediate mitigation, long-term mitigation, secure coding practices, operational controls, monitoring strategies.

## 11. Related Concepts
Identify similar vulnerabilities and name the **specific track and topic** in each relevant curriculum this connects to — e.g. "Curriculum 1 Track 04 (SSRF)" and "Curriculum 3 Track 08 (Cloud IAM Design)" rather than a vague pointer.

## 12. Interview Perspective
How to answer questions about this topic in an interview.

## 13. Key Lessons
Engineering, security, and architectural lessons to remember.

The goal is to understand not only what happened, but why, how it could have been prevented, and how to recognize similar issues in the future.