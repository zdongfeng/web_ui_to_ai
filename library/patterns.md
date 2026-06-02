# Patterns Library v0.1

Patterns 是可复用 UI 组合。

它们比 components 更重要，因为它们指导 AI 如何组织页面结构。

## 初始 10 个 Patterns

1. app-shell
2. management-list
3. data-table-workspace
4. settings-section
5. detail-drawer
6. auth-form
7. billing-overview
8. onboarding-flow
9. editor-layout
10. landing-page

## Pattern Spec 模板

```yaml
pattern:
  id: management-list
  register: product
  purpose: "Manage and inspect a collection of records"
  layout:
    default_structure: sidebar-content
    density: compact
  required_regions:
    - page-header
    - filter-toolbar
    - data-table
    - pagination
  optional_regions:
    - bulk-actions
    - detail-drawer
  components:
    recommended:
      - search-input
      - select
      - table
      - badge
      - pagination
  avoid:
    - "marketing hero"
    - "large decorative cards"
    - "unrelated stats section"
```

## Pattern 设计规则

Pattern 必须说明什么时候应该用，以及什么时候不应该用。

