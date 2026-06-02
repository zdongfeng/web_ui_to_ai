# Brand Profiles v0.1

Brand profiles define style direction without copying specific companies.

## Initial 3 Profiles

### precise-product-ui

Use for professional product tools, admin systems, operations interfaces, and dashboards.

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
    - "large marketing cards"
```

### calm-saas

Use for SaaS products that need to feel approachable but still practical.

```yaml
brand_profile:
  id: calm-saas
  density: medium
  color_strategy: restrained-with-accent
  surface_style: soft
  border_strategy: subtle
  typography_character: clear-friendly
  motion: light-feedback
  avoid:
    - "generic purple gradients"
    - "excessive rounded cards"
    - "too many decorative illustrations"
```

### editorial-brand

Use for landing pages, content pages, launches, and brand-led surfaces.

```yaml
brand_profile:
  id: editorial-brand
  density: open
  color_strategy: committed
  surface_style: content-first
  border_strategy: minimal
  typography_character: expressive
  motion: selective
  avoid:
    - "identical card grids"
    - "hero metric template"
    - "stock SaaS layout"
```

## Profile Rule

Profiles should describe visual behavior, not brand imitation.

