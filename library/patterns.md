# Patterns Library v0.1

Patterns are reusable UI compositions.

They are more important than components because they guide AI page structure.

## Initial 10 Patterns

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

## Pattern Spec Template

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

## Pattern Design Rule

A pattern must explain when it should be used and when it should not be used.

