# Brief Ask

Ask Brief a product question. Brief is a product strategy agent that answers from the workspace's decisions, personas, strategy, customers, and competitive landscape.

## Usage

`/brief-ask <question>`

Calls continue the current MCP coding-session conversation by default. Start fresh with `new_conversation: true`, or pass an explicit `conversation_id` as a one-off override that leaves the default in place; fast mode is stateless.

Summarize the returned recommendation and rationale, then finish. Do not save product guidance to local conversation memory.

## Examples

- `/brief-ask What should we prioritize next?`
- `/brief-ask --mode check Should we use Redis for caching?`
- `/brief-ask --mode fast What did we decide about onboarding copy?`

## Modes

- **advise** (default) — Open-ended strategic guidance grounded in your org's data
- **check** — Validate an approach against existing decisions (use before architectural choices)
- **fast** — Sub-2-second response using inline context; best for quick mid-build lookups
