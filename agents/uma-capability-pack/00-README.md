# Uma — Agent Capability Pack
**Agent:** Uma | **Role:** UX Architect (UI review & improvement)
**Pack version:** 1.0.0 | **Compiled:** 2026-07-12 | **Review by:** 2026-10-12

## What this is
A role-specific capability, knowledge, and operating-system upgrade for the agent
"Uma." It does **not** retrain any underlying AI model. It equips Uma with a role
charter, current-practice knowledge, an operating playbook, decision support,
templates, training, assessment, and a governed improvement loop.

## Installation
Place this directory alongside Uma's instruction file:
```
agents/
├── uma.md                  ← replace body with 14-improved-agent-instructions.md
└── uma-capability-pack/    ← this directory
```
Load order for Uma at task start: `uma.md` → `06-standard-operating-playbook.md`
→ relevant sections of `05-role-knowledge-guide.md` → `08-checklists.md`.

## Contents
| File | Purpose |
|---|---|
| 01-executive-capability-assessment.md | Findings, assumptions, risk summary |
| 02-role-charter.md | Mission, authority, boundaries, done criteria |
| 03-competency-matrix.md | Required competencies by domain and level |
| 04-prioritized-knowledge-gaps.md | Ranked gaps with risk scoring |
| 05-role-knowledge-guide.md | Applied knowledge for the role (largest file) |
| 06-standard-operating-playbook.md | End-to-end task procedure |
| 07-decision-trees-and-tables.md | Recurring decisions + dangerous edge cases |
| 08-checklists.md | Pre-work, review, security, handoff checklists |
| 09-templates.md | 13 fill-in templates with epistemic labeling |
| 10-training-exercises.md | Progressive exercises incl. adversarial |
| 11-model-solutions.md | Expected solutions with rationale |
| 12-competency-examination.md | The exam |
| 13-scoring-rubric.md | 0–100 rubric, levels, automatic failures |
| 14-improved-agent-instructions.md | Drop-in replacement body for uma.md |
| 15-continuous-improvement-process.md | Governed learning loop |
| 16-source-register.md | Cited sources with dates |
| 17-implementation-guide.md | How the human supervisor deploys this |
| 18-thirty-day-roadmap.md | Day-by-day development plan |

## Change log
- 1.0.0 (2026-07-12): Initial release.
