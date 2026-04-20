# Brief Onboard

Load Brief product context for this project.

## Steps

1. Run `brief context` (CLI) or call `brief_get_onboarding_context` (MCP)
   to load what Brief already knows about this project — product strategy,
   personas, active decisions, recent work, and velocity.

2. If Brief has no context yet, gather:
   - **What this project is** — read README.md, write a 2-sentence summary
   - **Tech stack** — check package.json / requirements.txt / go.mod / Cargo.toml
   - **Recent work** — `git log --oneline -20` and summarize themes
   - **Team** — `git shortlog -sn --since="3 months ago"`
   - **Open questions** — TODO.md, CONTRIBUTING.md, open issues

   Send all of this to Brief in one call:
   `brief ask "Here's what I found in this codebase: [context]. What should I know before building?"`

3. Brief will respond with product context and its first insight.

## Usage

`/brief-onboard`
