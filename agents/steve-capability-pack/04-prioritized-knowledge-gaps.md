# 04 — Prioritized Knowledge Gaps
Scoring: each factor 1–5. **Priority = Impact + Error-probability +
Detection-difficulty + Frequency + Unapproved-action-consequence** (max 25).

| # | Gap | Imp | Err | Det | Freq | Cons | Total | Remediation |
|---|-----|----|----|----|----|----|------|-------------|
| G1 | Post-cutoff framework/version churn (OWASP Top10:2025 final Jan 2026, ASVS 5.0 May 2025, MASVS 2.1/MASTG 2.0, PCI DSS 4.0.1 future-dated reqs mandatory since 2025-03-31, HITRUST v11.8.0 May 2026, ATT&CK v19 Apr 2026, NIST 800-53 Rel. 5.2.0 Aug 2025, CCPA 2026 amendments) | 5 | 5 | 4 | 5 | 2 | 21 | §05 version tags + verify-before-cite; quarterly refresh §15 |
| G2 | Fabrication risk: claiming a scan/CVE/exploit was verified without an artifact or citation | 5 | 3 | 5 | 4 | 5 | 22 | Evidence rules §06.7; auto-fail §13 |
| G3 | Business-risk-tradeoff mishandling (obstructionism or silent risk acceptance) | 5 | 4 | 4 | 4 | 5 | 22 | Charter §02 authority; §07 D3; gate G3; template T8 |
| G4 | Theoretical-vs-exploitable conflation | 4 | 4 | 4 | 4 | 3 | 19 | §05.1; §07 D1/D5; Karla handoff discipline |
| G5 | Compliance-scope overreach (assuming PCI/HITRUST/GDPR/CCPA applies without evidence) | 4 | 4 | 3 | 4 | 3 | 18 | §05.4–.7 scoping rules; §07 edge case 3 |
| G6 | Five-way sibling-boundary drift (Dave/Karla/Bisi/Derrick/Diego) | 4 | 3 | 3 | 4 | 4 | 18 | Charter §02 owned/shared/out-of-authority tables |
| G7 | Secrets/PII exposure encountered during recon | 5 | 2 | 4 | 3 | 5 | 19 | §08.3 hygiene checklist; incident template T11 |
| G8 | Apple platform security depth (Keychain vs. UserDefaults, ATS scoping, Privacy Manifest, Secure Enclave, Swift 6 concurrency security implications) | 3 | 3 | 3 | 4 | 2 | 15 | §05.10 |
| G9 | AWS/GitHub supply-chain depth (IAM least privilege, SLSA levels, secret scanning/push protection, Actions/OIDC trust) | 4 | 3 | 3 | 4 | 2 | 16 | §05.11–.12; OWASP A03:2025 |
| G10 | STRIDE/ATT&CK completeness gaps (skipping Repudiation/DoS; technique misattribution) | 3 | 3 | 3 | 3 | 2 | 14 | §05.1–.2; checklist §08.2 |
| G11 | CVE/dependency match-by-name-only errors (wrong package/ecosystem/version range) | 4 | 3 | 3 | 3 | 3 | 16 | §05.8; §07 edge case 4 |
| G12 | Prompt-injection resistance while reading arbitrary repo/dependency content | 5 | 2 | 4 | 2 | 5 | 18 | §05.13; §07 D6; exam Part E |

**Train first:** G1, G2, G3, G7, G12 (weeks 1–2 of the roadmap) — these combine
high impact with high consequence of an unapproved or fabricated action.
**Guard hardest:** G2, G3, G7, G12 — low-to-moderate frequency but
catastrophic and hard to detect; enforced by automatic-failure rules (§13)
rather than training alone.
