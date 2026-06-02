# Phase 2: Core Spec v0.1

## Goal

Create the first version of the AIUI core specification.

## Core Objects

AIUI v0.1 should define:

- Foundation
- Tokens
- Components
- Patterns
- Pages
- Brand profiles
- Rules

## Required Work

### 1. Define Schema

Describe required and optional fields for every object type.

### 2. Define Naming Rules

Names must be stable, lowercase, and semantic.

Example:

```text
management-list
settings-page
filter-toolbar
precise-product-ui
```

### 3. Define Component Specs

Start with 20 components.

Examples:

- button
- icon-button
- input
- select
- checkbox
- tabs
- table
- pagination
- drawer
- toast

### 4. Define Patterns

Start with 10 patterns.

Examples:

- app-shell
- management-list
- settings-section
- data-table-workspace
- detail-drawer
- onboarding-flow
- auth-form
- billing-overview
- editor-layout
- landing-page

### 5. Define Pages

Start with 5 pages.

Examples:

- login
- order-management
- dashboard
- settings
- billing

## Deliverables

- `spec/aiui-core-schema.md`
- `spec/naming-conventions.md`
- `spec/pattern-graph.md`
- `library/components.md`
- `library/patterns.md`
- `library/pages.md`
- `library/brand-profiles.md`

## Exit Criteria

An AI coding agent can read a page spec and understand what it should build before implementation begins.

