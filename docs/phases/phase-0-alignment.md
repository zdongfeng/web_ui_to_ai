# Phase 0：产品边界确认

## 目标

定义产品边界，避免太早把产品做大。

## 关键问题

- 第一批用户是谁？
- 他们的明确痛点是什么？
- AIUI 不做什么？
- v0.1 支持哪些 agent workflow？
- 用哪个前端技术栈做验证？

## 决策

### 第一批用户

主要使用 AI coding agent 写前端页面的开发者。

### 痛点

AI 生成的前端页面经常泛、丑、不稳定，也不像真实产品。

### 产品边界

AIUI 提供 UI 意图规范和 agent handoff workflow。

v0.1 不提供可视化设计画布。

### 第一版技术栈

React + Tailwind。

## 产出

- Vision document
- v0.1 scope document
- Product architecture document
- Initial repository structure

## 退出标准

团队可以用一句话解释 AIUI：

```text
AIUI 是一个 UI 意图协议，帮助 AI coding agent 在写代码前理解页面结构和设计约束。
```

