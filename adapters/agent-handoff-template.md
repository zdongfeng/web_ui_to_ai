# Agent Handoff Template

Use this template when giving AIUI to a coding agent.

## Instruction

Before writing frontend code, read the AIUI files in this project.

Follow this priority order:

1. Existing project components and conventions
2. AIUI page spec
3. AIUI patterns
4. AIUI brand profile
5. AIUI adapter guidance
6. General frontend judgment

## Rules

- Do not invent a different page structure unless the AIUI spec is incomplete.
- Do not use marketing layouts for product pages.
- Do not use repeated decorative card grids unless the pattern asks for them.
- Keep density, spacing, and hierarchy consistent with the brand profile.
- Prefer practical product UI over decorative UI.
- Preserve existing codebase patterns when available.
- Ask for clarification only if a required region or primary user goal is missing.

## Expected Output

Implement the requested page according to:

```text
.aiui/project.aiui.yaml
.aiui/page.aiui.yaml
.aiui/tokens.aiui.yaml
```

If the framework adapter conflicts with existing project conventions, follow the project conventions and explain the difference.

