# AIUI

AIUI 是 AI UI Specification 的缩写。它是一套给 AI coding agent 使用的 UI 意图协议。

目标很简单：当开发者让 Codex、Claude Code、Cursor、Gemini CLI、Windsurf、Augment 或其他 AI agent 开发前端页面时，AI 不应该从空白页自由发明布局、样式、密度、层级和组件组合。它应该先读取一份结构化的 UI 规范。

AIUI 不是：

- UI 组件库
- React 或 Vue 框架
- Figma 替代品
- 可视化设计画布
- 自动审美裁判

AIUI 是：

- 机器可读的 UI 意图规范
- 常见产品页面的 Pattern Graph
- AI coding agent 的设计约束层
- 让 AI 写代码前先理解页面结构的 handoff pack
- 轻量的规范一致性校验系统

## 目录结构

```text
docs/
  00-vision.md
  01-human-ai-workflow.md
  02-product-architecture.md
  03-development-roadmap.md
  04-v0.1-scope.md
  05-validation-plan.md
  06-stage-execution-plan.md
  07-product-design-plan.md
  08-next-actions.md
  09-risks-and-boundaries.md
  10-mvp-build-order.md
  phases/
    phase-0-alignment.md
    phase-1-research.md
    phase-2-core-spec.md
    phase-3-handoff-pack.md
    phase-4-validate.md
    phase-5-benchmark.md
    phase-6-productization.md

spec/
  aiui-core-schema.md
  naming-conventions.md
  pattern-graph.md

library/
  components.md
  components/
    *.aiui.yaml
  patterns.md
  patterns/
    *.aiui.yaml
  pages.md
  pages/
    *.aiui.yaml
  brand-profiles.md
  brand-profiles/
    *.aiui.yaml

adapters/
  agent-handoff-template.md
  react-tailwind-adapter.md

guides/
  use-with-codex.md
  use-with-claude-code.md

prompts/
  generate-page-from-aiui.md
  draft-page-spec.md
  extract-pattern-from-reference.md
  compare-without-aiui.md

examples/
  order-management-page.aiui.yaml
  saas-settings-page.aiui.yaml
  ai-tool-landing-page.aiui.yaml

research/
  README.md
  templates/
    design-case-template.md
    pattern-extraction-template.md

benchmarks/
  README.md
  scoring-rubric.md
  result-template.md
  tasks/
    order-management.md
    saas-settings.md
    ai-tool-landing.md

templates/
  project-aiui/
    project.aiui.yaml
    tokens.aiui.yaml
    agent-instructions.md
    pages/
      order-management.aiui.yaml

validator/
  README.md
  rules.md
  implementation-plan.md
```

## 建议阅读顺序

1. `docs/00-vision.md`: 产品愿景
2. `docs/06-stage-execution-plan.md`: 中文阶段执行总纲
3. `docs/07-product-design-plan.md`: 产品设计方案
4. `docs/03-development-roadmap.md`: 阶段路线
5. `docs/04-v0.1-scope.md`: 第一版边界
6. `docs/09-risks-and-boundaries.md`: 风险和边界
7. `docs/10-mvp-build-order.md`: MVP 构建顺序
8. `spec/aiui-core-schema.md`: 核心规范骨架
9. `library/`: 第一批 components、patterns、pages、brand profiles
10. `templates/project-aiui/`: 示例 `.aiui` handoff 包
11. `guides/`: Codex 和 Claude Code 使用指南
12. `prompts/`: 可复制 AI 工作流 prompt
13. `benchmarks/`: 第一批验证任务和评分表
14. `validator/`: 轻量校验规则和实现计划

## 第一个里程碑

把 AIUI v0.1 做成一个文档优先、验证优先的项目：

- 20 abstract components
- 10 reusable patterns
- 5 page specs
- 3 style profiles
- 1 React + Tailwind adapter
- 1 agent handoff template
- 1 lightweight spec validator
- 3 benchmark examples

第一阶段的成功指标不是用户规模，而是证明：

> Given the same frontend task, an AI coding agent using AIUI should produce a page that is more consistent, less generic, and closer to a real product UI than the same agent working without AIUI.

也就是：同一个前端需求，使用 AIUI 的 AI agent 产出应该比不使用 AIUI 时更稳定、更少 AI 味、更接近真实产品界面。
