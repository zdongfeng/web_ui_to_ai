# Pages Library v0.1

Pages 是完整页面意图。

## 初始 5 个 Pages

1. login
2. order-management
3. dashboard
4. settings
5. billing

## Page Spec 模板

```yaml
page:
  id: order-management
  type: management-list
  register: product
  primary_user: operations-user
  goal: "Find, filter, inspect, and update orders"
  layout:
    structure: sidebar-content
    density: compact
  patterns:
    required:
      - app-shell
      - management-list
    optional:
      - detail-drawer
  regions:
    - page-header
    - filter-toolbar
    - data-table
    - pagination
  avoid:
    - "landing page structure"
    - "hero metrics"
    - "decorative feature cards"
```

## Page 设计规则

Page spec 应该足够清楚，让两个不同 AI agent 即使写出不同代码，也能生成相近的页面结构。

