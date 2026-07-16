# Wise Penny — Agent Skill

The `wise-penny` [Agent Skill](https://www.wisepenny.app/help/connect-ai) teaches an AI assistant how to analyze and organize personal or household finances through [Wise Penny](https://www.wisepenny.app) — an MCP server connected **read-only** (via Plaid) to a user's bank accounts.

It covers connecting an assistant, the finance tools (read / organize / sync), the common workflows (review a month, plan, check in, tidy categories), and the safety rules (reads finances, never moves money; confirm destructive edits).

## Install

The skill pairs with the Wise Penny MCP connection — set that up first at
<https://www.wisepenny.app/help/connect-ai>.

Via [skills.sh](https://skills.sh):

```bash
npx skills add ottowatt/wisepenny-skill --skill wise-penny
```

The skill is [`SKILL.md`](SKILL.md) at the repo root — its name (`wise-penny`) comes from the file's frontmatter, not this repo's name. The same skill is also served at `https://www.wisepenny.app/.well-known/skills/SKILL.md`.

## License

MIT
