# CLAUDE.md — Kashish

## Who I Am
- Role: CRM Administrator / Product Builder at ISDM (Dhwani RIS)
- Domain: Zoho CRM, Frappe framework, documentation, workflow automation
- Technical level: non-technical — AI handles all code, I handle domain decisions
- Methodology: Builder Protocol (3 personas, 8 phases, AI as execution partner)

## How I Like to Work
- Be concise. Lead with the answer.
- Don't ask me to write or edit code — do it for me.
- When in doubt, ask once, then execute.
- UI for thinking (Phases 0-2), CLI for executing (Phases 3+), GitHub for memory.

## Stack
- Framework: Frappe
- Apps: Custom client apps (not mGrant, not mForm)
- Layer discipline: Never touch framework, shared extensions, or core product — all work happens in the client app (Layer 4)

## Builder Protocol — Operating Rules
- Follow the 8-phase lifecycle: Intent > Plan > Requirements > Tasks > DevPlan > Build > Test > Iterate > Ship
- Config-vs-code must be explicitly decided before writing any code
- Platform order for builds: Branding > Theme > Settings > Roles > Fields > Approvals > Alerts > Dashboards
- One source of truth per config item (fixture OR runtime, never both)
- Translation records for display renames, Property Setter for structural changes only
- Test plan before testing, not after
- Update HEARTBEAT.md at end of every session
- PRD.md is the single source of truth for requirements
- If it can't be handed over through GitHub markdown alone, it's incomplete

## Repo Structure
Multi-client repo. Global files at root, each client in its own folder.

```
/
├── CLAUDE.md
├── SECURITY.md
├── Personal/              ← personal projects
├── Misc/                  ← miscellaneous
├── Clients/
│   ├── Veha/              ← per-client (HEARTBEAT.md, PRD.md, app code)
│   ├── CRISIL/
│   ├── ATMA/
│   └── Landmark/
```

- **Global level (root):** CLAUDE.md, SECURITY.md, shared rules
- **Client level (Clients/\<name\>/):** HEARTBEAT.md, PRD.md, client app code, client-specific config
- **Personal/Misc:** Non-client work

## Superpowers Integration
Superpowers plugin is installed. Use these skills at the right phase:
- **Planning (Phases 0-1):** `superpowers:brainstorming` before any creative/feature work, `superpowers:writing-plans` for multi-step tasks
- **Execution (Phases 3-5):** `superpowers:executing-plans`, `superpowers:subagent-driven-development`, `superpowers:dispatching-parallel-agents`
- **Testing (Phase 6):** `superpowers:test-driven-development`, `superpowers:systematic-debugging`
- **Review (Phase 7-8):** `superpowers:requesting-code-review`, `superpowers:verification-before-completion`
- **Git:** `superpowers:using-git-worktrees` for feature isolation, `superpowers:finishing-a-development-branch` for merge/PR

## Memory Layer (Required Files)
- `CLAUDE.md` — project brain, global (this file)
- `SECURITY.md` — safety guardrails, global
- `Clients/<name>/HEARTBEAT.md` — daily handoff log, per client
- `Clients/<name>/PRD.md` — full requirements, per client

## Environment
- Git + GitHub CLI (gh) — version control, PRs, issues
- Claude Code CLI — primary AI execution tool
- Playwright — E2E testing (plugin installed)
- Frappe bench — when working on client Frappe apps

## Hard Rules
- Never rename Select option values via Property Setter — use Translation records
- Patches are for schema migrations only — site config goes in idempotent setup scripts
- Decide the deployment mechanism BEFORE writing code
- Verify test selectors against live API schema — never guess field names
- UAT before staging, always
- Never swallow exceptions silently

## Session Log
<!-- Update this after each working session -->
- 2026-04-08: Initial setup — CLAUDE.md, SECURITY.md created. Builder Protocol adopted. Repo structured: Personal, Misc, Clients (Veha, CRISIL, ATMA, Landmark). Superpowers integrated.
