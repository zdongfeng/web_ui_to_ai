# AIUI Core Schema

This document describes the first conceptual schema for AIUI.

The schema is intentionally written in Markdown first. Once the structure stabilizes, it can be converted into JSON Schema or another machine-checkable format.

## Foundation

Foundation defines high-level design principles.

Example:

```yaml
foundation:
  hierarchy:
    max_heading_levels: 3
    primary_method: typography-and-spacing
  consistency:
    reuse_components: true
  accessibility:
    required: true
  layout:
    avoid_nested_cards: true
```

## Tokens

Tokens define reusable design values.

Example:

```yaml
tokens:
  spacing:
    xs: 4
    sm: 8
    md: 16
    lg: 24
    xl: 32
  radius:
    sm: 6
    md: 10
    lg: 14
  typography:
    body:
      size: 16
      line_height: 1.5
```

## Components

Components define semantic UI building blocks, not framework code.

Example:

```yaml
component:
  id: button
  category: action
  variants:
    - primary
    - secondary
    - ghost
  sizes:
    - sm
    - md
    - lg
  states:
    - default
    - hover
    - focus
    - disabled
```

## Patterns

Patterns define component composition.

Example:

```yaml
pattern:
  id: management-list
  purpose: "Manage a collection of records"
  regions:
    - page-header
    - filter-toolbar
    - data-table
    - pagination
  optional_regions:
    - bulk-actions
    - detail-drawer
  avoid:
    - "marketing hero"
    - "large decorative stats cards"
```

## Pages

Pages define complete screen intent.

Example:

```yaml
page:
  id: order-management
  type: management-list
  register: product
  layout:
    structure: sidebar-content
  uses:
    patterns:
      - app-shell
      - management-list
    components:
      - table
      - search-input
      - select
      - badge
      - drawer
```

## Brand Profiles

Brand profiles define style direction without copying specific brands.

Example:

```yaml
brand_profile:
  id: precise-product-ui
  density: compact
  color_strategy: restrained
  surface_style: flat
  border_strategy: subtle-lines
  typography_character: precise
  motion: minimal-functional
  avoid:
    - "heavy shadows"
    - "decorative gradients"
    - "oversized marketing sections"
```

