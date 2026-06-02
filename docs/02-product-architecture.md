# 产品架构

AIUI 由六个产品模块组成。

## 1. AIUI Spec

核心规范。

它定义：

- Foundation principles
- Tokens
- Components
- Patterns
- Pages
- Brand profiles
- Rules and anti-patterns

Spec 保持框架无关，但必须足够具体，让 adapter 可以生成稳定的前端实现约束。

## 2. Pattern Graph

Pattern Graph 是 AIUI 的主要壁垒。

它描述 pages、patterns、regions、components 之间如何组合。

示例：

```yaml
page:
  type: management-list
  uses:
    - app-shell
    - page-header
    - filter-toolbar
    - data-table
    - detail-drawer
```

它的作用是避免 AI 随机拼页面。

## 3. Handoff Pack

Handoff Pack 是开发者交给 Codex、Claude Code、Cursor、Gemini CLI 或其他 AI coding agent 的文件包。

建议结构：

```text
.aiui/
  project.aiui.yaml
  tokens.aiui.yaml
  page.aiui.yaml
  agent-instructions.md
  examples/
```

它把规范转成 coding agent 可以直接读取的上下文。

## 4. Adapters

Adapter 说明 AIUI 如何落到某个技术栈。

v0.1 只支持：

```text
React + Tailwind
```

未来可以支持：

- Vue + UnoCSS
- Svelte
- Flutter
- SwiftUI
- HTML + CSS

Adapter 不应该污染 AIUI Core。

## 5. Validate

AIUI Validate 用来检查规范一致性。

它检查：

- 必填字段
- 未知引用
- 重复命名
- 循环依赖
- 缺失 tokens
- page spec 是否缺少关键 region
- brand profile 是否缺少 density 或 color strategy

v0.1 不做视觉审美判断。

## 6. Project Profiler

Project Profiler 是未来模块。

它读取现有项目、截图或设计说明，生成项目专属 AIUI profile。

这会成为项目自己的 UI memory。

示例：

```yaml
project:
  register: product
  audience: internal-operators

style:
  density: compact
  color_strategy: restrained
  surface_style: flat
  border_strategy: subtle-lines
```

Project Profiler 很有价值，但不应该在核心规范未验证前进入 v0.1。

