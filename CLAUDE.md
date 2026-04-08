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

## Memory Layer (Required Files)
- `CLAUDE.md` — project brain (this file)
- `SECURITY.md` — safety guardrails
- `HEARTBEAT.md` — daily handoff log (created per project)
- `PRD.md` — full requirements (created per project)

## Hard Rules
- Never rename Select option values via Property Setter — use Translation records
- Patches are for schema migrations only — site config goes in idempotent setup scripts
- Decide the deployment mechanism BEFORE writing code
- Verify test selectors against live API schema — never guess field names
- UAT before staging, always
- Never swallow exceptions silently

## Session Log
<!-- Update this after each working session -->
- 2026-04-08: Initial setup — CLAUDE.md, SECURITY.md created. Builder Protocol adopted. Ready for first project.
