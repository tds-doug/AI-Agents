# 08 — Checklists
Check items literally; attach evidence where marked (E).

## 08.1 Pre-work inspection
- [ ] Task intake complete; requester + ticket recorded
- [ ] Repo cloned/fetched; commit SHA recorded (E)
- [ ] App builds / preview loads (E: build-log tail or screenshot)
- [ ] Correct target: platform(s), min OS, device sizes listed
- [ ] Design-system reference located (or "none exists" recorded)
- [ ] Tools available: Accessibility Inspector / axe / Python env (E: versions)
- [ ] Security-relevance classification done
- [ ] Evidence directory created: `evidence/<task-id>/`

## 08.2 Screen review (run per screen)
- [ ] Baseline screenshot captured, named per convention (E)
- [ ] Primary action obvious; hierarchy sane; standard nav pattern or justified
- [ ] All states present: loading / empty / error / success (screenshots) (E)
- [ ] Dynamic Type at AX5: no clipping/truncation of essential content (E)
- [ ] Dark mode + Increased Contrast pass (E)
- [ ] Touch targets ≥ 44×44 pt (native) / ≥ 24×24 CSS px or spaced (web)
- [ ] Text contrast ≥ 4.5:1 (3:1 large); non-text UI ≥ 3:1 (E: computed values)
- [ ] Glass/translucent surfaces tested over worst-case backgrounds (E)
- [ ] VoiceOver/screen-reader order + labels sensible (notes) (E)
- [ ] Keyboard-only completion possible (web) ; focus visible, not obscured
- [ ] Copy: plain language, no leaking internals, consistent terminology
- [ ] No dark patterns (pre-checked consent, disguised decline, forced action)

## 08.3 Security & privacy hygiene (every deliverable)
- [ ] No secrets/tokens/keys anywhere in report, screenshots, URLs, or commits
- [ ] PII in screenshots masked or synthetic data used
- [ ] Auth-flow recommendations co-flagged for security review (G3)
- [ ] Error-message recommendations checked for information leakage
- [ ] No recommendation disables paste/password-manager/autofill
- [ ] No recommendation weakens confirmation of destructive actions w/o G3
- [ ] Evidence dir contains nothing beyond what the report needs

## 08.4 Self-review before delivery
- [ ] Every finding: ID, tier, severity, evidence path, citation, recommendation
- [ ] Severity ≤ what tier supports; scopes recorded
- [ ] Reproducible: a stranger could verify each finding from evidence alone
- [ ] Assumptions section present and honest
- [ ] "Not tested" section present (what + why)
- [ ] All [VERSIONED] claims carry version qualifiers
- [ ] Tool claims match saved artifacts exactly (E)
- [ ] Warnings quoted, not laundered into "success"
- [ ] Out-of-scope observations segregated, not investigated
- [ ] Report uses template; epistemic labels applied throughout

## 08.5 Branch/PR (only after G2)
- [ ] Branch `uma/<UX-id>-<slug>` from fresh default branch
- [ ] Only approved files touched (diff reviewed against approved list) (E)
- [ ] Draft PR; `[PROPOSAL][UX-####]` title; template body; `agent-proposal` label
- [ ] No secrets in diff or new screenshots
- [ ] CI results read and quoted (what CI does/doesn't cover stated)
- [ ] Not merged, not marked ready-for-review by Uma

## 08.6 Handoff
- [ ] Handoff report sent (T9); artifacts index included
- [ ] Repo state (branch+SHA) stated; receiver's inherited assumptions listed
- [ ] Receipt acknowledged
