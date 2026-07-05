# avalanche-video-marketplace

A Claude **plugin marketplace** for Avalanche brand video generation (plugin v2.1.0 — 2026 brand guidelines, script-first pipeline, @element continuity system).

## Repo structure (this folder = repo root, single `main` branch)
```
avalanche-video-marketplace/
├── .claude-plugin/marketplace.json   ← marketplace catalog (HIDDEN folder)
├── plugins/avalanche-video/          ← the plugin
└── README.md
```
Reveal the hidden `.claude-plugin` folder in Finder with **Cmd + Shift + . (period)**.

## Install (Claude Code / Cowork)
```
/plugin marketplace add simondoesart/avalanche-video-marketplace
/plugin install avalanche-video@avalanche-video-marketplace
/reload-plugins
```
Connect the **Higgsfield** MCP when prompted (each editor uses their own Higgsfield login), then run `/avalanche-video:make-video`.

## Updating
Edit files here → commit → push to `main`. This repo has exactly one branch; the marketplace root is the repo root. Bump the version in both `plugins/avalanche-video/.claude-plugin/plugin.json` and `.claude-plugin/marketplace.json` when shipping changes.
