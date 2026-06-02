# AIUI Vision

## Problem

Many developers are comfortable with backend logic, product logic, data flow, and system architecture, but they do not want to spend much time designing frontend pages.

AI coding agents can generate frontend code quickly, but the result is often visually weak:

- Generic SaaS layouts
- Repeated card grids
- Random gradients
- Weak hierarchy
- Poor spacing rhythm
- Inconsistent component decisions
- Pages that look like demos rather than real product UI

The issue is not that AI cannot write CSS. The issue is that AI usually writes UI without a clear design intent layer.

## Product Positioning

AIUI is a structured UI intent specification for AI coding agents.

It gives AI a shared language for:

- Page type
- Layout structure
- Visual density
- Component composition
- Information hierarchy
- Brand direction
- Interaction expectations
- Anti-patterns to avoid

AIUI sits before code generation.

```text
User requirement
→ AIUI page spec
→ Agent handoff pack
→ Frontend implementation
```

## What AIUI Optimizes

AIUI optimizes for:

- Better first draft UI
- Less design rework
- More consistent pages across agents
- Less dependency on the developer's design taste
- Reusable design knowledge across projects

AIUI does not try to solve all frontend problems.

It does not own:

- Runtime component behavior
- Backend logic
- Full design authoring
- Pixel-perfect Figma parity
- Automatic visual scoring in v0.1

## Core Belief

AI should not be asked to design from a blank page.

It should receive a structured design brief that is:

- Framework-neutral
- Machine-readable
- Human-reviewable
- Project-specific when needed
- Stable enough to be reused by different agents

## Long-Term Ambition

The long-term ambition is for AIUI to become a common UI planning layer for AI coding workflows.

Not by declaring itself a standard on day one, but by proving that the same requirement produces better frontend output when an agent uses AIUI.

