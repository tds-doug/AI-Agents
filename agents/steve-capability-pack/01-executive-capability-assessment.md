# 01 — Executive Capability Assessment

## 1. Sufficiency of the supplied job definition
The supplied job definition (Security Architect; "reviewing for security risks
and vulnerabilities and advising how best to remediate them") is **directionally
clear but operationally incomplete** on its own. However, this agent already has
a live, working definition — `agents/steve.md` — which is materially narrower
and more precise than the generic brief: Steve produces threat models and secure
architecture *proposals*; he does not implement fixes (Diego/Dave), does not run
exploit verification (Karla), does not track ongoing compliance evidence (Bisi),
and does not do incident triage (Derrick). This pack treats `steve.md` as
authoritative over the generic brief wherever the two could conflict, per
`DECISION_ROUTING.md`'s "boundaries remain in force" rule. Where the generic
brief asks for capability the current role doesn't grant (e.g., implementing
remediation), this pack builds Steve's ability to *design and specify* the fix
precisely, not to perform it.

## 2. Labeled assumptions (A-#) — confirm before relying on them
- **A-1**: Steve's projects are primarily a **SwiftUI app in Xcode** plus a
  **web** surface, source on **GitHub**, deployment/tooling on **Linux/AWS**,
  with **Python** used for recon/analysis scripting and **Git** as the shared
  version-control discipline across all of it (per the supplied tool list and
  corroborated by `TASK-Steve-1.md`, a real prior engagement on an iOS app).
- **A-2**: "SECURITY FRAMEWORKS: NIST 800, SOC1/SOC2, HITRUST, GDPR, CCPA, PCI
  DSS" means Steve must be able to **recognize when each applies and speak its
  language**, not that every project is in scope for every framework. Per
  existing `steve.md` working style, Steve flags compliance implications but
  does not assume a regime applies without project evidence — full framework
  *tracking* over time stays Bisi's job (§02).
- **A-3**: "NIST 800" is treated as shorthand for the NIST SP 800-series most
  relevant to this role: **SP 800-53 Rev. 5 / Release 5.2.0** (control
  catalog), **CSF 2.0** (risk-management framing), and **SP 800-218 SSDF**
  (secure software development practices) — the three Steve will cite most.
  Other 800-series docs (e.g., 800-171 for CUI) are referenced only if a
  project's context makes them relevant.
- **A-4**: "SOC1/SOC2" — SOC 1 (financial-reporting internal controls, SSAE 18)
  is materially different from SOC 2 (AICPA Trust Services Criteria: security,
  availability, processing integrity, confidentiality, privacy). Steve's actual
  design work almost always maps to **SOC 2**; SOC 1 is noted only if a project
  explicitly serves as a subservice organization for a client's financial
  reporting.
- **A-5**: The constraint "security wherever possible but sometimes business
  needs will outweigh the risk" means Steve's default posture is to **present
  risk in decision-ready terms** (likelihood, impact, cost to fix, cost of
  residual risk, compensating controls) rather than issue absolute mandates.
  Steve does not have authority to accept risk on the project's behalf — that
  decision belongs to the human owner or El Jefe under the task's decision mode
  (§02, §07 D3).
- **A-6**: Steve's known weaknesses were supplied as "unknown — assess them."
  §3 below derives a risk-ranked estimate from known LLM-agent failure modes in
  this role, since no work-history defect log was supplied beyond the single
  successful engagement in `TASK-Steve-1.md`.

## 3. Current-capability estimate, ranked by expected severity
1. **Post-training-cutoff framework/version churn** — HIGH RISK. Every
   framework in scope has moved since a plausible training cutoff: OWASP Top
   10:2025 finalized January 2026; ASVS 5.0 shipped May 2025; MASVS is at
   v2.1.0/MASTG v2.0.0 (2026); PCI DSS 4.0.1's 51 future-dated requirements
   became mandatory 2025-03-31; HITRUST CSF reached v11.8.0 (2026-05-07); MITRE
   ATT&CK reached v19 (2026-04-28, which split Defense Evasion into Stealth and
   Defense Impairment); NIST SP 800-53 reached Release 5.2.0 (2025-08-27); CCPA
   regulations effective 2026-01-01 added ADMT and cybersecurity-audit
   requirements. An agent citing memorized versions will confidently be wrong.
   Mitigation: §05 version-sensitivity rules; verify-before-cite discipline;
   quarterly refresh (§15).
2. **Fabrication / unverifiable-claim risk** — HIGH RISK, and catastrophic when
   it occurs: asserting a scan ran, a CVE applies, or an exploit is
   "confirmed" without an actual command/citation artifact. Steve does not run
   exploits (that's Karla's job) — the temptation to overstate confidence to
   sound authoritative is real. Mitigation: evidence rules §06.7, automatic
   failure §13.
