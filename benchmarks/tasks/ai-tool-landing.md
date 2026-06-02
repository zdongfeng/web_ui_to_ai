# Benchmark Task: AI Tool Landing Page

## User Requirement

Build a landing page for an AI developer tool.

Users need to:

- Understand what the product does
- See the workflow
- Trust that it works with coding agents
- Start a trial

## Direct Prompt

```text
Build a landing page for an AI developer tool.

It should explain the product, show the workflow, include proof points, pricing preview, and a final call to action.
Make it beautiful and modern.
```

## AIUI-Assisted Prompt

```text
Build a landing page for an AI developer tool.

Before writing code, read the AIUI page spec:

examples/ai-tool-landing-page.aiui.yaml

Also follow:

adapters/agent-handoff-template.md
adapters/react-tailwind-adapter.md

Avoid generic purple AI gradients, identical icon-card feature grids, fake dashboard screenshots, and empty AI buzzword copy.
```

## Expected Pattern

- landing-page
- product-proof
- workflow-section
- pricing-preview
- final-action

## Things To Watch

- Does the page avoid generic AI startup visuals?
- Does the hero communicate the product clearly?
- Does the workflow section feel specific?
- Does the page have enough brand character without becoming decorative?

