# Pattern Graph

Pattern Graph 描述 AIUI 对象之间如何依赖和组合。

这是 AIUI 最重要的部分之一。

## 为什么重要

AI 生成 UI 经常失败，是因为它自由选择页面结构。

Pattern Graph 给 agent 一条受约束的组合路径。

```text
Page
→ Patterns
→ Regions
→ Components
→ Tokens
```

## 示例 Graph

```yaml
page:
  id: order-management
  uses:
    patterns:
      - app-shell
      - management-list

pattern:
  id: management-list
  uses:
    regions:
      - page-header
      - filter-toolbar
      - data-table
      - pagination
      - detail-drawer

region:
  id: filter-toolbar
  uses:
    components:
      - search-input
      - select
      - button
```

## Graph 规则

- 一个 page 可以使用多个 patterns
- 一个 pattern 可以使用多个 regions
- 一个 region 可以使用多个 components
- Components 可以依赖 tokens
- Patterns 不应该依赖 pages
- Components 不应该依赖 pages
- 循环依赖无效

## Validation 示例

无效：

```text
management-list -> data-table-workspace -> management-list
```

无效：

```text
button -> order-management
```

有效：

```text
order-management -> management-list -> data-table -> tokens
```

