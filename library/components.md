# Components Library v0.1

AIUI components 是语义化 UI 构件。它们不是 React、Vue、Tailwind 或 HTML 组件。

## 初始 20 个 Components

1. button
2. icon-button
3. input
4. search-input
5. textarea
6. select
7. checkbox
8. radio
9. switch
10. tabs
11. badge
12. table
13. pagination
14. drawer
15. popover
16. toast
17. tooltip
18. form-field
19. empty-state
20. section-header

## Component Spec 模板

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
  usage:
    preferred:
      - "primary page action"
      - "form submission"
    avoid:
      - "using multiple primary buttons in the same region"
```

## Component 设计规则

每个 component 都应该描述：

- Purpose
- Variants
- States
- Usage guidance
- Avoid rules
- Related patterns

