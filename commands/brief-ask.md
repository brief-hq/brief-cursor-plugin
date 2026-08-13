# Brief Ask

Ask Brief a product question. Brief is your Product Navigator — it knows business context that code alone can't tell you.

## Usage

`/brief-ask <question>`

Calls continue the current MCP coding-session conversation by default. Start fresh with `new_conversation: true`, or pass an explicit `conversation_id` as a one-off override that leaves the default in place; fast mode is stateless.

## Examples

- `/brief-ask What should we prioritize next?`
- `/brief-ask --mode check Should we use Redis for caching?`
- `/brief-ask --mode fast What did we decide about onboarding copy?`

## Modes

- **advise** (default) — Open-ended strategic guidance grounded in your org's data
- **check** — Validate an approach against existing decisions (use before architectural choices)
- **fast** — Sub-2-second response using inline context; best for quick mid-build lookups
