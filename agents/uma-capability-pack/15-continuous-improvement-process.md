# 15 — Continuous-Improvement Process (governed)

## Storage layout
```
uma-capability-pack/
├── lessons/approved/      durable, human-approved rules (YAML, one per file)
├── lessons/candidates/    Uma's proposals awaiting G5
├── project-notes/         project-specific facts (never generalize from here)
└── CHANGELOG.md           every pack change, versioned
```

## Lesson record format (required fields)
```yaml
id: LSN-0001
date: 2026-07-20
source_task: UXT-0042
observation: <what happened, one paragraph, evidence links>
proposed_rule: <imperative, testable>
evidence_strength: single-incident | repeated(n=_) | externally-corroborated
scope: general | project:<name>        # project-scoped stays in project-notes
expires_or_review_by: <date>           # mandatory for [VERSIONED] content
sources: [<urls + dates if external>]
status: candidate | approved(by, date) | retired(date, reason)
```

## Rules of the loop
1. **Capture:** every task ends with T12; mistakes and corrections are logged
   the day they occur, with evidence.
2. **Quarantine:** new conclusions enter `candidates/` only. Uma may consult
   candidates but must cite them as "unvalidated lesson" if relied upon.
3. **Promotion (gate G5):** human approval required to move a lesson to
   `approved/`. Single-incident lessons are normally not promoted — wait for
   repetition or corroboration. No lesson may expand Uma's authority, weaken
   a gate, or contradict uma.md; such proposals are rejected on sight.
4. **Staleness tracking:** [VERSIONED] knowledge (Apple platform, browser,
   tool versions) carries `review_by` dates. A quarterly refresh task
   (next: 2026-10-12) re-verifies §05.3/§05.10 against current official docs
   and WWDC/release notes, and updates the source register.
5. **Separation:** project facts ("our nav bar is intentionally custom") live
   in project-notes and never become general rules.
6. **Reassessment:** re-run Parts B/E/F of the exam quarterly; full exam
   (incl. capstone) after any automatic-failure incident, after major platform
   shifts (e.g., iOS 27 GA), or annually — whichever comes first.
7. **Change log:** every change to any pack file gets a CHANGELOG entry
   (semver: knowledge fixes = patch, new sections = minor, authority/gate
   changes = major + human sign-off).
8. **Rollback:** the pack is in git; any regression in Uma's behavior after a
   pack change → revert first, diagnose second.
