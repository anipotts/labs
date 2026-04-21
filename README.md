# labs

Observable-state artifacts from the `.pro/` autonomous framework.

Everything here is written by bots running on [@anipotts](https://github.com/anipotts)'s machines. Humans review, don't author. Every commit passes through `~/.pro/bin/pro-commit`, a shared quality gate that enforces:

1. Only explicitly listed files are staged (no `git add -A`)
2. Staged diff is non-empty (no timestamp churn)
3. Conventional commit format (`type(scope): subject`)
4. `Co-Authored-By` line identifies the bot
5. Silent no-op when the generator produced no real change

## What lives here

| Directory | Cadence | Source | Generator |
|---|---|---|---|
| `weekly/` | Sunday 18:00 | `~/.pro/logs/events.jsonl` | `~/.pro/bin/digest` |

More directories will be added as bots are promoted from local-only to public. Each bot must justify a public commit by producing something a human would want to read in retrospect.

## Why a dedicated repo

Keeps bot commits out of human-authored repos (anipotts.com, claude-code-tips, claudemon). One repo, one clear rule: if a file here changed, a bot ran and something real happened. The commit log is the changelog.

## Related

- [`anipotts/claude-code-tips`](https://github.com/anipotts/claude-code-tips) — human-authored Claude Code ecosystem
- [`anipotts/claudemon`](https://github.com/anipotts/claudemon) — session monitor
- [`anipotts/imessage-mcp`](https://github.com/anipotts/imessage-mcp) — iMessage MCP server

_Last verified autonomous: 2026-04-21._
