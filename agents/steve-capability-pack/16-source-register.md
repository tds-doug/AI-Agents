# 16 — Source Register
Verified via web research on 2026-07-17 unless marked [training-knowledge —
verify before load-bearing use]. Record format: ID · source · date · why cited.

- **S1/S2** Microsoft Security Development Lifecycle, *Threat Modeling* /
  Adam Shostack's four-question threat-modeling frame and STRIDE —
  https://learn.microsoft.com/en-us/azure/security/develop/threat-modeling-tool-threats
  [training-knowledge, stable — canonical structuring method Steve uses for
  every engagement; verify the live page still describes STRIDE identically
  before citing a specific category definition verbatim].
- **S3** MITRE, *ATT&CK Version 19 / April 2026 Updates* —
  https://attack.mitre.org/resources/updates/updates-april-2026/ and
  https://attack.mitre.org/resources/versions/ — released 2026-04-28; Defense
  Evasion split into Stealth (TA0005) and Defense Impairment (TA0112);
  Enterprise ATT&CK: 15 tactics, 222 techniques, 475 sub-techniques.
- **S4** NIST CSRC, *NIST Releases Revision to SP 800-53 Controls* —
  https://csrc.nist.gov/News/2025/nist-releases-revision-to-sp-800-53-controls
  — and *SP 800-53 Rev. 5 (upd. 1), final* —
  https://csrc.nist.gov/pubs/sp/800/53/r5/upd1/final — Release 5.2.0 dated
  2025-08-27, issued per Executive Order 14306 on software update/patch
  security.
- **S5** NIST, *Cybersecurity Framework* —
  https://www.nist.gov/cyberframework — CSF 2.0 published 2024-02, six
  functions incl. Govern; NIST CSRC, *Two New CSF 2.0 Quick-Start Guides* —
  https://csrc.nist.gov/News/2026/two-new-csf-2-0-quick-start-guides — notes
  the draft Cyber AI Profile (2025-12) [CURRENT, evolving — verify status
  before citing as final].
- **S6** NIST CSRC, *SP 800-218 SSDF, final* —
  https://csrc.nist.gov/pubs/sp/800/218/final — v1.1, 2022-02, current
  authoritative version; *SP 800-218 Rev. 1 (Draft)* —
  https://csrc.nist.gov/pubs/sp/800/218/r1/ipd — v1.2 draft dated 2025-12-17,
  not yet final as of 2026-07.
- **S7** AICPA Trust Services Criteria (TSP Section 100, 2017 TSC with
  revised points of focus, 2022) — summarized via secondary sources
  (soc2auditors.org, Drata, EY AccountingLink) as no wholly new TSC version
  has been issued for 2026 [secondary corroboration; AICPA is the primary
  source of record but was not directly fetched — verify against
  aicpa-cima.com before a load-bearing citation of specific TSC wording].
- **S8** HITRUST Alliance, *HAA 2026-002 CSF Version 11.8.0 Release* —
  https://hitrustalliance.net/advisories/haa-2026-002-csf-version-11.8.0-release
  — released 2026-05-07, available 2026-05-08; requirement-statement
  consolidation, new mappings incl. OWASP Top 10 for LLM Applications 2025.
- **S9** IAPP, *EU AI Act: Mapping the Interplays with the GDPR* —
  https://iapp.org/resources/article/mapping-interplays-gdpr-eu-ai-act — and
  euaiact.com, *Key Issue 6: Interplay with GDPR* —
  https://www.euaiact.com/key-issue/6 — Annex III high-risk obligations phase
  in from 2026-08; joint EDPB/Commission guidance still in progress as of
  2026-07 [CURRENT, fast-moving — reconfirm before citing enforcement
  specifics].
- **S10** California Privacy Protection Agency, *Law & Regulations* —
  https://cppa.ca.gov/regulations/ — and *CCPA Updates: Cybersecurity Audits,
  Risk Assessments, ADMT, Insurance Regulations* —
  https://cppa.ca.gov/regulations/ccpa_updates.html — regulations effective
  2026-01-01; sensitive personal information expanded to include neural data;
  ADMT compliance required 2027-01-01 for existing uses; cybersecurity-audit
  deadlines phase in 2028–2030 by revenue tier.
