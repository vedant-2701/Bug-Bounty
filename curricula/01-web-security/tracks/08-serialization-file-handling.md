# Track 08 — Serialization & File Handling

Purpose: parallel track to injection (Track 02) — can be studied alongside it or after, both feed the same "trust the interpreter, not the input" instinct.

### Insecure Deserialization 🔑
**Purpose:** frequently leads directly to RCE; language-specific (Java, PHP, Python, .NET each have their own gadget-chain ecosystems).
**Prerequisites:** Command Injection (shares the "attacker-controlled code path" mental model)
**Core concept:** what "gadget chains" actually are; why deserializing untrusted data is fundamentally different from parsing untrusted data.
**Primary resource:** PortSwigger Insecure deserialization learning path
**Secondary resources:** ysoserial (Java) and ysoserial.net (.NET) docs — read to understand gadget chains, not as a black box
**Practice:** PortSwigger labs; for at least one lab, manually construct the malicious serialized object instead of using a generator tool
**Real-world example:** search "Java deserialization RCE" for well-documented enterprise incidents
**Cross-links:** offensive: File Upload below (often the delivery mechanism) | defensive: Curriculum 3 Track 03 (secure coding) | bounty: Curriculum 2 Track 05
**Expected outcome:** can explain, language-agnostically, why deserialization of untrusted data is dangerous even without naming a specific gadget chain
**Notes:**
**Status:** not-started | difficulty: 5 | last-reviewed: | tags: [deserialization, rce]

### File Upload Vulnerabilities
- Purpose: common real-world finding; content-type/extension validation bypass patterns
- Primary resource: PortSwigger File upload vulnerabilities learning path
- Practice: PortSwigger labs; identify which validation layer (extension/content-type/content) each lab bypasses
- Status: not-started

### Path Traversal
- Purpose: simple mechanically, still very common in the wild
- Primary resource: PortSwigger Path traversal learning path
- Practice: PortSwigger labs; enumerate the traversal filter-bypass techniques used
- Status: not-started

### XML External Entity (XXE) Injection
- Purpose: parser-trust failure, often chains into SSRF or file disclosure
- Primary resource: PortSwigger XXE topic
- Practice: PortSwigger labs; explain the connection between XXE and SSRF explicitly
- Status: not-started
