# Track 01 — Environment & Tooling Foundations

Purpose: the general-purpose skills every later track depends on. Not bounty-specific by itself, but nothing in bounty hunting works without it.

### Bash for Security Automation 🔑
**Purpose:** most recon/automation pipelines are glued together with Bash, even when the core tools are Go binaries.
**Prerequisites:** basic Linux/CLI (Curriculum 1 Track 00)
**Core concept:** pipes, xargs, process substitution, basic scripting patterns for chaining CLI security tools.
**Primary resource:** any solid modern Bash scripting guide — pick one, don't overthink it
**Secondary resources:** study real public recon scripts on GitHub (search "bug bounty recon script")
**Practice:** write a script that chains 2+ tools' output together (even before learning those tools in depth — use dummy commands first)
**Real-world example:** n/a
**Cross-links:** offensive: Track 04 (automation pipelines) | defensive: n/a | bounty: this track underlies all of Curriculum 2
**Expected outcome:** comfortable piping/xargs-ing output between arbitrary CLI tools without looking up syntax every time
**Notes:**
**Status:** not-started | difficulty: 3 | last-reviewed: | tags: [bash, tooling]

### Python for Security Tooling 🔑
**Purpose:** needed once you outgrow shell one-liners — custom scanners, API interaction scripts, data processing.
**Prerequisites:** Bash basics
**Core concept:** requests library, basic concurrency (threading/asyncio) for scanning, JSON parsing.
**Primary resource:** "Automate the Boring Stuff with Python" for fundamentals if needed, then move straight to writing real recon helper scripts
**Secondary resources:** requests and httpx (python) library docs
**Practice:** write a script that takes a list of URLs and checks response codes/titles
**Real-world example:** n/a
**Cross-links:** offensive: Track 04
**Expected outcome:** can write a working Python script to automate a repetitive manual testing step without external help
**Notes:**
**Status:** not-started | difficulty: 3 | last-reviewed: | tags: [python, tooling]

### Burp Suite Extensions for Bounty Work
- Purpose: goes beyond Curriculum 1's core-tool usage into bounty-specific extensions
- Primary resource: BApp Store — look at Autorize, Turbo Intruder, Param Miner
- Practice: install and use one extension end-to-end on a permitted target
- Status: not-started

### VPS / Cloud Environment Setup for Scanning
- Purpose: local scanning gets rate-limited/IP-banned fast; a cheap VPS is standard practice
- Primary resource: any provider's basic setup docs (this is infra, not security-specific)
- Practice: stand up a VPS, install your core toolchain, confirm you can run a scan from it
- Status: not-started