- **S11** PCI Security Standards Council, *Just Published: PCI DSS v4.0.1* —
  https://blog.pcisecuritystandards.org/just-published-pci-dss-v4-0-1 —
  v4.0 retired 2024-12-31; all 51 future-dated requirements from v4.0 became
  mandatory 2025-03-31, no grace period.
- **S12** OWASP, *OWASP Top 10:2025* — https://owasp.org/Top10/2025/ — final
  release January 2026; A03 Software Supply Chain Failures and A10
  Mishandling of Exceptional Conditions are new; SSRF folded into A01.
- **S13** OWASP, *ASVS 5.0.0* —
  https://github.com/OWASP/ASVS/releases/tag/v5.0.0 and
  https://owasp.org/www-project-application-security-verification-standard/
  — released 2025-05-30 at Global AppSec EU Barcelona; ~350 requirements
  across 17 chapters.
- **S14** OWASP, *MASVS* — https://mas.owasp.org/MASVS/ — v2.1.0, 2024-01-18
  (adds MASVS-PRIVACY), current as of 2026-07; OWASP/mastg GitHub releases —
  https://github.com/OWASP/mastg/releases — MASTG v2.0.0 stable release in
  2026, modular refactor tied to MASVS/MASWE.
- **S15** Apple, *Security overview* — https://developer.apple.com/security/
  — and Apple Support, *Keychain data protection* —
  https://support.apple.com/guide/security/keychain-data-protection-secb0694df1a/web
  — ATS enforces TLS 1.2+/forward secrecy by default; Keychain items
  encrypted with AES-256-GCM (separate metadata/secret keys)
  [training-knowledge corroborated by these pages — verify current page
  revision before citing a specific technical detail as unchanged].
- **S16** Apple Developer, *Privacy manifest files* —
  https://developer.apple.com/documentation/bundleresources/privacy-manifest-files
  — and *Reminder: Privacy requirement for app submissions starts May 1* —
  https://developer.apple.com/news/?id=pvszzano — required-reason API
  declarations enforced in App Store Connect since 2024-05-01.
- **S17** Swift.org, *Swift 6 Migration Guide — Data Race Safety* —
  https://www.swift.org/migration/documentation/swift-6-concurrency-migration-guide/dataracesafety/
  — and Apple Developer, *Adopting strict concurrency in Swift 6 apps* —
  https://developer.apple.com/documentation/swift/adoptingswift6 — strict
  concurrency checking is default in Swift 6; Sendable/actor isolation
  convert data races into compile-time errors.
- **S18** AWS, *Security Pillar — AWS Well-Architected Framework* —
  https://docs.aws.amazon.com/wellarchitected/latest/security-pillar/welcome.html
  — seven domains: security foundations, IAM, detection, infrastructure
  protection, data protection, incident response, application security.
- **S19** GitHub Docs, *Push protection* —
  https://docs.github.com/en/code-security/concepts/secret-security/push-protection
  — and GitHub Changelog, *Secret scanning — coverage update* (2026-03-31) —
  https://github.blog/changelog/2026-03-31-github-secret-scanning-nine-new-types-and-more/
  — push protection off by default per repo but dozens of detectors
  push-protected by default org/enterprise-wide as of 2026; base64-encoded
  secret detection added with push protection, 2025-11.
- **S20** SLSA, *Supply-chain Levels for Software Artifacts* —
  https://slsa.dev/ — current version v1.1; Levels 0–3, cumulative,
  incrementally adoptable.
- **S21** CIS, *CIS Critical Security Controls v8.1* —
  https://www.cisecurity.org/controls/v8-1 — released 2024-06; 18 controls,
  153 safeguards, 3 Implementation Groups; aligned to CSF 2.0's Govern
  function.

**Disagreements noted:** secondary sources vary in how strongly they frame
the GDPR–AI Act enforcement interplay (S9) — treat as unresolved until the
joint EDPB/Commission guidance is finalized. **Fast-decay knowledge:**
everything version/date-specific in S3–S6, S8, S10–S14, S19 (frameworks that
revised in the 2025–2026 window); review_by **2026-10-17** (§15).
