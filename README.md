# ECC

This repo vendors the [ECC](https://github.com/affaan-m/ECC) Claude Code toolkit as project-level configuration under `.claude/`, so Claude Code loads it automatically whenever this repo is opened — no `/plugin` install step needed.

## What's included

- `.claude/skills/` — 286 skills
- `.claude/agents/` — 68 subagents
- `.claude/commands/` — 97 slash commands
- `.claude/rules/` — language/stack-specific rules
- `.claude/ecc-hooks/` — the original `hooks/` and `scripts/` from ECC, vendored **for reference only**. They are **not wired into `.claude/settings.json`** and will not run as-is: they depend on Node dependencies (`npm install` inside `.claude/ecc-hooks/`) and on a `CLAUDE_PLUGIN_ROOT` resolution path designed for a real plugin install. Treat this as source to adapt, not a working feature.
- `.claude/ECC-CLAUDE.md` — ECC's own project instructions, kept for reference
- `.claude/ECC-LICENSE` — ECC's MIT license (attribution for the vendored content)

## Source

Vendored from https://github.com/affaan-m/ECC (MIT licensed), version 2.2.0, on 2026-08-21.

To get updates, re-sync the relevant directories from upstream, or install the plugin normally via `/plugin marketplace add https://github.com/affaan-m/ECC` + `/plugin install ecc@ecc` in an interactive Claude Code CLI session (this only works locally, not in Claude Code on the web).
