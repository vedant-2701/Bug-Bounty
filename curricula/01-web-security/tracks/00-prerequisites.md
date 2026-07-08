# Track 00 — Prerequisites

Purpose: the floor PortSwigger assumes you're already standing on. Do not start Track 01 until this track is solid — most "I'm lost" moments in early PortSwigger labs trace back to a gap here, not to the vulnerability itself.

### HTTP Fundamentals 🔑
**Purpose:** Every other track depends on fluently reading a raw request/response.
**Prerequisites:** none
**Core concept:** methods, status codes, headers, statelessness, request/response cycle.
**Primary resource:** MDN HTTP docs (https://developer.mozilla.org/en-US/docs/Web/HTTP)
**Secondary resources:** RFC 9110 (HTTP semantics) for anything MDN leaves ambiguous
**Practice:** intercept and read 20+ real requests in Burp before touching any lab
**Real-world example:** n/a — foundational
**Cross-links:** offensive: everything in Track 01+ | defensive: Curriculum 3 Track 00 | bounty: Curriculum 2 Track 02
**Expected outcome:** can read a raw HTTP request/response and explain every header without looking it up
**Notes:**
**Status:** not-started | difficulty: 2 | last-reviewed: | tags: [http, foundations]

### Cookies & Sessions
- Purpose: needed before Track 05 (Auth) makes any sense
- Primary resource: MDN Cookies docs
- Practice: inspect Set-Cookie/Cookie headers on a real site in Burp
- Status: not-started

### Burp Suite Setup & Core Tools 🔑
**Purpose:** Burp is the lens for every lab in this curriculum.
**Prerequisites:** HTTP Fundamentals
**Core concept:** Proxy, Repeater, Intruder, Decoder — what each is *for*, not just how to click it.
**Primary resource:** PortSwigger's official Burp tutorial videos (linked from Getting Started)
**Secondary resources:** Burp Suite official docs
**Practice:** intercept a request, modify it in Repeater, resend it, observe the diff
**Real-world example:** n/a
**Cross-links:** offensive: all labs | defensive: n/a | bounty: Curriculum 2 Track 01
**Expected outcome:** comfortable moving a request between Proxy → Repeater → Intruder without hesitation
**Notes:**
**Status:** not-started | difficulty: 2 | last-reviewed: | tags: [burp, tooling]

### Basic Linux / CLI
- Purpose: needed before any bug bounty tooling (Curriculum 2) and useful for local test setups
- Primary resource: any modern "Linux basics" guide — pick one, don't overthink it
- Practice: comfortable with cd/grep/curl/cat/pipes
- Status: not-started

### Basic JavaScript & Browser DevTools
- Purpose: needed for DOM-based XSS, prototype pollution, client-side tracks
- Primary resource: MDN JavaScript guide (just enough — variables, functions, DOM, fetch)
- Practice: open DevTools on a real site, set a breakpoint, inspect the console
- Status: not-started
