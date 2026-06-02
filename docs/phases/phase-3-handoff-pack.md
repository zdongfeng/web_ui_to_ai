# Phase 3：Agent Handoff Pack

## 目标

让 AIUI 能进入真实 AI coding workflow。

## Handoff 结构

输出文件包建议为：

```text
.aiui/
  project.aiui.yaml
  tokens.aiui.yaml
  page.aiui.yaml
  agent-instructions.md
  examples/
```

## Agent Instruction 要求

Instruction 文件应该告诉 AI agent：

- 修改前端代码前先读取 AIUI 文件
- 优先使用现有项目组件
- 遵守 AIUI page structure
- 不要发明无关视觉 pattern
- 遵守 density、layout、brand profile
- spec 不完整时才询问
- framework-specific 决策交给 adapter

## 第一版 Adapter

第一版 adapter 是 React + Tailwind。

它应该解释：

- 如何把 tokens 映射为 Tailwind classes
- 如何解释 component specs
- 如何组织 page regions
- 如何避免常见 AI UI 错误

## 产出

- `adapters/agent-handoff-template.md`
- `adapters/react-tailwind-adapter.md`
- `examples/` 中的 page specs

## 退出标准

开发者可以把 handoff pack 交给 Codex 或 Claude Code，得到符合 AIUI 结构的页面。

