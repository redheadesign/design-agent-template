# Design Agent Template

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
- `.cursor/rules/design-workflow.mdc`: persistent agent guidance for design tasks.
- `.cursor/rules/security-and-secrets.mdc`: persistent guidance for keeping local tokens out of Git.
- `.cursor/mcp.example.json`: safe MCP template for Lazyweb setup.
- `.cursor/skills/manifest.json`: beginner-friendly metadata for a future visual skills catalog.
- `docs/`: workflow notes for subagents, GitHub, skills catalog, and adding more skills or rules.

## Local Files Vs Public Template

`.cursor/mcp.json` is intentionally ignored because it can contain local bearer tokens. Keep real credentials there only on your machine. Commit `.cursor/mcp.example.json` instead.

## Lazyweb Token

Lazyweb provides a free no-billing MCP token through the one-click installer:

```text
https://www.lazyweb.com/mcp-install
```

An agent can open that setup page during project bootstrap, copy the generated bearer token into ignored local config, and then verify `lazyweb_health` and `lazyweb_search`.

## Recommended Use

Use this folder as the first layer of a design agent workspace. Add project-specific docs, Figma notes, screenshots, and rules as a project grows. Keep reusable guidance in `.cursor/rules/` and reusable slash workflows in `.cursor/skills/`.

For design research, ask the agent to use Lazyweb when you need pricing page references, onboarding examples, paywalls, dashboards, settings screens, app flows, or comparisons against real products.

## GitHub Safety

Before publishing, always check:

```bash
git status --ignored
git diff -- . ":(exclude).cursor/mcp.json"
```

Do not commit `.cursor/mcp.json`, `.env`, tokens, private screenshots, customer data, or private Figma exports.
