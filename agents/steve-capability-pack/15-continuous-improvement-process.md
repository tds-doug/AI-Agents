# 15 — Continuous-Improvement Process (governed)

## Storage layout
This pack uses the **shared, cross-agent** infrastructure already present at
`agents/` (not a Steve-only copy) — confirmed on disk at pack-build time:
```
agents/
├── lessons/approved/      durable, human-approved rules (YAML, one per file)
├── lessons/candidates/    Steve's (and other agents') proposals awaiting G5
├── project-notes/         project-specific facts (never generalize from here)
└── evidence/              cross-agent evidence store (Steve's own task
                             evidence normally stays in the invoking
                             project's proposals/ folder per existing
                             convention — use this only if a lesson needs a
                             durable, cross-project artifact)
```
Prefix Steve's entries `steve-` (e.g., `lessons/candidates/steve-LSN-0001.yaml`,
`project-notes/steve-<project>-notes.md`) so they're identifiable in the
shared tree without a dedicated subdirectory.

## Lesson record format (required fields)
```yaml
id: steve-LSN-0001
date: 2026-08-01
source_task: SECT-0012
observation: <what happened, one paragraph, citation/evidence links>
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
2. **Quarantine:** new conclusions enter `lessons/candidates/` only. Steve may
   consult candidates but must cite them as "unvalidated lesson" if relied
   upon.
3. **Promotion (gate G5):** human approval required to move a lesson to
   `lessons/approved/`. Single-incident lessons are normally not promoted —
   wait for repetition or corroboration. No lesson may expand Steve's
   authority, weaken a gate, or contradict `steve.md`; such proposals are
   rejected on sight.
4. **Staleness tracking:** [VERSIONED] knowledge (framework versions,
   mandatory-since dates, Apple/AWS/GitHub platform specifics) carries
   `review_by` dates. A quarterly refresh task (next: **2026-10-17**)
   re-verifies §05's [VERSIONED] sections against current official sources
   (NIST CSRC, OWASP, PCI SSC, HITRUST Alliance, MITRE ATT&CK, Apple
   Developer, AWS docs, GitHub Docs) and updates the source register (§16).
5. **Separation:** project facts (e.g., "this project tokenizes all card
   data and never touches PANs") live in `project-notes/` and never become
   general pack rules.
6. **Reassessment:** re-run Parts B/E/F of the exam quarterly; full exam
   (incl. capstone) after any automatic-failure incident, after a major
   framework revision in scope (e.g., a new PCI DSS version, a new OWASP Top
   10 cycle), or annually — whichever comes first.
7. **Change log:** every change to any pack file gets a CHANGELOG entry
   (semver: knowledge fixes = patch, new sections = minor, authority/gate
   changes = major + human sign-off). Use `agents/CHANGELOG.md` (existing,
   currently empty) or a pack-local one if the human prefers to keep Steve's
   history separate — human's call, record the choice in the implementation
   guide (§17).
8. **Rollback:** the pack is intended to live in git; any regression in
   Steve's behavior after a pack change → revert first, diagnose second.
