# Web Security & Bug Bounty Learning Resources

> **Purpose:** A curated list of high-quality resources for learning web security, bug bounty hunting, secure engineering, and staying up to date.
>
> **Learning Philosophy:**
>
> * Master one primary resource before jumping to others.
> * Use secondary resources to reinforce understanding.
> * Learn concepts first, tools second, automation third.
> * Practice continuously.
>
> This list is now organized to support all three curricula in `/curricula/` — sections 1–2, 4, 7 are mainly Curriculum 1; section 3 is mainly Curriculum 2; section 10 (expanded below) is mainly Curriculum 3.

---

# 1. Primary Learning Resource (Highest Priority)

## PortSwigger Web Security Academy

Website: https://portswigger.net/web-security
Learning Paths: https://portswigger.net/web-security/learning-paths
All Topics: https://portswigger.net/web-security/all-topics

Why: structured curriculum, excellent explanations, hands-on labs, Burp Suite integration, covers offensive and defensive concepts.

Recommendation: follow the Learning Paths in order (as re-sequenced in `curricula/01-web-security/`); use All Topics only as a reference.

Priority: ⭐⭐⭐⭐⭐

---

# 2. Web Security Reference

## OWASP

Website: https://owasp.org

Useful resources: OWASP Top 10, Web Security Testing Guide (WSTG), Cheat Sheet Series, ASVS (Application Security Verification Standard).

Purpose: defensive understanding, best practices, industry standards.

Priority: ⭐⭐⭐⭐⭐

---

# 3. Bug Bounty & Offensive Security

## ProjectDiscovery

Website: https://projectdiscovery.io
Documentation: https://docs.projectdiscovery.io
GitHub: https://github.com/projectdiscovery

Purpose: reconnaissance, asset discovery, automation, modern bug bounty tooling.

Priority: ⭐⭐⭐⭐⭐ — note: this is Curriculum 2's highest-churn resource area (see Track 04, Automation Pipelines).

---

# 4. Practical Labs

## PortSwigger Labs
https://portswigger.net/web-security — primary practice platform. Priority ⭐⭐⭐⭐⭐

## OWASP Juice Shop
https://owasp.org/www-project-juice-shop/ — intentionally vulnerable app practice. Priority ⭐⭐⭐⭐⭐

## DVWA
https://github.com/digininja/DVWA — classic vulnerable application. Priority ⭐⭐⭐⭐

## Hack The Box Academy
https://academy.hackthebox.com — guided learning and practical labs. Priority ⭐⭐⭐⭐

## TryHackMe
https://tryhackme.com — beginner-friendly guided rooms. Priority ⭐⭐⭐⭐

## PicoCTF
https://picoctf.org — CTF-style web challenges. Priority ⭐⭐⭐

---

# 5. Bug Bounty Platforms

## HackerOne
https://www.hackerone.com

## Bugcrowd
https://www.bugcrowd.com

## Intigriti
https://www.intigriti.com

Purpose: real-world bug bounty programs after building a solid foundation. Priority ⭐⭐⭐⭐⭐ (later stage)

---

# 6. Research & Writeups

* PortSwigger Research — https://portswigger.net/research (new attack techniques, browser research, HTTP protocol research)
* HackerOne Hacktivity — https://hackerone.com/hacktivity (publicly disclosed reports)
* Bugcrowd Blog — https://www.bugcrowd.com/blog/
* Intigriti Blog — https://www.intigriti.com/researchers/blog
* ProjectDiscovery Blog — https://projectdiscovery.io/blog
* Detectify Labs — https://labs.detectify.com

---

# 7. Documentation

## Mozilla Developer Network (MDN)
https://developer.mozilla.org — HTTP, cookies, browser APIs, JavaScript, web standards. Priority ⭐⭐⭐⭐⭐

## RFC Editor
https://www.rfc-editor.org — protocol specifications (HTTP, TLS, DNS, etc.), for deep protocol understanding.

---

# 8. Tool Documentation

Burp Suite, Nuclei, ffuf, httpx, Subfinder, Amass, Katana — always prefer official documentation before third-party tutorials.

---

# 9. GitHub Resources

* ProjectDiscovery — https://github.com/projectdiscovery
* TomNomNom — https://github.com/tomnomnom
* OWASP — https://github.com/OWASP
* PortSwigger — https://github.com/PortSwigger

---

# 10. Secure Engineering References (Curriculum 3)

## Standards & Frameworks

* OWASP ASVS (Application Security Verification Standard) — the verification-standard companion to the Top 10; primary reference for Curriculum 3 Track 00 and Track 09
* OWASP Cheat Sheet Series — input validation, session management, authorization, cryptographic storage, logging — referenced throughout Curriculum 3
* NIST SP 800-207 — Zero Trust Architecture (Curriculum 3 Track 01)
* NIST SP 800-218 — Secure Software Development Framework, SSDF (Curriculum 3 Track 07)
* NIST SP 800-61 — Computer Security Incident Handling Guide (Curriculum 3 Track 06)
* NIST SP 800-57 — Key Management (Curriculum 3 Track 04)
* SLSA framework (supply-chain security levels) — https://slsa.dev (Curriculum 3 Track 07)
* Sigstore — artifact signing — https://www.sigstore.dev (Curriculum 3 Track 07)
* Adam Shostack, *Threat Modeling: Designing for Security* — the standard reference for Curriculum 3 Track 01

## Engineering Blogs

* Google Security Blog
* Cloudflare Blog

These help understand mitigation and secure system design at a level PortSwigger and OWASP's own docs don't fully reach.

---

# Learning Order

1. PortSwigger Web Security Academy
2. PortSwigger Labs
3. OWASP references
4. ProjectDiscovery tools & documentation
5. Practical labs (Juice Shop, DVWA, HTB Academy, TryHackMe)
6. Public writeups
7. Real bug bounty programs
8. Secure engineering standards (ASVS, NIST SSDF) — ongoing, in parallel with 3–7 once Curriculum 3 begins

---

# General Rules

* Finish the primary resource for a topic before searching for external explanations.
* Read writeups only after attempting the challenge yourself.
* Prefer official documentation over random blogs.
* Practice every concept immediately.
* Focus on understanding why an attack works and how to mitigate it, not just how to reproduce it.