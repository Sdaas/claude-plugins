# sdaas — Claude Code plugin marketplace

The **release channel** (umbrella marketplace) for Soumendra Daas's Claude Code plugins. Each plugin
lives in its own repository and is published here pinned to a released **git tag** — so installing from
this marketplace always gives you a specific, reproducible version, never a moving target.

## Install

```bash
claude plugin marketplace add Sdaas/claude-plugins
claude plugin install sdlc-lite@sdaas
```

Then, inside a Claude Code session, run the plugin's commands (e.g. `/implement-feature`). See the
plugin's own repo for setup prerequisites (a real user must install its Python toolchain into their
environment first).

## Plugins

| Plugin | What it does | Source |
|---|---|---|
| **`sdlc-lite`** | Interview-driven, test-first, human-in-the-loop workflow that builds a reviewed, tested, committed Python feature via a conductor + isolated, model/effort-pinned subagent gates. | [`Sdaas/sdlc-lite`](https://github.com/Sdaas/sdlc-lite) (tag-pinned) |

## Why an umbrella marketplace?

A Claude Code marketplace maps to **one repository**, but these plugins live in **separate repos** (each
is independently versioned and released). This umbrella catalog aggregates them behind a single
`marketplace add`, so you add one marketplace and can install any of them.

> **Install from _here_, not from a plugin's own repo.** Adding a product repo directly
> (e.g. `marketplace add Sdaas/sdlc-lite`) would give you an **unpinned, live** checkout of its default
> branch. This umbrella pins each plugin to a released tag — that's the supported path.
