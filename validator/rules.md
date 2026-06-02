# Validator Rules v0.1

This document defines the first validation rules for AIUI.

## Rule Groups

### 1. File Rules

Required files in a project AIUI pack:

```text
.aiui/project.aiui.yaml
.aiui/tokens.aiui.yaml
.aiui/agent-instructions.md
```

Recommended files:

```text
.aiui/pages/*.aiui.yaml
```

### 2. Naming Rules

All ids must:

- Use lowercase
- Use hyphen-separated words
- Avoid spaces
- Avoid framework names
- Avoid brand imitation names

Invalid:

```text
LinearDashboard
react-button
purple glass panel
```

Valid:

```text
management-list
settings-section
precise-product-ui
```

### 3. Project Rules

`project.aiui.yaml` must define:

- `project.id`
- `project.name`
- `project.register`
- `project.primary_users`
- `stack.frontend`
- `style.brand_profile`
- `style.density`
- `style.color_strategy`

### 4. Token Rules

`tokens.aiui.yaml` should define:

- `tokens.spacing`
- `tokens.radius`
- `tokens.typography`

Recommended:

- `tokens.surfaces`
- `tokens.motion`

### 5. Page Rules

Every page spec must define:

- `page.id`
- `page.type`
- `page.register`
- `page.primary_user`
- `page.goal`
- `layout.structure`
- `layout.density`
- `patterns.required`
- `regions.required`

### 6. Reference Rules

The validator should check that:

- Referenced patterns exist in the AIUI library
- Referenced components exist in the AIUI library
- Referenced brand profiles exist in the AIUI library or project pack
- Referenced tokens exist when a spec uses explicit token ids

### 7. Graph Rules

The validator should reject:

- Circular dependencies
- Components depending on pages
- Patterns depending on pages
- Unknown graph nodes

### 8. Avoid Rule Completeness

Every page and brand profile should include at least one `avoid` rule.

This helps reduce generic AI UI output.

## Error Format

```text
AIUI validation failed

<file>
  - [rule-id] Human-readable error message
```

Example:

```text
AIUI validation failed

.aiui/pages/order-management.aiui.yaml
  - [page.required] Missing page.goal
  - [reference.pattern] Unknown pattern: record-table
```

