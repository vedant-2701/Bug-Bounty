Curriculum 1 — reorganize by dependency, not by PortSwigger's own path order:

Track 0: Prerequisites (HTTP internals, cookies/sessions, Burp setup, basic Linux/CLI, basic JS)
Track 1: Core web mechanics (same-origin policy, HTTP semantics)
Track 2: Injection (SQLi, command injection, SSTI, NoSQLi)
Track 3: Client-side (XSS, CSRF, clickjacking, CORS, DOM-based, prototype pollution)
Track 4: Access & server logic (access control, business logic, SSRF, race conditions)
Track 5: Auth & session (authentication, OAuth, JWT)
Track 6: Advanced HTTP (request smuggling, host header attacks, cache poisoning/deception)
Track 7: APIs (GraphQL, API testing, Web LLM attacks)
Track 8: Serialization & file handling (deserialization, file upload, path traversal)
Track 9: Supplementary depth (crypto basics, HTTP/2-3, browser isolation, CSP authoring)
Track 10: Capstone (chained labs, mystery-lab challenges, Burp Practitioner-style exercises)

Rationale for ordering: access control and auth depend on understanding client-side/CORS basics; business logic labs assume you can already do basic exploitation; advanced HTTP topics assume core HTTP fluency. This isn't PortSwigger's own path order, but it's the order that minimizes "wait, I don't know what X means yet" moments.

---

Curriculum 2 — organize around the bounty workflow lifecycle, not a tool list, because tools rotate every few months but methodology doesn't:

Track 0: Program mechanics, scope, legal, platform norms
Track 1: Environment & tooling foundations (Bash, Python, Burp extensions)
Track 2: Recon & asset discovery (subdomains, ASN, cloud, OSINT/GitHub)
Track 3: Content & endpoint discovery (JS recon, wayback/gau, API discovery)
Track 4: Automation pipelines (ffuf, httpx, katana, nuclei — isolate these as the "expect to rewrite this section every 6–12 months" zone)
Track 5: Manual testing & chaining (applying C1 knowledge live)
Track 6: Specialized testing (API/GraphQL, business logic in the wild)
Track 7: Reporting & professionalism (CVSS, PoC craft, triager relations)
Track 8: Continuous practice (monitoring targets, staying current, community)

This isolates volatility: Track 4 will need constant edits as ProjectDiscovery ships new tools; Tracks 0, 2, 5, 7 will barely change in 3 years.

---

Curriculum 3 — organize by SDLC phase / architecture layer, mirroring how a backend engineer actually thinks:

Track 0: Foundations for engineers (shared vocabulary with C1 — explicitly link back rather than re-explain)
Track 1: Secure design (STRIDE/DREAD/PASTA, defense in depth, zero trust)
Track 2: AuthN/AuthZ & session design (building, not exploiting)
Track 3: Secure coding & input validation
Track 4: Secrets & data protection (key management, encryption at rest/in transit)
Track 5: API & microservices security (gateways, rate limiting, mTLS)
Track 6: Logging, monitoring, incident response basics
Track 7: Secure SDLC & DevSecOps (SAST/DAST/SCA, CI/CD, supply chain)
Track 8: Cloud & infrastructure (IAM, containers/K8s, network segmentation)
Track 9: System design integration (security in HLD/LLD docs, breach case studies mapped to design flaws)