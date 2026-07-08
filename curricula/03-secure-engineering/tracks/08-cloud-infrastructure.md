# Track 08 — Cloud & Infrastructure Security

Purpose: can be studied in parallel with Track 07. This is the design-side counterpart of Curriculum 1's SSRF entry and Curriculum 2's cloud-recon entry — cloud misconfiguration is where a huge share of modern real-world impact actually lives.

### Cloud IAM Design 🔑
**Purpose:** the single highest-leverage cloud security control — most cloud breaches trace back to over-permissioned IAM, not a novel exploit.
**Prerequisites:** Track 00
**Core concept:** least privilege as an operational discipline, not a one-time setup; the difference between identity-based and resource-based policies; why role assumption chains need auditing.
**Primary resource:** your primary cloud provider's IAM best-practices documentation (AWS IAM, GCP IAM, or Azure RBAC — pick the one you actually use)
**Secondary resources:** the Capital One breach post-mortem (SSRF → over-permissioned IAM role → S3 access) — a direct case study connecting this track to Curriculum 1 Track 04
**Practice:** review a real IAM policy (yours or a public example) and identify at least one over-broad permission
**Real-world example:** Capital One 2019 breach — strong `incident_analysis.md` candidate, ties SSRF (offense) directly to IAM design (defense)
**Cross-links:** offensive: Curriculum 1 Track 04 (SSRF), Curriculum 2 Track 02 (cloud recon) | this is the canonical defensive counterpart of both
**Expected outcome:** given an IAM policy, can identify permissions broader than the stated use case requires
**Notes:**
**Status:** not-started | difficulty: 4 | last-reviewed: | tags: [cloud, iam]

### Container & Kubernetes Security
- Purpose: explicit subtopic rather than assumed under "infra security" generally — has its own distinct failure modes (privileged containers, RBAC misconfig, network policy gaps)
- Primary resource: NSA/CISA Kubernetes Hardening Guide
- Practice: review a Kubernetes manifest (yours or a public example) for privileged mode, host network access, and missing resource limits
- Status: not-started

### Network Segmentation
- Purpose: the network-layer implementation of zero trust (Track 01) — reduces blast radius when a single service is compromised
- Primary resource: your cloud provider's VPC/network security documentation
- Practice: diagram a network segmentation approach for a hypothetical multi-tier application
- Status: not-started
