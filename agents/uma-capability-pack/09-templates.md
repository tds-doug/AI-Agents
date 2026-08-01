# 09 — Templates
All templates require **epistemic labels** on substantive statements:
`[FACT-OBSERVED]` directly observed/measured (evidence attached) ·
`[FACT-USER]` supplied by requester (not independently verified) ·
`[INFERENCE]` reasoned from evidence · `[ASSUMPTION]` proceeding-basis ·
`[RECOMMENDATION]` Uma's advice · and in status/completion docs:
`[DONE]` performed (evidence) · `[PROPOSED]` suggested, not performed ·
`[TESTED]` executed with artifact · `[NOT-TESTED]` explicitly untested ·
`[RISK]` remaining risk.

## T1 Task Intake
```
Task ID: UXT-____   Date:        Requester(+ticket):
Goal (one sentence):
Scope: screens/flows/platforms:
Out of scope (explicit):
Constraints (deadline, min OS, formats):
Security-relevant? [ ]no [ ]yes → areas:
Deliverables expected:
```
## T2 Requirements & Assumptions
```
Confirmed facts: [FACT-OBSERVED]/[FACT-USER] …
Open questions (batched, sent on: ____):
Assumptions (each: ASSUMPTION-#, basis, what changes if wrong):
```
## T3 Work Plan
```
Ordered items (screen/flow → method → tools → est.):
Gates expected: G1 [ ] G2 [ ] G3 [ ]
Out-of-scope declarations:
Approval: requested ____ / granted by ____ on ____ (G1 if triggered)
```
## T4 Risk Assessment
```
Risk → likelihood/impact → mitigation   (≥3 rows; PII/staleness/severity-error)
```
## T5 UX Findings Report  ← primary deliverable
```
Header: task ID, date, repo+SHA, build/env, methods used, coverage map
Summary: counts by severity; top 3 themes; overall assessment [INFERENCE]
Findings (each):
  UX-#### | Severity S_ | Tier T_ | Scope: users×flow
  What: …             Where: screen/component + evidence path
  Standard/heuristic cited:
  Impact: [INFERENCE unless measured]
  Recommendation: [RECOMMENDATION] + effort estimate + version notes
Out-of-scope observations (OOS-#, one line each):
Assumptions carried:            Not tested (what + why):
```
## T6 Accessibility Audit Report
As T5 plus: per-SC results table (SC → pass/fail/not-tested → method →
evidence), tool versions, device/AT matrix, and the statement: "This is an
internal audit, not a conformance claim (VPAT/ACR requires human sign-off)."
## T7 Proposed-Change PR body
```
[PROPOSAL][UX-####] Title
Finding + link; What this changes / does NOT change; Files touched (=G2 list);
Verification: [TESTED …artifacts] [NOT-TESTED …]; Risks; Rollback: revert PR.
Approval: G2 granted by ____ on ____.
```
## T8 Approval Request
```
Gate: G_   What I will do (exact):   What I will NOT do:
Why needed; alternatives considered:   Rollback path:
Deadline impact if delayed:
```
## T9 Handoff Report
```
To: ____  Delivered: …  Artifacts index: …  Repo state: branch+SHA
Open questions you inherit:   Assumptions you inherit:   Ack received: [ ]
```
## T10 Status Report
```
Period; Done [DONE+evidence]; In progress; Blocked (by what, since when);
Next; Gates pending; Risks changed.
```
## T11 Incident / Failure Report
```
Severity: SEV-_  Discovered: when/how [FACT-OBSERVED]
What happened (no secrets reproduced — describe, don't paste):
Immediate action taken:      Work stopped: [ ]yes
Who notified, when:          Suggested next steps [RECOMMENDATION]:
```
## T12 Lessons Learned
```
Task; What went well; What went wrong; Root cause [INFERENCE];
Candidate durable lesson? [ ]no [ ]yes → draft rule + evidence → route §15/G5
Project-specific notes (stay out of pack):
```
## T13 Final Completion Report
```
Task ID; Definition-of-done items → each [DONE/NOT-DONE + evidence];
Actions performed [DONE] vs proposed only [PROPOSED];
Tests executed [TESTED] vs not [NOT-TESTED];
Remaining risks [RISK]; Gates satisfied (list, approver, date);
Deliverable locations.
```
