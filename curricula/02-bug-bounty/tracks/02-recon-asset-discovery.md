# Track 02 — Reconnaissance & Asset Discovery

Purpose: the attack surface doesn't exist until you find it. This track is where most professional bounty hunters actually spend a disproportionate share of their time.

### Subdomain Enumeration 🔑
**Purpose:** the classic starting point of recon — most orgs have far more subdomains exposed than they realize.
**Prerequisites:** Bash/Python basics
**Core concept:** passive (cert transparency, DNS aggregators) vs. active (brute-force, permutation) enumeration; why combining multiple sources beats any single tool.
**Primary resource:** ProjectDiscovery `subfinder` docs (https://docs.projectdiscovery.io)
**Secondary resources:** Amass docs (OWASP) as a second data source
**Practice:** run subfinder + amass against a permitted target, diff the results, investigate why they differ
**Real-world example:** any recon-methodology bounty write-up (NahamSec/STÖK content is full of these)
**Cross-links:** offensive: Content Discovery (Track 03) | defensive: Curriculum 3 Track 08 (cloud/infra — this is what asset inventory is meant to prevent surprises about) | bounty: this track feeds everything downstream
**Expected outcome:** can produce a deduplicated, validated subdomain list for a target using at least 2 independent tools/sources
**Notes:** high tool-churn area — check ProjectDiscovery's blog for updates every few months
**Status:** not-started | difficulty: 3 | last-reviewed: | tags: [recon, subdomains]

### ASN & Cloud Recon
- Purpose: finds infrastructure that plain subdomain enum misses (IP ranges, cloud assets not tied to obvious DNS names)
- Primary resource: ProjectDiscovery's `asnmap` docs; also manual ASN lookups via BGP tools
- Practice: identify a target's ASN and map its IP ranges
- Status: not-started

### OSINT: GitHub Dorking & Certificate Transparency
- Purpose: leaked secrets, internal hostnames, and unlisted subdomains often surface here before anywhere else
- Primary resource: GitHub code search syntax docs; crt.sh for certificate transparency
- Practice: find one real (non-sensitive) example of a hostname or config reference in public GitHub code for a permitted target
- Status: not-started

### Shodan & Censys
- Purpose: internet-wide scan data — finds exposed services/infrastructure fast
- Primary resource: Shodan and Censys official docs
- Practice: search a target's known IP range in both tools and compare what each surfaces
- Status: not-started
