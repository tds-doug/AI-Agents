# Steve — Agent Capability Pack
**Agent:** Steve | **Role:** Cybersecurity/Security Architect (threat modeling, secure-design review, remediation advisory)
**Pack version:** 1.0.0 | **Compiled:** 2026-07-17 | **Review by:** 2026-10-17

## What this is
A role-specific capability, knowledge, and operating-system upgrade for the agent
"Steve." It does **not** retrain any underlying AI model. It equips Steve with a
role charter, current-practice knowledge across NIST 800-53/CSF 2.0/SSDF,
SOC 1/SOC 2, HITRUST CSF, GDPR, CCPA/CPRA, and PCI DSS, an operating playbook,
decision support for risk-vs-business tradeoffs, templates, training, assessment,
and a governed improvement loop — built to sit on top of, not replace,
`steve.md`'s existing frontmatter (tools/model registration) and the team's
shared `DECISION_ROUTING.md`.

This pack does **not** expand Steve's authority beyond what `steve.md` and
`agents/README.md` already grant him: read-only recon (Bash/Read/Grep/Glob),
research (WebSearch/WebFetch), and Write access limited to proposals/threat
models. Steve still cannot Edit application/infra code, still writes findings
only and stops, and still routes ordinary ambiguity to El Jefe per
`DECISION_ROUTING.md`.

## Installation
Place this directory alongside Steve's instruction file:
```
/Users/dj/Projects/AI-Wonder-Team/agents/
├── steve.md                  ← keep existing frontmatter (name/description/tools/model);
│                                replace the body below the frontmatter with
│                                14-improved-agent-instructions.md's body
└── steve-capability-pack/    ← this directory
```
Shared team infrastructure this pack reads/writes into (already present on
disk, shared across agents — not duplicated per pack):
`agents/lessons/approved/`, `agents/lessons/candidates/`, `agents/project-notes/`,
`agents/evidence/` (cross-agent, rarely used by Steve — Steve's own evidence
normally lives in the *invoking project's* `proposals/` folder per existing
convention), `agents/tools/`.

Load order for Steve at task start: `steve.md` → `06-standard-operating-playbook.md`
→ relevant sections of `05-role-knowledge-guide.md` (by framework/technology in
scope) → `08-checklists.md` → `09-templates.md` for the deliverable being produced.

## Contents
| File | Purpose |
|---|---|
| 01-executive-capability-assessment.md | Findings, labeled assumptions, risk summary |
| 02-role-charter.md | Mission, authority, boundaries vs. Dave/Karla/Bisi/Derrick/Diego/El Jefe, done criteria |
| 03-competency-matrix.md | Required competencies by domain and level |
| 04-prioritized-knowledge-gaps.md | Ranked gaps with 5-factor risk scoring |
| 05-role-knowledge-guide.md | Applied security-architecture knowledge (largest file) |
| 06-standard-operating-playbook.md | End-to-end task procedure, intake → lessons learned |
| 07-decision-trees-and-tables.md | Recurring decisions + 7 dangerous edge cases |
| 08-checklists.md | Pre-work, threat-model, compliance-flagging, security-hygiene, self-review, handoff checklists |
| 09-templates.md | 13 fill-in templates with mandatory epistemic labeling |
| 10-training-exercises.md | Progressive exercises incl. adversarial and cross-agent |
| 11-model-solutions.md | Expected solutions with rationale |
| 12-competency-examination.md | The exam (7 parts, 100 pts) |
| 13-scoring-rubric.md | 0–100 rubric, 5 readiness levels, automatic failures |
| 14-improved-agent-instructions.md | Drop-in replacement body for steve.md |
| 15-continuous-improvement-process.md | Governed learning loop using the shared `lessons/` tree |
| 16-source-register.md | Cited sources with dates (NIST, OWASP, PCI SSC, Apple, AWS, etc.) |
| 17-implementation-guide.md | How the human supervisor (DJ) deploys this pack |
| 18-thirty-day-roadmap.md | Day-by-day development plan |

## Quality-review summary (required before adoption — see full detail in 01 §6)
Important assumptions, unresolved questions, sections needing human review, and
capabilities that cannot be safely delegated to Steve are consolidated in
`01-executive-capability-assessment.md` §5–§7. Read that section before treating
any part of this pack as settled.

## Change log
- 1.0.0 (2026-07-17): Initial release.
