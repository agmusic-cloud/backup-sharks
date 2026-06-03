# OpenClaw all-in-one backup

This repo backs up the important portable state for SharkMain/SharkZap:

- `backup/workspace-main/`: main agent workspace, including `MEMORY.md` and daily memory files
- `backup/workspace-sharkzap/`: SharkZap workspace/playbooks/prompts
- `backup/runtime-memory/`: OpenClaw runtime memory DB/index files
- `backup/agents/`: agent metadata, models, skills, and recent sessions
- `backup/openclaw.sanitized.json`: OpenClaw config with secrets redacted

Security exclusions:

- raw credentials/tokens/bot tokens/auth dirs
- Telegram/WhatsApp login/session auth state
- npm/cache/media/generated artifacts

Session policy:

- Agent session folders can grow a lot, so this backup keeps the latest 80 session files per agent plus `sessions.json`.
