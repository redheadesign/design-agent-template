# Design Agent Template

[Русский](README.md) | English

Current version: `v0.2.0`

Cursor workspace template for design-heavy projects: UI research, Figma implementation, Lazyweb references, design reviews, and reusable agent guidance.

## Quick Start

1. Clone or download this folder for a new design project.
2. Get a free Lazyweb MCP token at https://www.lazyweb.com/mcp-install.
3. Copy `.cursor/mcp.example.json` to `.cursor/mcp.json`.
4. Put your local Lazyweb bearer token into `.cursor/mcp.json`.
5. Reload Cursor so MCP servers and local slash skills are discovered.
6. Start design work with the local rules and skills in `.cursor/`.

## What Is Included

- `.cursor/skills/lazyweb/SKILL.md`: local `/lazyweb` skill for UI references, screenshots, onboarding patterns, pricing pages, and design comparisons.
- `.cursor/skills/manifest.json`: beginner-friendly metadata for the visual skills catalog.
- `docs/skills/index.html`: dark-first bento-style skills gallery with RU/EN and theme switching.
- `.cursor/rules/design-workflow.mdc`: persistent agent guidance for design tasks.
- `.cursor/rules/security-and-secrets.mdc`: persistent guidance for keeping local tokens out of Git.
- `.cursor/mcp.example.json`: safe MCP template for Lazyweb setup.
- `docs/`: workflow notes for subagents, GitHub, skills catalog, and adding more skills or rules.

## Visual Skills Catalog

Open `docs/skills/index.html` to see the current skills as bento cards. The catalog starts in Russian and dark mode, includes an English switch, and uses the official Lazyweb video preview.

## Local Files Vs Public Template

`.cursor/mcp.json` is intentionally ignored because it can contain local bearer tokens. Keep real credentials there only on your machine. Commit `.cursor/mcp.example.json` instead.

## Lazyweb Token

Lazyweb provides a free no-billing MCP token through the one-click installer:

```text
https://www.lazyweb.com/mcp-install
```

An agent can open that setup page during project bootstrap, copy the generated bearer token into ignored local config, and then verify `lazyweb_health` and `lazyweb_search`.

## GitHub And GitLab README Languages

GitHub and GitLab do not provide a reliable automatic README language switch. Keep `README.md` as the primary audience language and link to secondary versions such as `README.en.md`.

## GitHub Safety

Before publishing, always check:

```bash
git status --ignored
git diff -- . ":(exclude).cursor/mcp.json"
```

Do not commit `.cursor/mcp.json`, `.env`, tokens, private screenshots, customer data, or private Figma exports.
