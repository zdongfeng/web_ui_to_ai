# Phase 6：产品化

## 目标

把 AIUI 从 specification repository 变成开发者可用产品。

## 产品形态

### CLI

```bash
aiui init
aiui add-page order-management
aiui validate
aiui handoff codex
```

### 文档站

文档站应该解释：

- AIUI 是什么
- 如何和 AI coding agents 一起使用
- Component 和 pattern references
- Example page specs
- Benchmark results

### Starter Repo

提供 starter repo：

- `.aiui/`
- Example React + Tailwind app
- Example page tasks
- Agent handoff instructions

## 未来模块

这些模块应该等 v0.1 被验证后再考虑：

- Project Profiler
- Figma import
- Screenshot-based UI audit
- Multi-framework adapters
- Pattern marketplace
- Team style profiles

## 退出标准

新用户可以安装或复制 AIUI，初始化项目，生成 page spec，并用 AI agent 构建更好的前端页面。

