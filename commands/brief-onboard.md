# Brief Onboard

Load Brief product context for this project. If Brief has none yet, send it a short project summary that the user has seen and confirmed.

## Steps

1. Call `brief_get_onboarding_context` (MCP)
   to load what Brief already knows about this project — product strategy,
   personas, active decisions, recent work, and velocity.

2. If Brief already has context for this project, summarize it for the user and stop. Send nothing.

3. If Brief has no context yet, draft a short summary from these local sources only:
   - **What this project is** — a 2-sentence summary of README.md
   - **Tech stack** — languages and main frameworks from package.json / requirements.txt / go.mod / Cargo.toml
   - **Recent work** — 3 to 5 themes from `git log --oneline -20`, without commit hashes, author names, or email addresses

   Do not include contributor lists, issue contents, secrets, environment files, or source code.

4. Show the user the exact summary and explain that Brief will use it to create product context and seed features in their workspace. Send it only after the user confirms:
   `brief_ask({ question: "What should I know before building?", context: "[confirmed summary]", onboarding: true })`

5. Brief will respond with product context and its first insight.

## Usage

`/brief-onboard`
