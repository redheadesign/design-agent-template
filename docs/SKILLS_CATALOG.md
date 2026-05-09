# Skills Catalog

Each skill should be easy to understand before someone opens the raw `SKILL.md`.

Open the visual catalog at `docs/skills/index.html`.

## Source Of Truth

Use `.cursor/skills/manifest.json` as the public catalog index. Each entry should describe:

- What the skill does.
- When to use it.
- Where the local `SKILL.md` lives.
- Which official resources explain the underlying tool.
- Which image or preview should be used in a visual catalog.

## Bento Card UI

The catalog renders each skill as a bento card from the manifest:

- Title and category.
- Short outcome-focused summary.
- Four common use cases.
- Official links.
- Preview image or product screenshot.

The important part is that the content stays in `manifest.json`, so adding a new skill automatically gives the catalog enough metadata to render a card.

## Adding A New Skill Card

1. Add the skill under `.cursor/skills/<skill-name>/SKILL.md`.
2. Add a matching entry to `.cursor/skills/manifest.json`.
3. Add an optional preview image under `docs/assets/skills/`.
4. Keep descriptions beginner-friendly and focused on the outcome, not internal implementation details.

## Current Skills

### Lazyweb

Lazyweb is for real product UI references: pricing pages, onboarding, paywalls, dashboards, settings screens, app flows, and design comparisons.

Official setup: https://www.lazyweb.com/mcp-install
