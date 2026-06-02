# Use AIUI With Claude Code

This guide explains how to use AIUI with Claude Code.

## Recommended Project Setup

Place a `.aiui/` folder in the target project.

```text
.aiui/
  project.aiui.yaml
  tokens.aiui.yaml
  agent-instructions.md
  pages/
    order-management.aiui.yaml
```

## Recommended Claude Code Prompt

```text
Use AIUI as the source of design intent for this frontend task.

Read these files first:

.aiui/agent-instructions.md
.aiui/project.aiui.yaml
.aiui/tokens.aiui.yaml
.aiui/pages/order-management.aiui.yaml

Then implement the requested page.

Important:
- Follow the required patterns and regions.
- Use existing components before creating new ones.
- Keep the UI compact and operational.
- Avoid generic AI UI patterns listed in the page spec.
- If the project conventions conflict with AIUI, explain the tradeoff before implementing.
```

## Good Claude Code Tasks

- Generate a page from AIUI
- Refactor an AI-generated page to follow AIUI
- Convert a product requirement into a draft page spec
- Check whether a page implementation includes the required regions
- Create a new pattern candidate from a repeated UI structure

## Human Review Points

After Claude Code generates a page, human review should check:

- Did it follow the page type?
- Did it include required regions?
- Did it avoid banned generic patterns?
- Did it preserve existing project conventions?
- Did it create unnecessary components?

