# Validator Implementation Plan

The validator should be implemented after the v0.1 spec stabilizes.

## Recommended Stack

Use Node.js for the first implementation.

Reasons:

- Easy CLI distribution through npm
- YAML parsing is straightforward
- Most frontend developers already have Node
- Works naturally with React + Tailwind validation experiments

## Suggested Packages

- `yaml` for YAML parsing
- `zod` or JSON Schema for structural validation
- A small custom graph checker for dependencies

## CLI Shape

```bash
aiui validate
aiui validate --path .aiui
aiui validate --strict
```

## Implementation Steps

1. Load `.aiui/` files
2. Parse YAML
3. Validate required fields
4. Validate names
5. Load built-in library ids
6. Check references
7. Build graph
8. Detect cycles
9. Print errors
10. Exit with non-zero status when validation fails

## First Tests

Create fixtures:

- valid project
- missing project fields
- unknown component reference
- unknown pattern reference
- circular pattern dependency
- invalid naming

## Future Strict Mode

Strict mode may check:

- Every page has avoid rules
- Every pattern has usage and non-usage rules
- Every component has states
- Every brand profile defines motion

