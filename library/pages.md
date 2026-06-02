# Pages Library v0.1

Pages are complete screen intents.

## Initial 5 Pages

1. login
2. order-management
3. dashboard
4. settings
5. billing

## Page Spec Template

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

## Page Design Rule

A page spec should be clear enough that two different AI agents produce similar structure even if their code differs.

