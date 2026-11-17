# Changelog

## 1.0.4 — 2026-11-17

- BRI-9721: Stop collecting and uploading repository data at session start or when Brief has no context. `/brief-onboard` now shows a bounded project summary (README, tech stack, recent-work themes; no contributors or issues) and sends it only after the user confirms.
- Write product context and other Brief data only for work the user requested or approved; no silent inferred updates. `brief_ask` questions are unchanged.

## 1.0.3 — 2026-11-10

- Update the rule, skill, and commands to current Brief product strategy wording.
- Use MCP onboarding and reconnect guidance, and finish Ask after summarizing its answer, matching the public Claude plugin.
- Document workspace permissions and the advertised MCP tools.

## 1.0.2 — 2026-11-08

- BRI-9091: Update Brief Labs Inc. branding, product strategy positioning, and public links; distinguish MCP deep-link setup from full-bundle local testing while marketplace review is pending.

## 1.0.1 — 2026-11-04

- BRI-2576: Route named workspace reads and writes through separate MCP tools.

## Unreleased

- Document default MCP Ask continuity and opt-in decision isolation through the
  returned `coding_session_key`.

## 1.0.0 — 2026-04-19

- Initial public release: `brief` plugin for Cursor's marketplace with rule (`rules/brief-context.mdc`), skill (`skills/brief/SKILL.md`), `/brief-ask` and `/brief-onboard` commands, and MCP server at `https://app.briefhq.ai/mcp`.
