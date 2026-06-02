# Benchmark Task: SaaS Settings Page

## User Requirement

Build a workspace settings page for a SaaS product.

Users need to:

- Update workspace name
- Manage billing email
- Toggle product preferences
- Review security settings
- Access a danger zone

## Direct Prompt

```text
Build a polished SaaS workspace settings page.

It should include workspace profile settings, billing email, preferences, security settings, and a danger zone.
Make it clean and modern.
```

## AIUI-Assisted Prompt

```text
Build a SaaS workspace settings page.

Before writing code, read the AIUI page spec:

examples/saas-settings-page.aiui.yaml

Also follow:

adapters/agent-handoff-template.md
adapters/react-tailwind-adapter.md

Use grouped settings sections and practical product UI. Avoid marketing-style cards, hero headers, and modal-first editing.
```

## Expected Pattern

- app-shell
- settings-section
- optional billing-overview

## Things To Watch

- Does the AI use rows and sections instead of feature cards?
- Are destructive actions visually separated?
- Does the page feel like real software settings?

