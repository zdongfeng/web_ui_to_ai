# Phase 4: Validate

## Goal

Keep the AIUI spec internally consistent.

## Validation Rules

v0.1 validation should check:

- Required fields exist
- Names follow conventions
- Referenced components exist
- Referenced patterns exist
- Referenced tokens exist
- No duplicate identifiers
- No circular dependencies
- Page specs include required regions
- Brand profiles define density, color strategy, surface strategy, typography, and avoid rules

## What Validate Does Not Do

It does not:

- Judge beauty
- Read screenshots
- Score visual design
- Automatically fix frontend code

## CLI Concept

```bash
aiui validate
```

Possible output:

```text
AIUI validation failed

pages/order-management.aiui.yaml
  - Unknown component: status-badge
  - Missing required region: page-header

patterns/management-list.aiui.yaml
  - Circular dependency detected: management-list -> data-table-workspace -> management-list
```

## Deliverables

- Validation rule list
- Error message format
- Implementation plan
- Future JSON Schema plan

## Exit Criteria

The spec can grow without becoming inconsistent.

