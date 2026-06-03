# OpenClaw all-in-one backup

This repository backs up the safe, portable parts of the OpenClaw setup in one place:

- sanitized OpenClaw config: `backup/openclaw.sanitized.json`
- main workspace snapshot: `backup/workspace-main/`
- SharkZap workspace snapshot: `backup/workspace-sharkzap/`
- safe agent metadata/models/skills under `agents/`

Excluded on purpose:

- credentials, tokens, auth directories, Telegram/WhatsApp session state
- runtime sessions/transcripts/logs/SQLite databases
- npm/cache/media/generated artifacts
- nested `.git` metadata from workspaces

Before pushing to GitHub, keep the repo private unless Shark explicitly wants it public.
