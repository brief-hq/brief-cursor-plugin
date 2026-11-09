# Brief — Cursor Plugin

**Brief is a product strategy agent that answers from the workspace's decisions, personas, strategy, customers, and competitive landscape.**

Published by **Brief Labs Inc.**

This repository contains Brief's full plugin bundle for [Cursor](https://cursor.com/): MCP configuration, a project-aware rule, skills, and slash commands.

## Install

### One-click deep link

Paste this URL into your browser to install Brief's MCP server in Cursor:

```text
cursor://anysphere.cursor-deeplink/mcp/install?name=brief&config=eyJ1cmwiOiJodHRwczovL2FwcC5icmllZmhxLmFpL21jcCIsInR5cGUiOiJodHRwIn0%3D
```

This installs only the MCP server. Rules, skills, and commands require the full plugin bundle described below.

### Full plugin bundle (local testing)

Brief's Cursor Marketplace listing has not been verified yet. Cursor documents marketplace installation and [local plugin testing](https://cursor.com/docs/plugins#test-plugins-locally), rather than a general install-from-GitHub flow for an individual plugin.

To review the full bundle locally:

1. Download the files from the [public repository](https://github.com/brief-hq/brief-cursor-plugin), or use this checkout for unshipped changes.
2. Create `~/.cursor/plugins/local/brief` and copy the plugin contents into it, including `.cursor-plugin/plugin.json`. Copy the files; Cursor skips symlinks pointing outside its local plugins folder.
3. Restart Cursor or run **Developer: Reload Window**.
4. Open **Customize** and confirm the bundled components appear. Local plugin imports must be allowed; Enterprise admins control this setting.

The bundle contains:

- `mcp.json` — Brief MCP server at `https://app.briefhq.ai/mcp`
- `rules/brief-context.mdc` — always-applied rule that tells Cursor's agent to check Brief for product context before architectural decisions
- `skills/brief/` — the Brief MCP reference skill, auto-invoked when a task matches its description
- `commands/brief-onboard.md` and `commands/brief-ask.md` — `/brief-onboard` and `/brief-ask` slash commands

## Authenticate

Cursor uses its native OAuth flow (DCR + PKCE + refresh, shipped in Cursor 2.5+) to authenticate with Brief. On first connect Cursor opens a browser to sign in; tokens refresh automatically after that — no shell env vars, no CLI token export.

The Brief server appears under **Cursor Settings → Tools & MCP**. If it ever shows "Logged out," click **Sign in** to re-trigger OAuth.

## Contents

| Path | Purpose |
|---|---|
| `.cursor-plugin/plugin.json` | Cursor plugin manifest |
| `mcp.json` | MCP server endpoint (OAuth handled natively by Cursor) |
| `rules/brief-context.mdc` | Always-applied project rule |
| `skills/brief/SKILL.md` | Brief MCP reference skill |
| `commands/brief-ask.md` | `/brief-ask` slash command |
| `commands/brief-onboard.md` | `/brief-onboard` slash command |
| `assets/logo.png` | Brief plugin logo |

## Links

- [Brief](https://usebrief.com)
- [Setup](https://usebrief.com/docs/mcp-setup/)
- [Support](https://usebrief.com/support/) · support@briefhq.ai
- [Privacy](https://usebrief.com/privacy-policy/)
- [Terms](https://usebrief.com/terms-of-service/)
- [Cursor plugins](https://cursor.com/docs/plugins)
- [Cursor plugin reference](https://cursor.com/docs/reference/plugins)
- [Cursor MCP install links](https://cursor.com/docs/mcp/install-links)

## License

ISC — see [LICENSE](./LICENSE).
