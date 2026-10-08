# Investor Search

[![skills.sh](https://skills.sh/b/verun-ai/investor-search)](https://skills.sh/verun-ai/investor-search)

Build a sourced list of the investors in a market — family offices, VCs, PE firms and
angels — and say honestly how complete it is.

By **BCP partners GmbH** · [bcpp.io](https://www.bcpp.io)

## Install

```
npx skills add verun-ai/investor-search
```

One command. The `skills` CLI detects the agents on your machine and installs into each
one's own skills folder. It knows 78 agents — among them Cline, Windsurf, OpenHands,
Continue, Kilo Code, Qwen Code, Trae, Goose, Warp, Zed, Replit, Droid, Amp, Junie,
Kiro CLI, Rovo Dev, OpenCode, Codex, GitHub Copilot and Claude Code.

No CLI? Copy `skills/investor-search/` into `.agents/skills/` in your project, or into
`~/.agents/skills/` to have it available everywhere.

## What it does

Ask for the investors in a country, region or sector. You get **one Excel file** in which
each field records the page it came from.

- Tells real investors apart from the advisers, banks and consultancies that sell to them
- Reports family offices as **two counts — proven and likely** — never one flattering number
- Asks for proof before treating two entries as the same firm
- Searches until six rounds in a row find nothing new, then says why it stopped
- Keeps its working files, so a second run continues instead of repeating the first

Where it cannot verify something, it records that rather than filling the gap.

## What it needs

A way to search the web, a way to fetch a page, and a shell that can run `python3`.
No account, no API key, no database.

If your agent has no web search, the skill says so in its first reply and works from
fetched pages only — the list will be thinner, and you will be told that rather than
left to assume it is complete.

Research only — **not investment advice**.

## Notes for some agents

- **Cline** — turn on auto-approve for terminal commands, or you will click Approve on
  every round.
- **Cloud agents** (Replit, Ona, Devin) — the Excel file is written in the agent's
  workspace; download it from there.
- **If a run stops early** — say `continue`. The skill keeps its files and resumes where
  it left off instead of starting over.

## Layout

| Path | What it is |
|---|---|
| `skills/investor-search/SKILL.md` | the rules |
| `skills/investor-search/references/` | lists, reasoning, file layout, report shape |
| `skills/investor-search/scripts/store.py` | the memory store — every write goes through it |

## Other packages

Some agents need their own build, because they deliver files differently or have their own
store. Those are packaged separately — see [bcpp.io](https://www.bcpp.io).

## Licence

MIT-0. See LICENSE.

---

© 2026 BCP partners GmbH · [Privacy](https://www.bcpp.io/investor-search-privacy) · [Terms](https://www.bcpp.io/terms-and-conditions)
