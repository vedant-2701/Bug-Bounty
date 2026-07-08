# Claude Project — Setup & Usage Guide

This is an operating manual for *you*, not for Claude. It doesn't explain any security concept — it explains how to run this Claude Project so it stays useful for years without you having to re-read or re-litigate its structure every few weeks.

A quick note on capacity before anything else: Claude Projects don't enforce a practical file-count limit — you can upload as many knowledge files as you want, each up to 30MB, and once the total content exceeds the active context window, Claude automatically switches to retrieval (pulling in only what's relevant to a given conversation) rather than rejecting uploads. Every file in this project is a small markdown file, so you will not hit real capacity problems even as curricula grow to hundreds of topics — organization is the constraint here, not storage. (Specifics can change — check support.claude.com if this ever matters for a decision.)

---

## 1. Initial Project Setup

### Folder organization

Upload the project maintaining this structure (Claude Projects don't support folder upload directly, so recreate the structure by naming files consistently, e.g. `curricula-01-web-security-00-index.md`, or upload via the desktop app which preserves relative paths more gracefully):

```
instructions.md
workflows/  (learning, topic, lab, bug_bounty, secure_engineering)
frameworks/ (thinking, assessment, obsidian_notes)
prompts/    (start_topic, deep_understanding, post_lab_review, notes_generation, daily_security_update, incident_analysis)
resources/  (resources, social_media)
meta/       (changelog)
curricula/  (01-web-security, 02-bug-bounty, 03-secure-engineering — each with 00-index.md + tracks/)
```

### Upload order

1. `instructions.md` first — it's the single source of truth for how every other file gets used. Everything else makes sense in light of it.
2. `frameworks/` next — `thinking_framework.md`, `assessment_framework.md`, `obsidian_notes.md`. These shape *how* every future conversation behaves.
3. `workflows/` — the five workflow files.
4. `prompts/` — the six trigger templates.
5. `resources/` and `meta/changelog.md`.
6. `curricula/` — start with Curriculum 1's `00-index.md` and its `00-prerequisites.md` track. You do not need to upload every track of every curriculum on day one. Add tracks as you approach them — see "Updating the Project" below.

### Which files rarely change

`instructions.md`, the five `workflows/` files, and the three `frameworks/` files are the stable core. Once tuned to how you actually like to learn, expect these to be edited a few times a year at most, mostly in response to something genuinely not working in practice, not on a schedule.

### Which files are expected to evolve

Every file in `curricula/` — topic status fields, next-review dates, notes, and periodically new topics/tracks as PortSwigger, the bounty tooling ecosystem, or OWASP/NIST guidance changes. `meta/changelog.md` grows by definition. `resources/resources.md` and `social_media.md` get occasional additions.

### Which files are only templates

Everything in `prompts/` is a template you copy, fill in the bracketed fields, and send — it is never itself "content" and never needs updating for curriculum reasons, only if the underlying workflow it triggers changes.

### Which files are reference documents

`resources/resources.md`, `resources/social_media.md`, and `meta/changelog.md` are things you consult, not things that drive behavior directly.

---

## 2. Daily Workflow

A typical session touches several files without you needing to think about which one — that's the point of having built it this way. Here's what actually happens, end to end, for one topic:

1. You send `start_topic.md` filled in (or a natural message naming the topic) → Claude reads the topic's entry in `curricula/.../tracks/*.md`, runs `topic_workflow.md`.
2. You study the primary resource, ask questions → Claude uses `thinking_framework.md` (full or abbreviated depth depending on whether the topic is 🔑).
3. You solve labs / test a target / do a design exercise → Claude follows `lab_workflow.md`, `bug_bounty_workflow.md`, or `secure_engineering_workflow.md` depending on which curriculum the topic belongs to.
4. You finish practice → send `post_lab_review.md` → Claude runs `assessment_framework.md`, gives you a confidence score and a next-review date.
5. You send `notes_generation.md` → Claude produces a note per `obsidian_notes.md` (frontmatter included) and updates the topic's status in its track file and the curriculum's `00-index.md`.

You don't have to name any of these files in your message — that mapping already lives in `instructions.md`. Just say what you're doing ("starting SQL injection," "done with the labs," "let's do notes") and the right file activates.

---

## 3. Starting a New Chat

### What to provide

* Which topic and which curriculum, if it's not obvious from context.
* Your current status on it, if you've already started elsewhere (e.g., "I did the theory already, want to go deep now").
* Anything genuinely new since the project knowledge was last updated — e.g., "I already tried X and it didn't work."

### What's already inferred — don't repeat it

* Your overall goals, teaching-style preferences, and the framework/workflow mapping — all in `instructions.md`.
* The topic's prerequisites, primary resource, and expected outcome — already in its `curricula/` entry.
* How labs should be hinted, how assessment should run, how notes should look — all in the relevant workflow/framework file.

If you find yourself re-explaining "don't spoil the answer" or "use the thinking framework," that's a sign the project files aren't being trusted to do their job — just reference the topic and let the files carry the rest.

### Template vs. natural message

Use a **prompt template** when you're deliberately switching modes (starting a topic, requesting notes, requesting a post-lab review, requesting a daily update, requesting an incident deep-dive) — the templates exist precisely so you don't have to remember what each mode needs.

A **natural message** is fine, and often better, for everything else: follow-up questions, "wait, why does that work," "give me another example," "I'm confused about X." Don't force a template onto a conversational question.

### Examples

> "Starting Access Control from Curriculum 1, Track 04. Haven't touched it before."

> "Finished the SSRF labs. Ready for post_lab_review."

> "Quick question — why does SameSite=Lax not fully stop CSRF?"

> Filled `daily_security_update.md`, sent as-is.

---

## 4. Learning Sessions

| Session type | Primary files in play |
|---|---|
| Theory | `topic_workflow.md` (prep), the topic's own Primary Resource field, `thinking_framework.md` for depth |
| Lab (Curriculum 1) | `lab_workflow.md` |
| Bug bounty practice (Curriculum 2) | `bug_bounty_workflow.md` |
| Secure engineering practice (Curriculum 3) | `secure_engineering_workflow.md` |
| Revision | `assessment_framework.md`, driven by which topics have a passed `next-review` date |
| Interview prep | `assessment_framework.md`'s model-answer format (Interview Answer / Technical Answer / Thinking Process) |

For revision sessions specifically: rather than picking a topic yourself, ask Claude to check which topics in `curricula/` have a `next-review` date that's passed and work through those first — that's the whole point of the confidence-scoring mechanism in `assessment_framework.md`.

---

## 5. Long Conversations

Claude conversations do have a practical ceiling — very long threads eventually push older messages out of active context.

**Continue in the same chat when:** you're mid-topic, mid-lab, or mid-assessment — switching chats mid-flow loses the specific reasoning trail you're in.

**Start a fresh chat when:** you're starting a genuinely new topic, or the current chat has accumulated many completed topics and is getting unwieldy. There's no fixed message count to watch for — if Claude starts asking you to re-explain something you covered earlier in the same conversation, that's the signal.

**Preserving continuity:**
* The project knowledge (curricula status, next-review dates, changelog) is what actually persists across chats — not conversation memory. Trust it, don't re-explain what's already reflected there.
* If you want Claude to be able to reference earlier conversations directly, check Settings for a "search past chats" toggle — this is separate from project knowledge and worth enabling for a project you'll run for years.
* When you do start fresh mid-topic, a one-paragraph session summary ("Working through JWT attacks, finished the alg-confusion labs, still need the jku/kid header labs") does more good than any template — write it once, not per message.

---

## 6. Updating the Project

| File type | Update trigger | Recommended review interval |
|---|---|---|
| `curricula/` track files | New PortSwigger topic, new tool, new technique discovered | Quarterly audit (see `learning_workflow.md`) |
| `curricula/` `00-index.md` files | New topic added or dependency map changes | Same quarterly audit |
| `workflows/*.md` | A workflow genuinely doesn't fit how you actually work | As needed — don't edit on a schedule, edit when something breaks in practice |
| `frameworks/*.md` | Standards evolve (new OWASP ASVS version, new NIST guidance) or the tiering/scoring rules need adjusting | Annually, or when a new major standard version ships |
| `prompts/*.md` | Only if the workflow it triggers changed | As needed, tied to workflow changes |
| `resources.md` / `social_media.md` | New resource worth adding, old one gone stale | Every few months, low effort |
| `meta/changelog.md` | Any structural change to the above | Every time you make one — this is the whole point of the file |

---

## 7. Using Prompt Templates

| Template | Use when | Unnecessary when |
|---|---|---|
| `start_topic.md` | Beginning a new topic from any curriculum | You're just asking a follow-up question about a topic already in progress |
| `deep_understanding.md` | Theory is done and you want the full multi-perspective treatment | The topic is a lightweight (non-🔑) entry and a normal question-and-answer exchange already got you there |
| `post_lab_review.md` | Labs/practice for a topic are complete | You're mid-lab and just want a hint (that's `lab_workflow.md` territory, no template needed) |
| `notes_generation.md` | A topic is fully done and ready to be archived as a note | You're not actually done yet — generating notes early means redoing them later |
| `daily_security_update.md` | Your daily/routine check-in on current security news | You already saw the news elsewhere and just want to discuss one specific item — that's a natural message |
| `incident_analysis.md` | A specific CVE/breach/research paper deserves a full deep-dive | A passing mention in a daily update is enough — not every incident needs the full 13-section treatment |

