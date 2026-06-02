# Components Library v0.1

AIUI components are semantic UI building blocks. They are not React, Vue, Tailwind, or HTML components.

## Initial 20 Components

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

## Component Spec Template

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

## Component Design Rule

Every component should describe:

- Purpose
- Variants
- States
- Usage guidance
- Avoid rules
- Related patterns

