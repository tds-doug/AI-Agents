# 17 — Implementation Guide (for the human supervisor, DJ)

1. **Install.** Copy this directory to
   `/Users/dj/Projects/AI-Wonder-Team/agents/uma-capability-pack/` and replace
   the body of `agents/uma.md` with `14-improved-agent-instructions.md`.
   Commit both; the pack is designed to live in git.
2. **Confirm assumptions.** Review A-1…A-5 in file 01 and gates G1–G5 in
   file 02. Edit file 14 if your authority model differs (e.g., no PR rights
   at all → delete the G2/D4 paths). This is the only step where editing 14
   is expected.
3. **Wire the environment.** Create `evidence/`, `lessons/approved/`,
   `lessons/candidates/`, `project-notes/`, and an empty `CHANGELOG.md` next
   to the pack. Ensure Uma's GitHub credentials can push only `uma/*`
   (branch-protection rules on main + a ruleset restricting branch creation
   patterns, if your plan supports it).
4. **Seed project notes.** Add product name(s), min OS targets, design-system
   location, and any intentional nonstandard patterns — this kills a whole
   class of false-positive findings on day one.
5. **Run the ramp.** Follow file 18. Do not grant branch/PR authority (G2
   eligibility) until the exam is passed at ≥ 85 with zero automatic failures.
6. **Operate.** Spot-check per the level table in file 13. Approve/deny gates
   in writing (a one-line reply with the gate ID is enough — it just has to be
   quotable).
7. **Maintain.** Quarterly refresh task (file 15, next 2026-10-12): the
   [VERSIONED] sections of file 05 and the source register are the only parts
   expected to decay quickly.
