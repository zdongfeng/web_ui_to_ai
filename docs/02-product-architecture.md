# Product Architecture

AIUI is composed of six product modules.

## 1. AIUI Spec

The core specification.

It defines:

- Foundation principles
- Tokens
- Components
- Patterns
- Pages
- Brand profiles
- Rules and anti-patterns

The spec is framework-neutral, but it should be precise enough for adapters to produce useful frontend output.

## 2. Pattern Graph

The pattern graph is the main product advantage.

It describes how pages, patterns, regions, and components relate to each other.

Example:

```yaml
page:
  type: management-list
  uses:
    - app-shell
    - page-header
    - filter-toolbar
    - data-table
    - detail-drawer
```

This prevents AI from assembling pages randomly.

## 3. Handoff Pack

The handoff pack is what developers give to Codex, Claude Code, Cursor, Gemini CLI, or another coding agent.

It should include:

```text
.aiui/
  project.aiui.yaml
  tokens.aiui.yaml
  page.aiui.yaml
  agent-instructions.md
  examples/
```

The handoff pack translates the spec into concrete instructions for a coding agent.

## 4. Adapters

Adapters explain how AIUI should be implemented in a specific stack.

v0.1 should only support:

```text
React + Tailwind
```

Future adapters may include:

- Vue + UnoCSS
- Svelte
- Flutter
- SwiftUI
- HTML + CSS

Adapters should not pollute the AIUI core spec.

## 5. Validate

AIUI Validate checks spec consistency.

It should check:

- Required fields
- Unknown references
- Duplicate names
- Circular dependencies
- Missing tokens
- Page specs without required regions
- Brand profiles without density or color strategy

It should not judge visual beauty in v0.1.

## 6. Project Profiler

Project Profiler is a future module.

It reads an existing project, screenshots, or design notes and generates a project-specific AIUI profile.

This becomes the project's UI memory.

Example:

```yaml
project:
  register: product
  audience: internal-operators

style:
  density: compact
  color_strategy: restrained
  surface_style: flat
  border_strategy: subtle-lines
```

Project Profiler is powerful, but it should not be part of v0.1 unless the core spec is already proven.

