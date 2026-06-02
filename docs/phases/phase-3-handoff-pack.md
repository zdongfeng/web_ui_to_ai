# Phase 3: Agent Handoff Pack

## Goal

Make AIUI usable inside real AI coding workflows.

## Handoff Structure

The output pack should look like:

```text
.aiui/
  project.aiui.yaml
  tokens.aiui.yaml
  page.aiui.yaml
  agent-instructions.md
  examples/
```

## Agent Instruction Requirements

The instruction file should tell the AI agent:

- Read AIUI files before editing frontend code
- Use existing project components first
- Follow AIUI page structure
- Do not invent unrelated visual patterns
- Respect density, layout, and brand profile
- Ask only when the spec is incomplete
- Keep implementation framework-specific decisions inside the adapter

## First Adapter

The first adapter is React + Tailwind.

It should explain:

- How to map tokens to Tailwind classes
- How to interpret component specs
- How to structure page regions
- How to avoid common AI UI mistakes

## Deliverables

- `adapters/agent-handoff-template.md`
- `adapters/react-tailwind-adapter.md`
- Example page specs in `examples/`

## Exit Criteria

A developer can give the handoff pack to Codex or Claude Code and get a page that follows the AIUI structure.

