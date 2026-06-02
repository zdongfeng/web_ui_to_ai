# Use AIUI With Codex

This guide explains how to use AIUI when asking Codex to build frontend pages.

## Recommended Project Setup

Place a `.aiui/` folder in the target project.

Use `templates/project-aiui/` as the starter structure.

```text
.aiui/
  project.aiui.yaml
  tokens.aiui.yaml
  agent-instructions.md
  pages/
    order-management.aiui.yaml
```

## Recommended Codex Prompt

```text
Before editing files, read:

.aiui/agent-instructions.md
.aiui/project.aiui.yaml
.aiui/tokens.aiui.yaml
.aiui/pages/order-management.aiui.yaml

Implement the order management page according to AIUI.

Follow the page structure, patterns, recommended components, density, brand profile, and avoid rules.
Use existing project components first.
Do not turn this product page into a marketing page.
```

## What To Ask Codex To Do

Good tasks:

- Implement a page from an AIUI page spec
- Adapt an existing page to match AIUI
- Extract missing project tokens into `.aiui/tokens.aiui.yaml`
- Compare current implementation against AIUI structure
- Add a new page spec based on an existing AIUI pattern

Avoid asking Codex:

- To invent the whole AIUI standard alone
- To decide final design taste without human review
- To run visual judging as part of v0.1

## Expected Codex Behavior

Codex should:

- Read the AIUI files before implementation
- Inspect existing project components
- Implement the page through explicit regions
- Keep design choices consistent with the brand profile
- Explain any deviation from the AIUI spec

