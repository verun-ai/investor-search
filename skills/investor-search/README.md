# Investor Search

Build a sourced list of the investors in a market — family offices, VCs, PE firms and
angels — and say honestly how complete it is.

By **BCP partners GmbH** · [bcpp.io](https://www.bcpp.io)

## Install

```
npx skills add verun-ai/investor-search
```

Or copy this folder into `.agents/skills/` in your project, or into `~/.agents/skills/`
to have it everywhere.

## What it does

Ask for the investors in a country, region or sector. You get one Excel file in which each
field records the page it came from.

It works to tell real investors apart from the advisers who sell to them, asks for proof
before treating two entries as the same firm, searches until six rounds in a row find
nothing new, and keeps its working files so a second run continues instead of repeating.

Where it cannot verify something, it records that rather than filling the gap.

## What it needs

A way to search the web, a way to fetch a page, and a shell that can run `python3`.
No account, no API key, no database. If your agent has no web search, the skill says so and
works from fetched pages only — the list will be thinner, and it will tell you that.

Research only — not investment advice.

## Licence

MIT-0. See LICENSE.
