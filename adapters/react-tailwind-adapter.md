# React + Tailwind Adapter

This adapter explains how an AI coding agent should implement AIUI specs in a React + Tailwind project.

## Mapping Principles

AIUI core remains framework-neutral.

The adapter maps:

```text
AIUI tokens → Tailwind theme or utility classes
AIUI components → React components
AIUI patterns → React page sections
AIUI pages → route-level page components
AIUI brand profile → visual defaults and avoid rules
```

## Implementation Rules

- Use existing project components first
- Keep layout regions explicit
- Use semantic component names
- Avoid large decorative wrappers around every section
- Avoid nested card structures
- Keep product pages compact unless the page spec says otherwise
- Use icons for common actions when the project already uses an icon library
- Ensure mobile and desktop layouts are both considered

## Example Page Structure

```tsx
export function OrderManagementPage() {
  return (
    <AppShell>
      <PageHeader />
      <FilterToolbar />
      <OrdersTable />
      <Pagination />
      <OrderDetailDrawer />
    </AppShell>
  );
}
```

## Tailwind Guidance

When mapping tokens:

- Use consistent spacing scale
- Avoid arbitrary values unless needed
- Prefer restrained shadows for product UI
- Avoid pure black and pure white if project tokens provide tinted neutrals
- Keep line length and responsive behavior under control

## Anti-Patterns

Do not default to:

- Purple gradients
- Glass panels
- Oversized cards
- Hero-style product pages
- Identical feature grids
- Decorative metrics without user value

