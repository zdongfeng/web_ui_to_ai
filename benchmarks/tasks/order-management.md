# Benchmark Task：订单管理页

## 用户需求

构建一个运营后台的订单管理页。

用户需要：

- 搜索订单
- 按状态筛选
- 按日期范围筛选
- 查看订单状态
- 检查订单详情
- 更新履约状态
- 执行批量操作

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

## 预期 Pattern

- app-shell
- management-list
- data-table-workspace
- optional detail-drawer

## 观察重点

- AI 是否使用真实 table，而不是装饰性 cards？
- Filters 是否真的有用？
- 是否保持 product UI density？
- 是否避免无关 hero metrics？

