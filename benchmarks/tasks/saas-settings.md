# Benchmark Task：SaaS 设置页

## 用户需求

构建一个 SaaS 产品的 workspace settings page。

用户需要：

- 更新 workspace name
- 管理 billing email
- 切换 product preferences
- 查看 security settings
- 访问 danger zone

## Direct Prompt

```text
Build a polished SaaS workspace settings page.

It should include workspace profile settings, billing email, preferences, security settings, and a danger zone.
Make it clean and modern.
```

## AIUI-Assisted Prompt

```text
Build a SaaS workspace settings page.

Before writing code, read the AIUI page spec:

examples/saas-settings-page.aiui.yaml

Also follow:

adapters/agent-handoff-template.md
adapters/react-tailwind-adapter.md

Use grouped settings sections and practical product UI. Avoid marketing-style cards, hero headers, and modal-first editing.
```

## 预期 Pattern

- app-shell
- settings-section
- optional billing-overview

## 观察重点

- AI 是否使用 rows 和 sections，而不是 feature cards？
- Destructive actions 是否被清晰分离？
- 页面是否像真实软件设置页？

