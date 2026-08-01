# AI-Wonder-Team — Global Agent Roster

> **Shared decision routing:** Every agent follows [DECISION_ROUTING.md](DECISION_ROUTING.md). Task prompts must declare `Decision mode: autonomous` or `Decision mode: interactive`; when omitted, the mode defaults to `interactive`. That file also defines **task tiers (0/1/2)** so simple, bounded work can skip the full delegate→implement→test→review chain — El Jefe records a tier before delegating.
>
> **Human approvals:** Fat Cat may approve work in the active Codex or Claude
> conversation. The client/coordinator's relay of that approval is authoritative
> for agents. No direct agent conversation, Git commit, changed approval file,
> or Claude/Codex-specific messaging mechanism is required. See
> [DECISION_ROUTING.md](DECISION_ROUTING.md) for scope and trust boundaries.
> Its relay section has mandatory precedence over generic rules that
> agent/coordinator messages cannot convey consent and over contrary historical
> task/story records. A hard gate still requires Fat Cat's approval; it does not
> require an impossible direct conversation with a private subagent.
>
> **Enforcement boundary:** The parent client validates required human approval
> before dispatch. Subagents receive pre-authorized assignments and never audit
> approval provenance. Parent dispatch—not a commit, checkbox, direct subagent
> turn, or special relay phrase—is the execution authority within stated scope.

Generic, project-agnostic subagents shared by Claude and Codex. Each agent
Markdown file here is the source of truth. Run `ruby sync-agent-configs.rb`
after changing an agent to regenerate the client-specific discovery files:

- Claude: `../.claude/agents/<name>.md` symlinks to the canonical Markdown.
- Codex: `../.codex/agents/<name>.toml` contains Codex-native metadata and the
  canonical instructions.
- Exception: Kyle is generated only for Claude; Randy is generated only for
  Codex.

Each agent is a standalone expert (no hardwired reporting chain between
them) — invoke whichever one fits the task at hand.

| Agent | Role | Claude model |
|---|---|---|
| [Dave](dave.md) | System administrator — Linux/SSH, Apache/FastAPI/MariaDB, OS hardening | Sonnet |
| [Steve](steve.md) | Cybersecurity architect — threat modeling, secure design/architecture review | Sonnet |
| [Karla](karla.md) | Hands-on security tester — dependency/SAST/DAST scanning, authorized exploit verification | Sonnet |
| [Derrick](derrick.md) | Security incident responder — triages logs/alerts, writes incident reports and response runbooks | Sonnet |
| [Bisi](bisi.md) | Compliance/audit tracker — maps controls to named frameworks (PCI/HIPAA/SOC 2/etc.), tracks gaps over time | Sonnet |
| [El Jefe](el-jefe.md) | Engineering lead — scopes and delegates bounded task files, reviews diffs | Sonnet |
| [Diego](diego.md) | General-purpose software implementer | Sonnet |
| [Kyle](kyle.md) | Independent test relay — runs tests, relays verdict verbatim, no editing | Haiku |
| [Randy](randy.md) | Codex-only independent test engineer — plans and executes multi-layer testing, tracks defects and regressions, read-only Git/GitHub | Inherit |
| [Ashley](ashley.md) | Social/growth product strategist | Haiku |
| [Debra](debra.md) | Competitive/power-user research analyst | Haiku |
| [Gary](gary.md) | Casual-user UX/copy reviewer (source-only) | Haiku |
| [Fred](fred.md) | Field-ops monitor — crash logs / user reviews dropped into a project | Haiku |
| [Barney](barney.md) | Release-notes / changelog scribe | Haiku |
| [Brenda](brenda.md) | User-facing documentation writer — README/user guides/how-tos, docs only | Haiku |
| [Wilma](wilma.md) | Dependency/platform advisory watcher | Haiku |
| [Uma](uma.md) | UX architect — researches comparable products and architects redesigned flows | Haiku |
| [Nell](nell.md) | Legal adviser — reviews and advises on IP, advertising, privacy, app store guidelines, ToS, NDAs, jurisdictions, accessibility compliance | Sonnet |
| [Badge Team Lead](badge-team-lead.md) | Coordinates cross-project badge-system work and approvals | Sonnet |
| [Badge Source Auditor](badge-source-auditor.md) | Audits live project capabilities before badge design | Sonnet |
| [Badge Researcher](badge-researcher.md) | Researches original, non-duplicative badge concepts | Haiku |
| [Badge Criteria Writer](badge-criteria-writer.md) | Defines deterministic criteria and user descriptions | Sonnet |
| [Badge Artist](badge-artist.md) | Creates final artwork and maintains the visual system | Sonnet |
| [Badge Documentation Curator](badge-documentation-curator.md) | Maintains user docs and the owner administration guide | Haiku |
| [Badge Integration Planner](badge-integration-planner.md) | Produces bounded existing-system implementation handoffs | Sonnet |
| [Badge Publisher](badge-publisher.md) | Validates and promotes production-ready badge records | Sonnet |

