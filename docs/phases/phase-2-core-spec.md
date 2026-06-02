# Phase 2：Core Spec v0.1

## 目标

创建 AIUI core specification 的第一版。

## 核心对象

AIUI v0.1 需要定义：

- Foundation
- Tokens
- Components
- Patterns
- Pages
- Brand profiles
- Rules

## 必做工作

### 1. 定义 Schema

描述每种对象的必填字段和可选字段。

### 2. 定义命名规则

名称必须稳定、小写、语义化。

示例：

```text
management-list
settings-page
filter-toolbar
precise-product-ui
```

### 3. 定义 Component Specs

先从 20 个 components 开始。

示例：

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

### 4. 定义 Patterns

先从 10 个 patterns 开始。

示例：

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

### 5. 定义 Pages

先从 5 个 pages 开始。

示例：

- login
- order-management
- dashboard
- settings
- billing

## 产出

- `spec/aiui-core-schema.md`
- `spec/naming-conventions.md`
- `spec/pattern-graph.md`
- `library/components.md`
- `library/patterns.md`
- `library/pages.md`
- `library/brand-profiles.md`

## 退出标准

AI coding agent 读取 page spec 后，能在实现前理解要构建什么页面。

