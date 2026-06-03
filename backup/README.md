# OpenClaw migration backup - Shark ecosystem

This is a migration-grade backup for SharkMain/SharkZap.

Included:

- `workspace-main/`: complete main workspace files, including `MEMORY.md`, daily memory, `AGENTS.md`, `SOUL.md`, `USER.md`, `TOOLS.md`, `HEARTBEAT.md` and local state files.
- `workspace-sharkzap/`: complete SharkZap workspace files, playbooks, prompts, procedures, routing docs and business context.
- `runtime-memory/`: complete OpenClaw runtime memory databases/index files.
- `agents/`: agent metadata, model files, skills and complete copied session folders/transcripts for ecosystem recall.
- `git-bundles/`: portable git history bundles for the two workspaces.
- `config/openclaw.sanitized.json`: OpenClaw config with secret values redacted.

Not included intentionally:

- raw Telegram/WhatsApp auth/session login folders
- raw credentials directory
- npm/cache/media/generated runtime artifacts

Secret policy:

- Procedures, memories and sessions are kept for recall.
- Obvious token/password/private-key values in text/JSON/session files are replaced with `<REDACTED>`.
- Shark plans to reconnect Telegram/WhatsApp and rotate credentials after migration.
