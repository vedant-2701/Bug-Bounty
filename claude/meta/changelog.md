# changelog.md

Log of structural changes to the project — curricula, workflows, and frameworks. This is where the quarterly audit ritual (see `workflows/learning_workflow.md`) records what changed and why, so 2–3 years from now it's possible to see how the project evolved rather than just its current snapshot.

Add a new entry each time a curriculum track is revised, a tool/technique is archived, or a workflow/framework file changes structurally. Routine topic-status updates (not-started → done) don't need an entry here — only structural changes.

---

## Format

```
## YYYY-MM-DD — Short title

**What changed:**
**Why:**
**Affected files:**
```

---

## 2026-07-08 — Initial architecture established

**What changed:** Replaced the original flat 17-file project with a folder structure (`curricula/`, `workflows/`, `frameworks/`, `prompts/`, `resources/`, `meta/`). Retired `track.md`, merging its content into each curriculum's `00-index.md`. Generalized `topic_workflow.md` and `learning_workflow.md` to branch across all three curricula instead of assuming PortSwigger/Burp Suite by default. Added `secure_engineering_workflow.md` as Curriculum 3's practice-loop equivalent to `lab_workflow.md`/`bug_bounty_workflow.md`. Added YAML frontmatter standard to `obsidian_notes.md` and confidence-score/next-review scheduling to `assessment_framework.md`. Added full-vs-abbreviated tiering to `thinking_framework.md`.

**Why:** the original files assumed every topic was a PortSwigger topic with Burp Suite involved, which breaks for Curriculum 2 (Bug Bounty) and Curriculum 3 (Secure Engineering) topics. Several files also duplicated the same "which file governs what" logic in 3+ places, risking drift over a multi-year project.

**Affected files:** all of them, to varying degrees — see the file-by-file review for detail.