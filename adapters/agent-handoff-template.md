# Agent Handoff Template

把 AIUI 交给 AI coding agent 时使用这份模板。

## Instruction

写前端代码前，先读取当前项目里的 AIUI 文件。

遵循优先级：

1. 现有项目组件和代码约定
2. AIUI page spec
3. AIUI patterns
4. AIUI brand profile
5. AIUI adapter guidance
6. 通用前端判断

## Rules

- 如果 AIUI spec 完整，不要发明完全不同的页面结构。
- 不要把 product pages 做成 marketing layouts。
- 不要使用重复装饰性 card grids，除非 pattern 明确要求。
- 保持 density、spacing、hierarchy 与 brand profile 一致。
- Product UI 优先实用性，少做装饰性 UI。
- 有现有代码规范时，优先遵守项目规范。
- 只有缺少 required region 或 primary user goal 时才询问。

## Expected Output

根据以下文件实现页面：

```text
.aiui/project.aiui.yaml
.aiui/page.aiui.yaml
.aiui/tokens.aiui.yaml
```

如果 framework adapter 与现有项目约定冲突，优先遵守项目约定，并解释差异。