---

## 8. Best Practices

* Don't repeat context that's already in the project — if it's in `instructions.md` or the topic's entry, trust it.
* Don't ask Claude to regenerate a workflow or framework file from scratch when what you actually need is a small edit — ask for the specific edit instead; wholesale regeneration risks losing details you tuned over time.
* Prefer improving an existing file over creating a new one. A new file should only appear when a genuinely new *responsibility* emerges (like `secure_engineering_workflow.md` did) — not as a place to dump one-off notes.
* Keep terminology consistent across curricula — if Curriculum 1 calls something "Access Control," don't let Curriculum 3 drift to calling the same concept something else.
* Use `meta/changelog.md` for anything structural — new tracks, retired files, changed schemas. Routine status updates don't need a changelog entry, only things that would confuse future-you if undocumented.

---

## 9. Common Mistakes

| Mistake | Why it hurts | Fix |
|---|---|---|
| Re-explaining your goals/preferences every chat | Wastes your effort; `instructions.md` already has it | Trust the project knowledge, reference it by name if needed |
| Treating every topic with the full 🔑 template/10-perspective treatment | Doesn't scale to hundreds of topics over years | Respect the flagship/lightweight tiering already built in |
| Skipping the `next-review` mechanism | Knowledge decays silently with nothing prompting revision | Actually ask "what's due for review" periodically |
| Letting `curricula/` status fields go stale | The dependency map becomes untrustworthy | Update status as part of `notes_generation.md`, not as an afterthought |
| Editing a workflow file with a full rewrite for a small tweak | Loses nuance tuned over months | Ask for the specific edit, not a regeneration |
| Forcing Curriculum 2/3 topics through Curriculum 1's Burp/lab completion criteria | Category error — this was fixed in the workflow rewrite, but watch for it creeping back in conversation | Remember each curriculum's completion criteria differs (`topic_workflow.md` Stage 8) |
| Never touching `meta/changelog.md` | 2 years from now, no record of why the structure is what it is | Log structural changes when they happen, not retroactively |

