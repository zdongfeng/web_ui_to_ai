# Risks and Boundaries

AIUI can easily become too large. This document keeps the product focused.

## Core Risk

The main risk is turning AIUI into a full design platform before proving the spec is useful.

AIUI should first prove:

```text
Structured UI intent improves AI-generated frontend output.
```

Everything else is secondary.

## Risk 1: Becoming A UI Framework

AIUI should not compete with:

- shadcn/ui
- Radix
- Ant Design
- Material UI
- Tailwind
- React Aria

Boundary:

```text
AIUI describes intent. Frameworks implement UI.
```

## Risk 2: Becoming A Design Canvas

AIUI should not start by competing with:

- Figma
- Claude Design
- Google Stitch
- v0
- Lovable

Boundary:

```text
AIUI provides the design intent layer that coding agents can read.
```

## Risk 3: Becoming An Automatic Aesthetic Judge

AIUI v0.1 should not do screenshot-based beauty scoring.

Boundary:

```text
Validate checks spec structure, not visual beauty.
```

Visual audit may become a future optional module only after the spec proves value.

## Risk 4: Copying Brands

AIUI should learn from strong products but avoid direct brand imitation.

Bad:

```yaml
brand: linear
```

Good:

```yaml
brand_profile:
  id: precise-product-ui
  density: compact
  border_strategy: subtle-lines
```

Boundary:

```text
Extract design decisions, not brand skins.
```

## Risk 5: Over-Abstracting

If AIUI is too abstract, agents will ignore it or interpret it randomly.

Bad:

```yaml
Card:
  radius: medium
```

Better:

```yaml
radius:
  md:
    value: 10
    usage: "cards, drawers, popovers"
    avoid:
      - "dense table rows"
      - "large landing hero regions"
```

Boundary:

```text
AIUI should be framework-neutral, not vague.
```

## Risk 6: Letting AI Define The Standard Alone

AI is useful for research and drafting, but final standards need human judgment.

Boundary:

```text
AI drafts. Humans decide.
```

## v0.1 Boundary Summary

Do:

- Spec
- Pattern graph
- Handoff pack
- React + Tailwind adapter
- Validate structure
- Benchmark

Do not:

- Visual canvas
- Screenshot beauty scoring
- Full code generation engine
- Figma replacement
- Multi-framework platform
- Brand-copy style packs

