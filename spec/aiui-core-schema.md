# AIUI Core Schema

这份文档描述 AIUI 的第一版概念 schema。

当前先用 Markdown 表达结构。等字段稳定后，再转换成 JSON Schema、Zod schema 或其他机器可校验格式。

## Foundation

Foundation 定义高层设计原则。

示例：

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

Tokens 定义可复用设计值。

示例：

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

Components 定义语义化 UI 构件，不是 React、Vue、Tailwind 或 HTML 代码。

示例：

```yaml
component:
  id: button
  category: action
  purpose: "Trigger a user action"
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

Patterns 定义组件和区域如何组合。

示例：

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

Pages 定义完整页面意图。

示例：

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

Brand profiles 定义风格方向，但不复制具体品牌。

示例：

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

