# AIUI Agent Instructions

Read these instructions before writing frontend code.

## Priority

Follow this order:

1. Existing project components and conventions
2. `.aiui/project.aiui.yaml`
3. Relevant page spec in `.aiui/pages/`
4. `.aiui/tokens.aiui.yaml`
5. React + Tailwind adapter guidance
6. General frontend judgment

## Core Rules

- Use the page spec to decide structure before writing JSX.
- Use existing project components when they exist.
- Keep product pages practical and task-focused.
- Do not turn product pages into marketing pages.
- Do not add decorative sections that are not requested by the page spec.
- Do not use generic AI visual cliches such as purple gradients, glass panels, and identical feature-card grids.
- Keep responsive behavior in mind for mobile and desktop.
- If the spec is incomplete, make the smallest reasonable assumption and state it.

## Implementation Flow

1. Identify page type.
2. Identify required patterns.
3. Identify required regions.
4. Map recommended components to project components.
5. Implement regions in order.
6. Check avoid rules before finishing.

