# Adding Skills And Rules

Use skills for reusable workflows and rules for persistent project guidance.

## Skills

Put project-local skills here:

```text
.cursor/skills/<skill-name>/SKILL.md
```

Use skills for actions the agent should intentionally invoke, such as design research, screenshot review, Figma workflows, or repeatable audits.

Keep each skill focused:

- When to use it.
- What inputs it needs.
- What tools or files it should inspect.
- What output format is expected.

Then add a public-facing entry to `.cursor/skills/manifest.json`. This keeps the repository understandable for people who want a visual catalog instead of reading every `SKILL.md`.

The visual catalog lives at `docs/skills/index.html`. If the skill has a preview, place a video, SVG, or image in `docs/assets/skills/` and reference it from the manifest.

## Rules

Put project rules here:

```text
.cursor/rules/<rule-name>.mdc
```

Use rules for guidance that should shape most answers in the workspace: design workflow, accessibility standards, token usage, security, or repository conventions.

Rules should be short, actionable, and scoped with frontmatter:

```markdown
---
description: Short description
alwaysApply: true
---

# Rule Title

- Do the important thing.
- Avoid the risky thing.
```

## Maintenance

- Keep reusable guidance generic enough for new projects.
- Move project-specific details into project docs instead of the base template.
- Do not put secrets, private links, or customer data in skills or rules.
- Prefer a new focused rule over a long mixed rule.
