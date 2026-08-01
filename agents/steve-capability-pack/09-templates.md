# 09 — Templates
All templates require **epistemic labels** on substantive statements:
`[FACT-OBSERVED]` directly observed in source/recon (cite path/command) ·
`[FACT-USER]` supplied by requester (not independently verified) ·
`[INFERENCE]` reasoned from evidence · `[ASSUMPTION]` proceeding-basis ·
`[RECOMMENDATION]` Steve's advice · and in status/completion docs:
`[DONE]` performed (evidence) · `[PROPOSED]` suggested, not performed ·
`[VERIFIED]` independently confirmed exploitable (name the verifier) ·
`[NOT-VERIFIED]` explicitly unverified/theoretical · `[RISK]` remaining risk.

## T1 Task Intake
```
Task ID: SECT-____   Date:        Requester(+context):
Goal (one sentence):
Scope: system/feature/components:
Out of scope (explicit):
Constraints (deadline, production-touching?, known compliance context):
Deliverable expected: threat model / proposal / compliance-flagging note
```
## T2 Requirements & Assumptions
```
Confirmed facts: [FACT-OBSERVED]/[FACT-USER] …
Open questions (batched, sent on: ____):
Assumptions (each: ASSUMPTION-#, basis, what changes if wrong):
```
## T3 Work Plan
```
Trust boundaries / components in scope → STRIDE coverage plan → research
needed (frameworks/CVEs to verify) → est. time
Gates expected: G1 [ ] G2 [ ]
Authorization confirmed for anything beyond local checkout: [ ]
```
## T4 Risk Assessment / Register
```
Row per credible threat:
ID | STRIDE category | Asset | Trust boundary | Likelihood | Impact |
Evidence status | Severity+method | Cited source | Proposed control
```
## T5 Threat Model / Secure Architecture Proposal  ← primary deliverable
```
Header: task ID, date, repo+commit, system/scope, methods used, coverage map
Summary: counts by severity; top themes; overall assessment [INFERENCE]
Findings (each):
  SEC-#### | Severity S_ + method | Evidence: Confirmed/Theoretical/Reported
  What: …                    Where: file/component/trust-boundary + citation
  Standard/CVE/ATT&CK cited:
  Impact: [INFERENCE unless independently verified]
  Proposed architecture/control: [RECOMMENDATION] — concrete enough to build
  Compensating control (if tradeoff-shaped): [RECOMMENDATION]
  Compliance relevance (if evidenced): framework + specific control ID
Out-of-scope observations (OOS-#, one line each):
Assumptions carried:            Not verified (what + why):
```
## T6 Framework/Compliance Mapping Note (when a finding is compliance-relevant)
```
Finding(s) referenced:  Framework: (NIST 800-53/CSF/SSDF | SOC 2 | HITRUST |
GDPR | CCPA/CPRA | PCI DSS)  Specific control/article/requirement ID:
Basis for applicability: [FACT-OBSERVED — actual data flow, not assumption]
Statement: "This note flags relevance; it is not a compliance determination
or audit opinion. Route to Bisi for ongoing tracking."
```
## T7 Verification/Implementation Handoff Spec
```
To: Karla (verification) / Dave (infra) / Diego (application)
Finding(s): SEC-####
Exactly what needs verification or building:
What Steve did NOT do: (run the exploit / change the config / write the code)
Suggested test/acceptance criteria:
```
## T8 Approval / Risk-Acceptance Request
```
Gate: G_   Finding(s): SEC-####
What I recommend (exact):        Alternative(s) considered (incl. compensate):
If risk is accepted instead of fixed — state the actual cost/impact being
accepted, in concrete terms. This section is a decision for the requester,
not Steve's conclusion.
Deadline impact if delayed:
```
## T9 Handoff Report
```
To: ____  Delivered: …  Findings by disposition: needs-Karla-verification /
needs-Dave-implementation / needs-Diego-implementation / needs-Bisi-tracking /
needs-human-risk-decision
Repo state: branch/commit   Assumptions inherited:   Ack received: [ ]
```
## T10 Status Report
```
Period; Done [DONE+evidence]; In progress; Blocked (by what, since when);
Next; Gates pending; Risks changed.
```
## T11 Incident / Failure Report (live secret, active compromise, PII exposure)
```
Severity: SEV-_  Discovered: when/how [FACT-OBSERVED]
What happened (no secrets/PII reproduced — describe, don't paste):
Immediate action taken:      Work stopped: [ ]yes
Who notified, when (Derrick/human):   Suggested next steps [RECOMMENDATION]:
```
## T12 Lessons Learned
```
Task; What went well; What went wrong; Root cause [INFERENCE];
Candidate durable lesson? [ ]no [ ]yes → draft rule + evidence → route §15/G5
Project-specific notes (stay in project-notes, not the pack):
```
## T13 Final Completion Report
```
Task ID; Definition-of-done items → each [DONE/NOT-DONE + evidence];
Findings delivered vs. proposed-only [PROPOSED];
Verifications executed [VERIFIED, by whom] vs. not [NOT-VERIFIED];
Remaining risks [RISK]; Gates satisfied (list, approver, date);
Deliverable locations.
```
