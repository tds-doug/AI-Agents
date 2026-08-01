# 04 — Prioritized Knowledge Gaps
Scoring: each factor 1–5. **Priority = Impact + Error-probability +
Detection-difficulty + Frequency + Unapproved-action-consequence** (max 25).

| # | Gap | Imp | Err | Det | Freq | Cons | Total | Remediation |
|---|-----|----|----|----|----|----|------|-------------|
| G1 | Post-cutoff Apple platform changes (Liquid Glass v2, iOS 27 APIs, new toolbar/Document APIs from WWDC26) | 5 | 5 | 4 | 5 | 2 | 21 | §05.3 + verify-before-assert rule; quarterly refresh (§15) |
| G2 | Fabrication risk: asserting audits/tests ran without artifacts | 5 | 3 | 5 | 4 | 4 | 21 | Evidence rules §06.7; auto-fail §13 |
| G3 | WCAG 2.2 applied concretely (esp. new SCs: Focus Not Obscured, Target Size 24×24, Dragging Movements, Accessible Authentication, Redundant Entry, Consistent Help) | 4 | 4 | 4 | 5 | 2 | 19 | §05.4 with per-SC test methods |
| G4 | Severity calibration & evidence tiers (opinion inflation) | 4 | 4 | 4 | 5 | 1 | 18 | §05.2; calibration exercises §10.E3 |
| G5 | Secure-UX intersection (auth flows, error leakage, permission prompts) | 5 | 3 | 4 | 3 | 3 | 18 | §05.6; joint-review gate G3 |
| G6 | Git/GitHub discipline (branch protection, draft PRs, never self-merge) | 4 | 3 | 2 | 4 | 5 | 18 | §05.7; hard rules §14 |
| G7 | Liquid Glass legibility/contrast pitfalls (documented NN/g criticism; iOS 27 transparency slider changes the calculus) | 4 | 4 | 3 | 4 | 1 | 16 | §05.3.4 |
| G8 | Scope control: review → redesign creep | 3 | 4 | 3 | 4 | 2 | 16 | Charter §02; playbook §06.2 |
| G9 | Screenshot/PII/secret hygiene | 4 | 2 | 4 | 3 | 3 | 16 | §08.3 checklist |
| G10 | Web ARIA/APG patterns for custom widgets | 3 | 3 | 3 | 3 | 1 | 13 | §05.5 |
| G11 | Coordination protocol with other agents (handoffs, conflicting asks) | 3 | 3 | 2 | 3 | 2 | 13 | §06.9, §09.T9 |
| G12 | Python evidence tooling (contrast calc, report generation) | 2 | 2 | 2 | 3 | 1 | 10 | §10.E2 |

**Train first:** G1–G4 (weeks 1–2 of the roadmap). **Guard hardest:** G2, G6 —
low frequency but catastrophic and hard to detect; enforced by automatic-failure
rules rather than training alone.
