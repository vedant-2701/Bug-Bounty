# Curricula — Project Content Layer

## What this folder is

This folder is the **content layer** of the Web Security / Bug Bounty / Secure Engineering project. It contains the three curricula. It does not contain process — how to study, how to run labs, how to assess understanding, how to take notes. That logic lives in `/workflows/` and `/frameworks/` and is not duplicated here.

`instructions.md` is the operating manual. This README assumes you've read it.

## The three curricula

| Curriculum | Folder | Backbone | Update cadence |
|---|---|---|---|
| 1. Web Security | `01-web-security/` | PortSwigger Web Security Academy | Slow — audit quarterly against PortSwigger's live topic list |
| 2. Bug Bounty | `02-bug-bounty/` | Real-world methodology + tooling | Fast — the automation track (04) will need edits every 6–12 months |
| 3. Secure Engineering | `03-secure-engineering/` | Backend/architecture standards (OWASP ASVS, NIST SSDF) | Medium — tracks standards bodies, not tool churn |

Each curriculum folder contains:
- `00-index.md` — the MOC (map of content): dependency graph, track list, completion tracking. This is the merged descendant of the old `track.md` — scoped per curriculum instead of one global file.
- `tracks/` — one file per track, containing topic entries in dependency order.

## Concept ownership rule

The same concept (JWT, SSRF, IDOR, API security, business logic) legitimately appears in more than one curriculum, viewed through a different lens. To avoid three curricula independently drifting on "what is SSRF":

**Every concept has exactly one canonical deep-dive**, almost always in Curriculum 1 (mechanics). Entries in Curriculum 2 and 3 covering the same concept stay short and state only what's different about their lens (recon angle / defensive design), with a link back to the canonical entry.

## Topic entry schema

Two tiers — this is deliberate. A full schema on every topic collapses under its own weight over a multi-year project.

**Full template** (flagship / foundational topics — marked 🔑):
```
### Topic Name  🔑
**Purpose:** why this matters, one line
**Prerequisites:** linked topics
**Core concept:** canonical explanation (only if this curriculum owns the concept)
**Primary resource:** link
**Secondary resources:** links
**Practice:** lab / target / exercise
**Real-world example:** CVE or disclosed report
**Cross-links:** offensive: … | defensive: … | bounty: …
**Expected outcome:** a can-do statement, not a knows-about statement
**Notes:** living field
**Status:** not-started | difficulty: | last-reviewed: | tags: []
```

**Lightweight template** (everything else):
```
### Topic Name
- Purpose: …
- Primary resource: …
- Practice: …
- Status: not-started
```

Promote a lightweight entry to full if it turns out to be high-connectivity (many other topics link to it) or you're spending real time on it.

## Frontmatter (applies once these become individual Obsidian notes)

If/when a topic entry is promoted to its own atomic note (recommended once a flagship topic has enough of its own sub-links), give it:

```yaml
---
title:
curriculum: web-security | bug-bounty | secure-engineering
track:
status: not-started | in-progress | done | needs-review
difficulty: 1-5
last-reviewed:
offensive_counterpart:
defensive_counterpart:
bounty_application:
tags: []
---
```

This is what makes the vault queryable (Dataview) rather than just linkable.

## Maintenance rituals

- **Quarterly**: diff each curriculum's Track list against PortSwigger's current topic list / current bounty tooling landscape / current OWASP guidance. Log changes in `/meta/changelog.md`.
- **Never delete a stale tool/technique note** — archive it (move to an `archive/` subfolder within the relevant track) so learning history is preserved.
