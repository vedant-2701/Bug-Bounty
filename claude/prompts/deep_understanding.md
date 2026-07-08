# deep_understanding_prompt.md

## Purpose

Use this prompt after theory for a topic is complete and deeper understanding is wanted.

---

I have completed the theory for this topic.

Do not repeat the learning material. Deepen understanding instead.

Follow `thinking_framework.md` — at full depth if this is a flagship (🔑) topic in its curriculum entry, at the abbreviated 4-perspective depth otherwise.

For every important concept:

* Explain the intuition before the technical details.
* Explain how it works internally and what assumptions it relies on.
* Explain how attackers abuse those assumptions.
* Explain how defenders prevent the issue.
* Explain how backend engineers should implement it securely.
* Explain architectural considerations and trade-offs.
* Compare it with similar concepts where appropriate — check the topic's "Cross-links" field in `/curricula/` for concepts already flagged in the other two curricula.
* Use realistic production scenarios instead of toy examples.
* Point out common misconceptions and implementation mistakes.

When appropriate: explain the relevant HTTP behaviour, explain how Burp Suite (or the relevant Curriculum 2/3 tool) helps analyse the issue, and recommend additional practical exercises if the primary resource doesn't cover an important aspect.

The goal is intuition, reasoning, and engineering judgement — not memorized facts.