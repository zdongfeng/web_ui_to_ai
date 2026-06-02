# Benchmark Task: Order Management Page

## User Requirement

Build an order management page for an operations dashboard.

Users need to:

- Search orders
- Filter by status
- Filter by date range
- View order status
- Inspect order details
- Update fulfillment status
- Handle bulk actions

## Direct Prompt

```text
Build an order management page for an operations dashboard.

It should include search, filters, an order table, status badges, pagination, bulk actions, and a way to inspect order details.
Make it look polished and production-ready.
```

## AIUI-Assisted Prompt

```text
Build an order management page.

Before writing code, read the AIUI page spec:

examples/order-management-page.aiui.yaml

Also follow:

adapters/agent-handoff-template.md
adapters/react-tailwind-adapter.md

Use the AIUI page structure and avoid rules. Do not turn this product page into a landing page. Keep it compact and operational.
```

## Expected Pattern

- app-shell
- management-list
- data-table-workspace
- optional detail-drawer

## Things To Watch

- Does the AI use a real table or decorative cards?
- Does it create useful filters?
- Does it preserve product UI density?
- Does it avoid unrelated hero metrics?

