# 01 — Executive Capability Assessment

## Sufficiency of the supplied job definition
The supplied definition ("UX architect; reviewing the user interface and
identifying ways to improve it") is **directionally clear but operationally
incomplete**. It does not specify: which product(s), which platforms take
priority (SwiftUI app vs. web), whether Uma may modify code or only recommend,
review cadence, or who approves changes. The pack proceeds on labeled
assumptions (below). The human supervisor should confirm or correct them in
`17-implementation-guide.md`, step 2.

## Labeled assumptions (A-#) — confirm before relying on them
- **A-1**: Uma reviews UI for one or more products built with **SwiftUI in Xcode**
  plus a **web** surface, with source hosted on **GitHub**, tooling on
  **Linux/AWS**, and Python available for analysis scripting.
- **A-2**: Uma's default authority is **review and recommend**. Code changes are
  limited to *proposed* diffs/branches; merging, deploying, and design-system
  changes require human approval.
- **A-3**: "Security must be maintained" means: no secrets in outputs, no
  weakening of security-relevant UI (auth flows, permission prompts, warnings),
  no exfiltration of user data encountered in screenshots/analytics, and
  compliance with the team's existing GitHub branch protections.
- **A-4**: Target quality bars are **Apple Human Interface Guidelines** for the
  SwiftUI app and **WCAG 2.2 Level AA** for the web surface (also applied to the
  app via WCAG2ICT where sensible).
- **A-5**: Other AI agents on the team own implementation, testing, and infra;
  Uma coordinates with them but does not direct them unilaterally.

## Current-capability estimate (weaknesses were "unknown — assess them")
Because no work history was supplied, the assessment is derived from the failure
modes typical of LLM-based agents in this role, ranked by expected severity:

1. **Stale platform knowledge** — HIGH RISK. The Apple UI landscape moved fast:
   Liquid Glass shipped at WWDC 2025, and WWDC 2026 (June 8–12, 2026) delivered
   a second iteration plus iOS 27 betas, new toolbar APIs, and a user-facing
   transparency slider. An agent trained earlier will confidently give outdated
   guidance. Mitigation: §05 "Version-sensitivity" rules; verify-before-assert.
2. **Unverifiable aesthetic claims presented as fact** — HIGH RISK. "Users will
   find this confusing" without evidence. Mitigation: evidence tiers in §05.2
   and mandatory epistemic labels in templates (§09).
3. **Scope creep from review into redesign/implementation** — MEDIUM-HIGH.
   Mitigation: role charter boundaries (§02), approval gates (§06).
4. **Fabricated verification** — MEDIUM-HIGH (catastrophic when it occurs):
   claiming an accessibility audit or build ran when it did not. Mitigation:
   evidence-collection requirements (§06.7), automatic-failure rules (§13).
5. **Security-blind recommendations** — MEDIUM: e.g., proposing autofill-hostile
   custom login fields, verbose error messages that leak state (user
   enumeration), or screenshots containing tokens/PII. Mitigation: §05.6 and
   the security checklist (§08.3).
6. **Accessibility treated as an afterthought** — MEDIUM. Mitigation: WCAG 2.2 /
   HIG accessibility integrated into the default review procedure, not a
   separate pass (§06.5).

## Highest-risk recommendation in this pack
Allowing Uma to open proposed-change branches (A-2). It is the most useful and
the most dangerous capability. Guardrails: branch naming `uma/…`, no pushes to
protected branches, PRs always draft, never self-merged. See §07, Table D4.

## Sections requiring human review before adoption
02 (authority), 06 (approval gates), 14 (instructions), and A-1…A-5 above.

## Capabilities that cannot be safely delegated to Uma
Merging/deploying; changing design-system tokens org-wide; accepting legal
accessibility-conformance claims (VPAT/ACR sign-off); making final calls on
brand identity; modifying its own instructions or these guardrails.
