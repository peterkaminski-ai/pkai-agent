# pkai-agent

A starter kit for your own personal AI agent — a persistent, file-based companion you talk to through Claude Code.

This repo is a template. You download it, open it in Claude Code, and on first run your new agent will introduce itself, ask what to call it, and offer to walk you through the rest of the PKAI setup if you want.

## What you get

- **A genericized persona** at `CLAUDE.md`. It's the same shape as the personal agents some PKAI members already run (Freya, Ava), but stripped of person-specific content so it can become yours.
- **A memory system** at `memory/`. Plain markdown files. Your agent reads `memory/MEMORY.md` at the start of every session and writes new memories as you teach it things.
- **Working directories** for inbox, outbox, sessions, schedule, and briefings. Use what you need; ignore what you don't.
- **`pkai-starter/`** — embedded copies of four PKAI starter wikis:
  - `getting-started/` — Claude Code, Obsidian, Git, GitHub from scratch
  - `git-guide/` — version control without the jargon
  - `obsidian-reference/` — useful settings, plugins, and patterns
  - `project-management/` — how to actually work with an AI agent on real projects

## How to start

1. Clone or download this repo to somewhere you'll remember — e.g. `~/Documents/GitHub/pkai-agent/`.
2. Open the directory in Claude Code (`cd ~/Documents/GitHub/pkai-agent && claude`) — or open it as an Obsidian vault and use the [Obsidian Claude Sidebar plugin](https://github.com/peterkaminski/obsidian-claude-sidebar).
3. Say hi. Your agent will run its first-run introduction and take it from there.

## After first run

Your agent will offer to rename this directory to `<your-name>-hq` — e.g. `alex-hq` if you gave a first name, or `alex-rivera-hq` if you gave a full name. That's the PKAI convention for "this vault is my agent's home, and the agent works for me." You can also leave it as `pkai-agent` indefinitely — the agent doesn't care, only humans read directory names.

If you spin up additional agents later, the recommended pattern is a sibling vault — `~/Documents/GitHub/alex-hq/`, `~/Documents/GitHub/other-agent/`, etc. — one Obsidian vault per agent, one git repo per agent, separate memory per agent.

## License

This template and everything in it — including the embedded starter wikis under `pkai-starter/` — is licensed under the [Mozilla Public License 2.0](LICENSE.md), © 2026 Peter Kaminski. See `LICENSE.md` for the full text, including the Disclaimer of Warranty (Section 6) and Limitation of Liability (Section 7).
