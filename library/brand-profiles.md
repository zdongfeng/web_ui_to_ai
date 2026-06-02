# Brand Profiles v0.1

Brand profiles 定义风格方向，但不复制具体公司。

## 初始 3 个 Profiles

### precise-product-ui

用于专业产品工具、管理系统、运营界面和 dashboards。

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

用于需要友好但仍然实用的 SaaS 产品。

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

用于 landing pages、内容页、发布页和品牌主导页面。

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

## Profile 规则

Profiles 应描述视觉行为，而不是品牌模仿。

