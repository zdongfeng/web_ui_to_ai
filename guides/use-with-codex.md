# 在 Codex 中使用 AIUI

这份文档说明如何在让 Codex 构建前端页面时使用 AIUI。

## 推荐项目结构

在目标项目中放置 `.aiui/` 文件夹。

可以使用 `templates/project-aiui/` 作为起始结构。

```text
.aiui/
  project.aiui.yaml
  tokens.aiui.yaml
  agent-instructions.md
  pages/
    order-management.aiui.yaml
```

## 推荐 Codex Prompt

```text
Before editing files, read:

.aiui/agent-instructions.md
.aiui/project.aiui.yaml
.aiui/tokens.aiui.yaml
.aiui/pages/order-management.aiui.yaml

Implement the order management page according to AIUI.

Follow the page structure, patterns, recommended components, density, brand profile, and avoid rules.
Use existing project components first.
Do not turn this product page into a marketing page.
```

## 适合交给 Codex 的任务

适合：

- 根据 AIUI page spec 实现页面
- 把现有页面调整为符合 AIUI
- 从项目中提取缺失 tokens 到 `.aiui/tokens.aiui.yaml`
- 对比当前实现是否符合 AIUI structure
- 基于已有 AIUI pattern 新增 page spec

不适合：

- 让 Codex 独自发明整个 AIUI 标准
- 让 Codex 在没有人工审阅时决定最终设计品味
- v0.1 阶段要求 Codex 做视觉审美评分

## 期望 Codex 行为

Codex 应该：

- 实现前读取 AIUI 文件
- 检查现有项目组件
- 按明确 regions 实现页面
- 根据 brand profile 保持设计一致性
- 解释任何偏离 AIUI spec 的地方

