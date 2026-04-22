# Brief — Cursor Plugin

**Brief is your Product Navigator — strategic product context, decision capture, and customer insight for AI coding agents.**

This repository is the Brief plugin for [Cursor](https://cursor.com/). Installing it wires Brief's MCP tools into Cursor's agent, drops a project-aware rule into every conversation, and adds slash commands for the two most common Brief workflows.

## Install

### One-click deep link

Paste this URL into your browser to install Brief's MCP server in Cursor:

```text
cursor://anysphere.cursor-deeplink/mcp/install?name=brief&config=eyJ1cmwiOiJodHRwczovL2FwcC5icmllZmhxLmFpL21jcCIsInR5cGUiOiJodHRwIn0%3D
```

This installs only the MCP server — no rules, skills, or commands. Use the marketplace install below if you want the full bundle.

### Cursor Marketplace (full bundle)

Search for **Brief** in Cursor's marketplace (`Cmd/Ctrl + Shift + P → "Cursor: Marketplace"`). Click install. Cursor will load:

- `mcp.json` — Brief MCP server at `https://app.briefhq.ai/mcp`
- `rules/brief-context.mdc` — always-applied rule that tells Cursor's agent to check Brief for product context before architectural decisions
- `skills/brief/` — the Brief CLI reference skill, auto-invoked when a task matches its description
- `commands/brief-onboard.md` and `commands/brief-ask.md` — `/brief-onboard` and `/brief-ask` slash commands

## Authenticate

Cursor uses its native OAuth flow (DCR + PKCE + refresh, shipped in Cursor 2.5+) to authenticate with Brief. On first connect Cursor opens a browser to sign in; tokens refresh automatically after that — no shell env vars, no CLI token export.

The Brief server appears under **Cursor Settings → Tools & MCP**. If it ever shows "Logged out," click **Sign in** to re-trigger OAuth.

## Contents

| Path | Purpose |
|---|---|
| `.cursor-plugin/plugin.json` | Cursor marketplace manifest |
| `mcp.json` | MCP server endpoint (OAuth handled natively by Cursor) |
| `rules/brief-context.mdc` | Always-applied project rule |
| `skills/brief/SKILL.md` | Brief CLI reference skill |
| `commands/brief-ask.md` | `/brief-ask` slash command |
| `commands/brief-onboard.md` | `/brief-onboard` slash command |
| `assets/logo.png` | Marketplace listing icon |

## Links

- [Brief](https://briefhq.ai)
- [Brief MCP docs](https://briefhq.ai/docs/mcp)
- [Cursor plugin reference](https://cursor.com/docs/plugins/building)
- [Cursor MCP install links](https://cursor.com/docs/context/mcp/install-links)

## License

ISC — see [LICENSE](./LICENSE).
