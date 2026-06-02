# React + Tailwind Adapter

这份 adapter 说明 AI coding agent 应该如何在 React + Tailwind 项目中实现 AIUI specs。

## 映射原则

AIUI Core 保持框架无关。

Adapter 负责映射：

```text
AIUI tokens → Tailwind theme or utility classes
AIUI components → React components
AIUI patterns → React page sections
AIUI pages → route-level page components
AIUI brand profile → visual defaults and avoid rules
```

## Implementation Rules

- 优先使用现有项目组件
- 明确拆分 layout regions
- 使用语义化 component names
- 不要给每个 section 都套大型装饰容器
- 避免 nested cards
- Product pages 默认保持紧凑，除非 page spec 另有说明
- 项目已有 icon library 时，常见操作优先用 icon
- 同时考虑 mobile 和 desktop

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

映射 tokens 时：

- 使用一致 spacing scale
- 除非必要，避免 arbitrary values
- Product UI 使用克制 shadow
- 如果项目有 tinted neutrals，避免纯黑纯白
- 控制 line length 和 responsive behavior

## Anti-Patterns

不要默认使用：

- Purple gradients
- Glass panels
- Oversized cards
- Hero-style product pages
- Identical feature grids
- Decorative metrics without user value

