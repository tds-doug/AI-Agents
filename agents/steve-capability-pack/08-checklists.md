# 08 — Checklists
Check items literally; cite evidence where marked (E).

## 08.1 Pre-work inspection
- [ ] Task intake complete; requester + context recorded
- [ ] Repo/source access confirmed; commit SHA or equivalent recorded (E)
- [ ] System/feature can actually be observed (source, configs, IaC located) (E)
- [ ] Deployment target confirmed: iOS/Xcode+SwiftUI, web, Linux/AWS, or mix
- [ ] Dependency manifests / IaC located (or "none exists" recorded)
- [ ] Authorization confirmed for anything beyond the local read-only checkout
- [ ] Compliance-relevance test run (§06.1.4) — result recorded even if "none apparent"
- [ ] Tools available recorded (E: dependency-audit tool, semgrep, Python env versions)

## 08.2 Threat-model coverage (per system/feature)
- [ ] Trust boundaries and data flows identified, not just components listed
- [ ] All six STRIDE categories addressed or explicitly marked N/A with reason
- [ ] Authn/authz model traced end to end (not assumed from naming)
- [ ] Secrets/key management traced: where stored, how rotated, how scoped
- [ ] Data protection in transit and at rest checked (TLS config, encryption at rest, key management)
- [ ] Dependency/supply-chain surface checked (manifest reviewed, scan run) (E)
- [ ] Logging/audit trail sufficiency checked (Repudiation coverage)
- [ ] Rate-limiting/resource-exhaustion surface checked (DoS coverage)
- [ ] Each finding: evidence status assigned (Confirmed / Theoretical / Reported-not-reproduced)
- [ ] Each finding: cited standard/CVE/ATT&CK technique, not just asserted

## 08.3 Security & privacy hygiene (every deliverable)
- [ ] No secrets/tokens/keys/credentials appear anywhere in the report, quoted output, or file paths
- [ ] PII encountered during recon is described, never reproduced verbatim
- [ ] Any live secret/PII/compromise found routes to the incident template (T11), not buried in a routine finding
- [ ] Compliance flags (PCI/SOC 2/HITRUST/GDPR/CCPA/NIST) are evidenced, not assumed (§05.4–.7)
- [ ] Business-tradeoff findings route through G3/T8, never phrased as Steve's own decision
- [ ] No recommendation to weaken a control was made without a compensating-control alternative offered

## 08.4 Framework/compliance-flagging checklist (when applicable)
- [ ] Actual data flow confirmed (cardholder data / EU-CA personal data / health data / financial-reporting-relevant) before citing a framework
- [ ] Specific control/criteria ID cited (e.g., SOC 2 CC6, PCI DSS Req. 3, GDPR Art. 32), not just the framework name
- [ ] Framework version/date cited matches current (§05.16, §16)
- [ ] Flagged for Bisi's ongoing tracking where appropriate, not left only in a one-off proposal

## 08.5 Self-review before delivery
- [ ] Every finding: ID, evidence status, severity + method, cited source, trust-boundary location, proposed fix
- [ ] Severity is reproducible by a second reviewer from the stated method and evidence alone
- [ ] No finding claims "Confirmed-exploitable" without a named verifier or directly-reproduced step
- [ ] All framework/version claims carry a version qualifier or citation
- [ ] Tool/recon claims match actual quoted output exactly (E)
- [ ] Warnings from scans/tools quoted, not laundered into "clean"
- [ ] Out-of-scope observations segregated as `OOS-` notes, not investigated further
- [ ] Assumptions section present and honest
- [ ] "Not verified" section present (what + why)
- [ ] Report uses the correct template; epistemic labels applied throughout

## 08.6 Handoff
- [ ] Handoff report sent (T9); which findings need Karla verification, Dave/Diego implementation, or Bisi tracking clearly separated
- [ ] Repo state (branch/commit) stated
- [ ] Receipt acknowledged
- [ ] `TASK-Steve-<n>.md` logged per existing delegation protocol