Codex agents intentionally omit `model` and `model_reasoning_effort`, so each
inherits the invoking Codex session's model and reasoning settings. Claude uses
the model declared in each canonical Markdown manifest.

## On-demand capabilities (skills)

Task-specific procedures that used to be baked into (and duplicated across)
agent files now live as **skills** — the source of truth is
[`../skills/`](../skills/), one directory per skill with a `SKILL.md`. Agents
carry only their intrinsic role, authority, and boundaries, and load a skill
only when a task actually needs it. This keeps simple tasks fast (agents aren't
wading through a documentation checklist to fix a typo) and keeps shared
procedures in one place instead of copy-pasted per agent.

| Skill | What it covers | Loaded by |
|---|---|---|
| `user-guide-quality` | User-guide / HTML-doc authoring + validation + review checklist; audience boundary | Diego, Gary, Brenda, El Jefe |
| `iterative-review` | Multi-round review protocol + standardized finding schema | Gary, Debra, (Diego responds) |
| `security-architecture` | Steve's capability-pack depth (playbook, knowledge, checklists, templates) | Steve |
| `ux-architecture` | Uma's capability-pack depth (playbook, knowledge, checklists, templates) | Uma |
| `system-administration` | Linux/Apache/FastAPI/MariaDB playbooks + CIS/STIG hardening checklist | Dave |
| `legal-compliance` | Seven-domain legal framework (IP, advertising, privacy, app store guidelines, ToS, NDAs, jurisdictions, accessibility) | Nell |
| `badge-development` | Badge pipeline, gates, catalog-state model, novelty/criteria/artwork rules | Badge Team |
| `dj-agent-sync` | Synchronizes canonical agents into Claude and Codex discovery formats | Parent client / owner |

**Wiring:** skills are source-of-truth in `skills/` and are exposed through
client-specific project discovery paths:

```bash
# Claude project-scoped discovery:
mkdir -p .claude/skills && for d in skills/*/; do ln -sfn "$(pwd)/$d" ".claude/skills/$(basename "$d")"; done
# Codex project-scoped discovery:
mkdir -p .agents/skills && for d in skills/*/; do ln -sfn "$(pwd)/$d" ".agents/skills/$(basename "$d")"; done
```

## Conventions

- **Delegation log:** whenever any agent above takes on work, it logs to
  `/Users/dj/Projects/AI-Wonder-Team/tasks/TASK-<Name>-<n>.md` per the shared
  [tasks/TASK_LOGGING.md](../tasks/TASK_LOGGING.md) convention (incrementing
  `<n>`, checked against existing files) — the per-agent copy of that template
  has been centralized there.
- **Proposal/finding output:** agents that only research and write findings
  (Ashley, Debra, Gary, Fred, Barney, Wilma, Uma, Steve, Karla, Derrick,
  Bisi) write their actual output into the *invoking project's own*
  `proposals/` folder (creating it if needed), not into this shared tree —
  findings are project-specific and belong with that project.
- **Decision routing:** ordinary ambiguity routes to El Jefe under the
  task's declared decision mode. Agents remain independently invocable, and
  safety, authorization, and role boundaries remain in force.

## Adding a new agent

1. Write `<name>.md` here with standard Claude Code subagent frontmatter
   (`name`, `description`, `tools`, `model`).
2. Add a row to the table above.
3. Run `ruby sync-agent-configs.rb` from this directory. Add the normalized
   agent name to `CLAUDE_ONLY` or `CODEX_ONLY` in that utility only when the
   agent is intentionally client-specific.

## Adding a new skill

1. Create `../skills/<skill-name>/SKILL.md` with `name` and `description`
   frontmatter (the `description` is what tells an agent *when* to load it, so
   make it specific).
2. Symlink it into the discovery path (see wiring above).
3. Reference it from the relevant agent(s) under an "On-demand capabilities
   (skills)" heading — don't inline the procedure back into the agent file.

Rule of thumb for what belongs in a skill vs. an agent: if a block of guidance
is only needed for *certain task types* (documentation, iterative reviews,
badge cycles, deep security/UX work), it's on-demand → skill. If it's needed on
*every* task the agent does (identity, authority, safety boundaries, output
location), it's intrinsic → stays in the agent.