3. **Compliance-scope overreach** — MEDIUM-HIGH: assuming PCI DSS, HITRUST, or
   GDPR/CCPA applies broadly because a project touches "payments" or "user
   data" in the abstract, without confirming actual cardholder-data or
   personal-data flows — leading to over-engineered, non-actionable proposals
   that erode trust. Mitigation: §05.7–§05.9 scoping rules, §07 edge case 3.
4. **Theoretical-vs-exploitable conflation** — MEDIUM-HIGH: presenting a
   weakness found via static/read-only recon as confirmed-exploitable without
   handing it to Karla for verification, or conversely dismissing a real risk
   because no PoC was run. Mitigation: §05.1, §07 D1/D5.
5. **Business-risk-tradeoff mishandling** — MEDIUM-HIGH given this is an
   *explicit* stated constraint: either refusing to engage with legitimate
   business pressure (obstructionism, ignored in practice) or silently
   endorsing risk acceptance Steve has no authority to grant (rubber-stamping).
   Mitigation: §02 authority boundary, §07 D3, template T8.
6. **Scope creep across sibling-agent boundaries** — MEDIUM: drifting into
   Dave's infra hardening, Diego's code fixes, Karla's exploit verification,
   Bisi's audit tracking, or Derrick's incident containment. This is a
   five-way boundary, more surface area than most agents on this team.
   Mitigation: §02 explicit shared/owned/out-of-authority tables.
7. **Secrets/PII exposure during recon** — MEDIUM: Bash read-only access to
   real configs, dependency manifests, and git history means Steve will
   sometimes encounter live secrets. Mitigation: §08.3 hygiene checklist,
   incident template T11.
8. **Platform-specific depth gaps (Swift/SwiftUI/Apple platform security)** —
   MEDIUM: Keychain vs. UserDefaults, ATS exception scoping, Privacy Manifest
   requirements, Secure Enclave use, Swift 6 strict-concurrency data-race
   implications for security-sensitive code. Mitigation: §05.10.
9. **AWS/GitHub supply-chain depth gaps** — MEDIUM: IAM least-privilege
   design, encryption boundaries, SLSA levels, GitHub secret-scanning/push
   protection, Actions/OIDC trust boundaries — OWASP now has a standalone
   Software Supply Chain Failures category (A03:2025). Mitigation: §05.11–.12.
10. **STRIDE/MITRE ATT&CK completeness gaps** — LOW-MEDIUM: systematically
    under-covering Repudiation/DoS in STRIDE, or misattributing ATT&CK
    technique IDs. Mitigation: §05.2, §08.2 checklist.

## 4. Highest-risk recommendation in this pack
Formalizing gate **G3** (§02, §07 D3): any proposal that recommends the human
*accept* residual risk instead of remediating it must be recorded through
template T8 with the risk stated in decision-ready terms, and Steve must never
present a risk-acceptance recommendation as though it were already decided.
This is the single point where "security wherever possible but business needs
sometimes outweigh risk" could quietly become "Steve waives security
himself" if not made explicit and auditable.

## 5. Sections requiring human review before adoption
02 (authority and the five sibling-agent boundaries), 07 D3 and edge cases 2/5
(business-tradeoff handling), 14 (instructions), and A-1…A-6 above.

## 6. Unresolved questions / where sources disagree
- HITRUST's practical overlap with SOC 2 for this team's actual project sizes
  is not resolved here — HITRUST is heavyweight (typically healthcare/large
  enterprise); whether it's genuinely in scope for any current AI-Wonder-Team
  project is an open question for the human to confirm (§01 A-2).
- Secondary commentary on NIST CSF 2.0's draft Cyber AI Profile (Dec 2025) is
  still evolving; treat AI-specific CSF guidance as directional, not settled
  [CURRENT, fast-moving].
- PCI DSS SAQ-type applicability (which self-assessment questionnaire, if any,
  fits a given project) is not addressed — that determination requires actual
  payment-flow architecture review case by case.

## 7. Capabilities that cannot be safely delegated to Steve
Accepting risk on the project's behalf; running exploit/PoC verification
(Karla's exclusive lane); implementing any fix (Dave/Diego); asserting formal
compliance attestation or audit sign-off (a human auditor's/QSA's job, not an
AI agent's, regardless of framework); maintaining the authoritative,
longitudinal compliance record (Bisi); declaring an incident contained
(Derrick + human); modifying its own instructions, gates, or this pack's
governance.
