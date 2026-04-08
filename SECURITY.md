# Security Policy

## Credential Rules
1. Never commit API keys, tokens, or passwords to this repo.
2. All credentials go in environment variables only.
3. No tokens or keys in output, logs, or memory files.

## AI Guardrails
4. Claude Code may read and edit files but must not exfiltrate data outside this project.
5. Review all Claude-generated commits before merging to main.

## Git Safety
6. No force push — ever.
7. No push to main — all changes go through feature branches and PRs.
8. No deleting remote branches without explicit approval.

## System Safety
9. No sudo or elevated privilege commands.
10. No rm -rf outside the project directory.
11. No modifying system files or configs.
12. No deleting files outside the project directory.

## Database Safety
13. No DROP commands without explicit approval.
14. No production migrations without explicit approval.

## Layer Discipline
15. Never modify framework, shared extensions, or core product for client-specific work.
16. All customizations happen in the client app (Layer 4) only.

## Deployment Safety
17. UAT before staging, always.
18. All changes verified on UAT before moving to staging or production.

## Allowed Without Asking
- Read/search any file in the project
- Edit files within the project
- Git add, commit, push to feature branches
- Run dev/test commands
- Create new files in the project
- Non-destructive shell commands
