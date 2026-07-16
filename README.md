# Wise Penny — Agent Skill

The `wise-penny` [Agent Skill](https://www.wisepenny.app/help/connect-ai) teaches an AI assistant how to analyze and organize personal or household finances through [Wise Penny](https://www.wisepenny.app) — an MCP server connected **read-only** (via Plaid) to a user's bank accounts.

It covers connecting an assistant, the finance tools (read / organize / sync), the common workflows (review a month, plan, check in, tidy categories), and the safety rules (reads finances, never moves money; confirm destructive edits).

## Install

This skill pairs with the Wise Penny MCP connection — set that up first at
<https://www.wisepenny.app/help/connect-ai>.

The skill is [`SKILL.md`](SKILL.md) at the repo root; its name (`wise-penny`)
comes from the file's frontmatter, not this repo's name. It's also served at
`https://www.wisepenny.app/.well-known/skills/SKILL.md`.

Install steps differ by client, because each looks for skills in a different
place.

### Claude Code

Claude Code loads skills only from `~/.claude/skills/<name>/` (personal) or a
project's `.claude/skills/<name>/`. Clone the repo into one of those, then
restart Claude Code:

```bash
git clone https://github.com/ottowatt/wisepenny-skill ~/.claude/skills/wise-penny
```

Run `git pull` in that folder later to update.

### Claude apps (claude.ai / Claude Desktop)

Zip the skill folder and upload it under **Settings → Features → Skills**
(requires a plan with code execution enabled).

### skills.sh / other agents

```bash
npx skills add ottowatt/wisepenny-skill --skill wise-penny
```

Heads up: this installs into `.agents/skills/`, which **Claude Code does not
read** — for Claude Code, use the `git clone` step above instead.

## License

MIT
