# Track 04 — Automation & Scanning Pipelines

⚠️ **Highest-churn track in this entire project.** Tool names, flags, and template formats here will age faster than anything else you're studying. Revisit this track's content every 6–12 months against ProjectDiscovery's current docs rather than trusting what's written here.

### httpx
- Purpose: fast HTTP probing of large host lists — the workhorse between raw domain lists and anything meaningful
- Primary resource: ProjectDiscovery httpx docs
- Practice: probe your subdomain list from Track 02 and extract status codes/titles/tech stack
- Status: not-started

### katana
- Purpose: modern crawler — replaces a lot of what older crawling tools did, with better JS-awareness
- Primary resource: ProjectDiscovery katana docs
- Practice: crawl a permitted target and diff results against your manual content discovery from Track 03
- Status: not-started

### nuclei 🔑
**Purpose:** template-based vulnerability scanner — the closest thing to an industry-standard automation layer in modern bounty work.
**Prerequisites:** httpx, basic understanding of the vuln classes being scanned for (Curriculum 1)
**Core concept:** nuclei finds *known* patterns fast; it does not replace manual testing — treat its output as leads to verify, not findings to report blind.
**Primary resource:** ProjectDiscovery nuclei docs + nuclei-templates GitHub repo
**Secondary resources:** browse the templates repo to understand what a template actually checks — don't run it as a black box
**Practice:** run nuclei against a permitted target, manually verify at least one finding before considering it real
**Real-world example:** n/a
**Cross-links:** offensive: entire Curriculum 1 (nuclei templates encode those vuln classes) | bounty: Track 05
**Expected outcome:** can read a nuclei template YAML and explain what it's actually testing for, not just run it
**Notes:** template repo updates constantly — this is the fastest-moving single resource in the whole project
**Status:** not-started | difficulty: 3 | last-reviewed: | tags: [nuclei, automation, high-churn]

### Building Notification Pipelines
- Purpose: continuous monitoring is only useful if you find out about changes — connect scans to Slack/Discord/Telegram alerts
- Primary resource: `notify` (ProjectDiscovery) docs
- Practice: wire up one tool's output to a notification channel
- Status: not-started

### Continuous / Diffed Monitoring
- Purpose: distinct skill from one-off recon — watching targets over time for new subdomains/endpoints/changes
- Primary resource: search "bug bounty continuous monitoring pipeline" for real-world architecture write-ups
- Practice: set up a basic recurring scan (cron or similar) that diffs today's subdomain list against yesterday's
- Status: not-started
