# Track 03 — Content & Endpoint Discovery

Purpose: once you know what hosts exist (Track 02), find what's actually running on them.

### Content Discovery with ffuf 🔑
**Purpose:** finds hidden endpoints, backup files, and admin panels that aren't linked anywhere.
**Prerequisites:** Track 02 (need targets to point it at)
**Core concept:** wordlist quality matters more than tool speed; recursive vs. single-level discovery; filtering noise (size/status-code based).
**Primary resource:** ffuf official docs/GitHub
**Secondary resources:** SecLists (wordlist repository) — spend real time understanding which list fits which situation
**Practice:** run ffuf against a permitted target with 2 different wordlists, compare noise levels
**Real-world example:** n/a
**Cross-links:** offensive: API Endpoint Discovery below | bounty: feeds Track 05 directly
**Expected outcome:** can tune ffuf filters to cut noise on a real target without missing genuine hits
**Notes:** wordlist and tool version details will age — check SecLists repo activity periodically
**Status:** not-started | difficulty: 3 | last-reviewed: | tags: [ffuf, content-discovery]

### JavaScript Recon
- Purpose: JS bundles frequently leak API endpoints, internal hostnames, and sometimes secrets/keys
- Primary resource: tools like `subjs`/`getJS` (ProjectDiscovery ecosystem) + manual review
- Practice: pull JS from a permitted target and manually grep for endpoint-looking strings and key-looking strings
- Status: not-started

### Historical URL Discovery (Wayback/gau)
- Purpose: finds old, possibly-still-live endpoints that current crawling misses
- Primary resource: `gau` (get all urls) docs, web.archive.org
- Practice: pull historical URLs for a permitted target and identify any still-responsive endpoints
- Status: not-started

### API Endpoint Discovery
- Purpose: bridges into Curriculum 1 Track 07 (API testing) — this is the discovery half, that's the exploitation-mechanics half
- Primary resource: search for exposed OpenAPI/Swagger docs; Postman public workspace search
- Practice: find and map one publicly documented API schema for a permitted target
- Status: not-started
