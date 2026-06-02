# Pattern Graph

The pattern graph describes how AIUI objects depend on and compose each other.

This is one of the most important parts of AIUI.

## Why It Matters

AI-generated UI often fails because the agent chooses page structure freely.

The pattern graph gives the agent a constrained composition path.

```text
Page
→ Patterns
→ Regions
→ Components
→ Tokens
```

## Example Graph

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

## Graph Rules

- A page can use many patterns
- A pattern can use many regions
- A region can use many components
- Components can depend on tokens
- Patterns should not depend on pages
- Components should not depend on pages
- Circular dependencies are invalid

## Validation Examples

Invalid:

```text
management-list -> data-table-workspace -> management-list
```

Invalid:

```text
button -> order-management
```

Valid:

```text
order-management -> management-list -> data-table -> tokens
```

