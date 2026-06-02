# Benchmark Task：AI 工具 Landing Page

## 用户需求

构建一个 AI developer tool 的 landing page。

用户需要：

- 理解产品做什么
- 看到 workflow
- 相信它能配合 coding agents 工作
- 开始 trial

## Direct Prompt

```text
Build a landing page for an AI developer tool.

It should explain the product, show the workflow, include proof points, pricing preview, and a final call to action.
Make it beautiful and modern.
```

## AIUI-Assisted Prompt

```text
Build a landing page for an AI developer tool.

Before writing code, read the AIUI page spec:

examples/ai-tool-landing-page.aiui.yaml

Also follow:

adapters/agent-handoff-template.md
adapters/react-tailwind-adapter.md

Avoid generic purple AI gradients, identical icon-card feature grids, fake dashboard screenshots, and empty AI buzzword copy.
```

## 预期 Pattern

- landing-page
- product-proof
- workflow-section
- pricing-preview
- final-action

## 观察重点

- 页面是否避免 generic AI startup visuals？
- Hero 是否清楚表达产品？
- Workflow section 是否具体？
- 页面是否有足够品牌性，但不过度装饰？