---

## 10. Example Month

**Week 1 — Start SQL Injection (Curriculum 1, Track 02)**
Send `start_topic.md`. Claude runs `topic_workflow.md`: overview, prerequisites check, learning objectives. Study the PortSwigger path alongside Claude filling gaps per `thinking_framework.md`.

**Week 2 — Labs**
Work through PortSwigger's SQLi labs under `lab_workflow.md`'s hint-progression rules. Also start Command Injection theory in parallel if the pace allows — its entry links back to SQLi's mental model.

**Week 3 — Assessment**
Send `post_lab_review.md`. Claude runs `assessment_framework.md`: conceptual/reasoning/completeness/communication evaluation, model answer at all three depths, confidence score, next-review date set.

**Week 4 — Notes + Revision + Related CVEs**
Send `notes_generation.md` → note generated per `obsidian_notes.md`, curriculum status updated. Check for any topics with a passed `next-review` date from prior months and revisit briefly. Send `incident_analysis.md` for a well-documented SQLi-driven breach as a real-world capstone on the month.

Throughout: `resources.md` and `social_media.md` inform what you read outside the chat; `daily_security_update.md` runs independently of the topic-of-the-month, a few minutes a day.

---

## 11. Long-Term Maintenance

This project is built to survive multiple years of drift in its subject matter without needing a structural rebuild — that was the point of last session's redesign. Concretely:

* **New PortSwigger topics** → quarterly audit compares `curricula/01-web-security/00-index.md` against PortSwigger's live topic list; add a new track entry, don't restructure existing tracks.
* **New bug bounty methodologies** → Curriculum 2's Track 05 (Manual Testing & Chaining) and Track 08 (Continuous Practice) absorb new methodology without touching the volatile Track 04 (Automation).
* **New tools** → isolated to Curriculum 2 Track 04, which is explicitly flagged as high-churn — expect to rewrite tool-specific content there every 6–12 months; this doesn't touch anything else.
* **New OWASP guidance** → Curriculum 3 tracks reference OWASP ASVS/Cheat Sheets by name in their Primary Resource fields; when a new ASVS version ships, update those references, not the track structure.
* **AI-assisted security workflows evolving** → PortSwigger's own "Web LLM attacks" content (Curriculum 1 Track 07) and this project's own use of Claude are both already inside the system; if a genuinely new category emerges (not just a new tool), it likely deserves a new track entry, following the same pattern as `secure_engineering_workflow.md` did when Curriculum 3 needed one.

The single habit that keeps all of this maintainable: **log structural changes in `meta/changelog.md` when they happen.** Everything else in this guide assumes that habit is kept.