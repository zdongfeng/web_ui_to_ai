# Prompt: Generate Page From AIUI

Use this prompt when asking an AI coding agent to implement a page from AIUI.

```text
You are implementing a frontend page using AIUI.

Before editing files, read:

1. .aiui/agent-instructions.md
2. .aiui/project.aiui.yaml
3. .aiui/tokens.aiui.yaml
4. The relevant page spec in .aiui/pages/

Then inspect the existing frontend codebase and identify reusable components.

Implementation rules:

- Follow the AIUI page type, layout, required patterns, and required regions.
- Use existing project components first.
- Keep framework-specific choices inside the current project's conventions.
- Respect the brand profile, density, and avoid rules.
- Do not add decorative sections that are not in the page spec.
- Do not turn product pages into landing pages.
- Do not use generic AI UI cliches such as purple gradients, glass panels, fake metrics, or identical icon-card grids.

After implementation, summarize:

- Which AIUI page spec was used
- Which required regions were implemented
- Which existing components were reused
- Any deviations from AIUI and why
```

