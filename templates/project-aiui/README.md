# Project AIUI Template

这个目录是给真实产品项目使用的 `.aiui/` starter pack。

在用户项目中，它会变成：

```text
.aiui/
  project.aiui.yaml
  tokens.aiui.yaml
  pages/
    order-management.aiui.yaml
  agent-instructions.md
```

## 使用方式

把这个结构复制进前端项目，然后让 AI coding agent 执行：

```text
Before editing frontend code, read .aiui/agent-instructions.md and the relevant page spec.
Implement the requested page according to AIUI.
```

