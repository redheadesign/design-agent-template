# Subagents

Subagents are useful when a design task has independent workstreams that can run in parallel.

## When To Use Them

Use subagents for:

- UI reference research while the main agent inspects the current project.
- Figma analysis while another agent reviews existing components.
- Competitive research across several flows, such as pricing, onboarding, checkout, and dashboards.
- Code review or QA after a larger design implementation.

Skip subagents for small one-file edits, direct questions, or tasks where the next step depends on one answer.

## Good Requests

Ask for parallel subagents when the scope is broad:

```text
Use subagents in parallel: one for Lazyweb pricing references, one for onboarding examples, and one for checking our current UI patterns.
```

```text
Have a subagent review the implemented design for visual regressions while you continue wiring the page.
```

## Suggested Roles

- `reference researcher`: finds real product examples with Lazyweb.
- `figma analyst`: extracts constraints, hierarchy, and reusable components from Figma.
- `component mapper`: finds existing app components and tokens to reuse.
- `reviewer`: checks risks, missing states, accessibility, and test gaps.

The main agent should synthesize the results and decide what to implement.
