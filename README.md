# ECC

This repo has the [ECC](https://github.com/affaan-m/ECC) Claude Code plugin properly installed at **project scope** via the `claude plugin` CLI — the same outcome as running `/plugin marketplace add` + `/plugin install ecc@ecc` interactively, but done through the CLI since the `/plugin` slash command isn't available in Claude Code on the web.

## How it works

`.claude/settings.json` declares the marketplace and the enabled plugin:

```json
{
  "enabledPlugins": { "ecc@ecc": true },
  "extraKnownMarketplaces": {
    "ecc": { "source": { "source": "git", "url": "https://github.com/affaan-m/ECC.git" } }
  }
}
```

Anyone who opens this repo in Claude Code gets the `ecc` marketplace and the `ecc@ecc` plugin automatically — 286 skills, 68 agents, 97 commands, rules, and hooks (7 hook types: PreToolUse, PreCompact, SessionStart, PostToolUse, PostToolUseFailure, Stop, SessionEnd). The actual plugin package is fetched and cached locally by Claude Code on each machine (like `node_modules` for `package.json`) — nothing bulky is committed to this repo.

## Hook profile

The plugin's hook automation profile (`off` / `minimal` / `standard` / `strict`) is **personal, per-machine configuration** — it doesn't travel with the repo. Set yours with:

```
claude plugin install ecc@ecc --config hook_profile=standard
```

(`standard` is the default if you don't set anything.)

## Source

https://github.com/affaan-m/ECC (MIT licensed), v2.2.0.
