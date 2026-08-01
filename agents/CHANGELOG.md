# Changelog

## 2026-08-01 — Cross-AI agent discovery enabled

- Added Codex-native `.codex/agents/*.toml` generation from the canonical
  `agents/<name>.md` roster.
- Added project-scoped Claude symlinks for every shared agent.
- Preserved the explicit runtime exceptions: Kyle is Claude-only and Randy is
  Codex-only.
- Added `agents/sync-agent-configs.rb` so both discovery trees can be refreshed
  deterministically after canonical agent changes.
- Completed Uma's Claude metadata so it can be discovered consistently by both
  clients.

## 2026-08-01 — DJ Agent Sync skill added

- Added the project-scoped `dj-agent-sync` skill for full-roster synchronization
  through `/dj-agent-sync` or `$dj-agent-sync`.
- Added targeted `agent.md claude|codex|all` synchronization while preserving
  the Kyle Claude-only and Randy Codex-only exception gates.
- Documented Claude `.claude/skills` and Codex `.agents/skills` discovery
  wiring.

## 2026-07-31 — Approval enforcement moved to parent client

- Made the user-facing Claude/Codex parent the sole approval gatekeeper.
- Defined every parent-dispatched assignment as pre-authorized within scope.
- Removed approval-provenance auditing from El Jefe and Dave; they may stop for
  technical safety conditions or material scope expansion, not to re-verify
  Fat Cat's consent.
- Retained relay language only as compatibility guidance; a special relay is no
  longer required because dispatch itself carries execution authority.

## 2026-07-30 — Client-neutral human approval relay

- Added a shared approval-relay contract to `DECISION_ROUTING.md`: Fat Cat's
  approval in an active Codex or Claude conversation is authoritative when
  relayed to an agent through normal coordination context.
- Removed the duplicated Claude Code/`SendMessage`-specific authorization text
  from El Jefe, Diego, Kyle, and Dave.
- Explicitly wired Uma and her governing capability-pack instructions into the
  shared contract.
- Clarified that no Git commit, approval file, direct agent conversation, or
  client-specific transport is required, while preserving scope limits,
  revocation, silence-is-not-approval, and untrusted-content protections.
- Strengthened the contract after an observed El Jefe/Dave deadlock: parent-
  client relays are trusted control context with mandatory precedence over
  generic "agent messages are not consent" rules and historical refusal logs;
  added direct, non-optional relay instructions to El Jefe, Dave, and Kyle.

## 2026-07-28 — Randy (Codex-only test engineer) added

Created Randy, a Codex-only independent test engineer derived from Kyle's
read-only testing role. Randy writes and executes development, integration,
user, and security test plans; produces failed-case handoffs with suggested
fixes; and maintains per-project regression history under `../testing/`.
Project repositories and all Git/GitHub access remain strictly read-only, and
Randy never commits or implements code.

## 2026-07-17 — Nell (legal adviser) added

Created Nell, the team's legal adviser. She reviews and advises on IP,
advertising/marketing, privacy/data protection, app store guidelines, ToS/EULAs,
NDAs, jurisdictions, and accessibility compliance. She verifies every claim
against authoritative sources; never invents legal precedent, cases, or laws;
declines unverifiable questions. Created `nell.md`, `nell-knowledge.md`
(persistent legal knowledge), and the `legal-compliance` skill (seven-domain
framework). Nell is invocable by other agents (Steve, Uma, Diego) for legal
review of their work, and by the human owner directly.

## 2026-07-17 — Skill extraction + task tiering

Refactored the agent roster to separate intrinsic behavior from on-demand
capability, so simple tasks stop paying the cost of the full workflow.

### Added
- `skills/` — source-of-truth for on-demand capabilities (symlink into
  `.claude/skills/` or `~/.claude/skills/`; see `agents/README.md`):
  - `user-guide-quality` — user-guide/HTML authoring, validation, review
    checklist, and audience boundary (previously duplicated in Diego, Gary,
    Brenda, El Jefe).
  - `iterative-review` — multi-round review protocol + finding schema
    (previously duplicated in Gary and Debra).
  - `security-architecture` — wraps Steve's capability pack.
  - `ux-architecture` — wraps Uma's capability pack.
  - `system-administration` — Linux/Apache/FastAPI/MariaDB service playbooks
    and a CIS/STIG-aligned hardening checklist (Dave).
  - `badge-development` — shared badge pipeline, gates, catalog states, and
    novelty/criteria/artwork rules (previously spread across 8 badge agents).
- `tasks/TASK_LOGGING.md` — single shared task-logging convention; the
  per-agent copy of the logging template was removed from every agent file.
- `DECISION_ROUTING.md` — **Task tiers (fast-path)** section: Tier 0
  (trivial/direct, one agent self-verifies), Tier 1 (standard, relevant
  reviewers only), Tier 2 (full chain). Tiering shortcuts process, never
  safety gates.

### Changed
- Every agent slimmed to its intrinsic role, authority, boundaries, and output
  location, plus an "On-demand capabilities (skills)" pointer where relevant.
- El Jefe now records a task tier at intake and pulls in only domain-relevant
  reviewers instead of the whole pool.

### Removed
- `dave-capability-pack/` — deleted. Its 18 files were UI-review material that
  contradicted Dave's System Administrator role. Dave now has the correct
  `system-administration` skill instead.

### Flagged (not changed)
- Stray file `agents/uma.` (note trailing dot, no extension) appears to be an
  accidental duplicate of `uma.md`; left in place for the owner to remove.
