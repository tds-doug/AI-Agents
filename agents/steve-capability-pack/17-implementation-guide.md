# 17 — Implementation Guide (for the human supervisor, DJ)

1. **Install.** This directory is already at
   `agents/steve-capability-pack/`. Replace
   the **body** of `agents/steve.md` (everything below the YAML frontmatter)
   with the body of `14-improved-agent-instructions.md`. **Keep `steve.md`'s
   existing frontmatter unchanged** (`name`, `description`, `tools: Bash,
   Read, Grep, Glob, Write, WebSearch, WebFetch`, `model: sonnet`) — that
   block is what registers Steve as a Claude Code subagent; this pack does
   not add or remove tools. Commit both; the pack is designed to live in git.
2. **Confirm assumptions.** Review A-1…A-6 in file 01 and gates G1–G5 in file
   02. Confirm in particular: whether HITRUST is genuinely in scope for any
   current project (§01 §6 — it's heavyweight and easy to over-scope), and
   whether the SOC 1 vs. SOC 2 distinction (§01 A-4) matches reality for any
   project serving as a subservice organization.
3. **Wire the environment.** The shared `agents/lessons/approved/`,
   `agents/lessons/candidates/`, `agents/project-notes/`, `agents/evidence/`,
   and `agents/tools/` directories already exist on disk (confirmed at
   pack-build time; used by prior packs including Uma's and Dave's). No new
   shared infrastructure needs to be created — Steve's lesson/note entries
   just need the `steve-` filename prefix per §15.
4. **Seed project notes.** For each active project, add a short
   `project-notes/steve-<project>-notes.md`: actual payment-data flow
   (tokenized vs. PAN-touching, for PCI scoping), whether any EU/CA personal
   data or health data is processed (for GDPR/CCPA/HITRUST scoping), and
   deployment target specifics (AWS account structure, iOS min version).
   This prevents Steve re-deriving (or mis-assuming) compliance scope on
   every engagement.
5. **Run the ramp.** Follow file 18. Do not grant G2 authority (recon beyond
   the local read-only checkout) or treat a G3 risk-acceptance recommendation
   as routine until the exam is passed at ≥ 85 with zero automatic failures.
6. **Operate.** Spot-check per the level table in file 13. Approve/deny gates
   in writing (a one-line reply with the gate ID and finding ID is enough —
   it just has to be quotable and attributable).
7. **Maintain.** Quarterly refresh task (file 15, next: **2026-10-17**): the
   [VERSIONED] sections of file 05 and the source register (file 16) are the
   parts expected to decay fastest — NIST, OWASP, PCI SSC, HITRUST, MITRE
   ATT&CK, and the CCPA/CPRA regulatory calendar all have near-term dated
   milestones already on record in this pack worth re-checking specifically.
8. **Coordinate the five-way boundary.** Steve's role charter (file 02)
   assumes Dave, Karla, Bisi, Derrick, and Diego continue to exist with their
   current `agents/*.md` definitions. If any of those roles change
   materially, re-review file 02's shared-responsibilities tables — that's
   the part of this pack most likely to drift out of sync with the rest of
   the team.
