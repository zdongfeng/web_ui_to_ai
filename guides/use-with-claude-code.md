# 在 Claude Code 中使用 AIUI

这份文档说明如何在 Claude Code 中使用 AIUI。

## 推荐项目结构

在目标项目中放置 `.aiui/` 文件夹。

```text
.aiui/
  project.aiui.yaml
  tokens.aiui.yaml
  agent-instructions.md
  pages/
    order-management.aiui.yaml
```

## 推荐 Claude Code Prompt

```text
Use AIUI as the source of design intent for this frontend task.

Read these files first:

.aiui/agent-instructions.md
.aiui/project.aiui.yaml
.aiui/tokens.aiui.yaml
.aiui/pages/order-management.aiui.yaml

Then implement the requested page.

Important:
- Follow the required patterns and regions.
- Use existing components before creating new ones.
- Keep the UI compact and operational.
- Avoid generic AI UI patterns listed in the page spec.
- If the project conventions conflict with AIUI, explain the tradeoff before implementing.
```

## 适合 Claude Code 的任务

- 根据 AIUI 生成页面
- 把 AI 生成过的页面重构为符合 AIUI
- 把产品需求转成 draft page spec
- 检查某个页面实现是否包含 required regions
- 从重复 UI 结构中提炼新的 pattern candidate

## 人工 Review 要点

Claude Code 生成页面后，人应该检查：

- 是否遵守 page type？
- 是否包含 required regions？
- 是否避开 banned generic patterns？
- 是否保留现有项目约定？
- 是否创建了不必要的新组件？

