# AIUI 产品设计方案

这份文档描述 AIUI 作为产品应该如何被用户使用、由哪些模块组成，以及第一版如何保持足够小。

## 目标用户

第一批目标用户不是专业设计师，而是：

```text
会写业务逻辑、会用 AI coding agent，但不想花大量时间设计前端页面的开发者。
```

他们常见的工作方式是：

```text
我有一个功能需求
→ 我让 AI 写页面
→ AI 生成了页面
→ 页面能跑，但很丑
→ 我不断说“好看一点”
→ 结果越改越乱
```

AIUI 要改变的是中间这一步：

```text
我有一个功能需求
→ AIUI 生成或选择页面 spec
→ AI agent 先读 spec
→ 再写页面
→ 页面第一稿更稳定
```

## 用户核心流程

### 流程 1：新项目初始化

```text
1. 用户运行 aiui init
2. AIUI 询问产品类型、用户、页面风格、前端技术栈
3. AIUI 生成 .aiui/project.aiui.yaml
4. AIUI 生成基础 tokens 和 brand profile
5. 用户把 .aiui/ 交给 AI coding agent 使用
```

### 流程 2：新增页面

```text
1. 用户描述页面需求
2. AIUI 判断 page type
3. AIUI 选择对应 pattern
4. AIUI 生成 page.aiui.yaml
5. 用户让 Codex 或 Claude Code 根据 page spec 实现页面
```

### 流程 3：已有项目接入

v0.1 可以先手动接入，后续再做自动 profiler。

```text
1. 用户提供项目说明和已有页面截图
2. AI 辅助生成 PROJECT_AIUI.yaml
3. 人确认 style profile、density、avoid rules
4. 后续 AI agent 按这个项目的 AIUI 继续开发页面
```

### 流程 4：规范校验

```text
1. 用户运行 aiui validate
2. 工具检查 spec 结构和引用
3. 输出缺失字段、错误引用、循环依赖
4. 用户或 AI 修复规范
```

## 产品模块

### 1. Spec Library

产品核心。

包含：

- Foundation
- Tokens
- Components
- Patterns
- Pages
- Brand Profiles

它回答：

```text
AI 应该如何理解一个页面？
```

### 2. Pattern Graph

AIUI 的关键差异点。

它回答：

```text
这个页面应该由哪些 pattern、region、component 组成？
```

例如：

```text
order-management
→ management-list
→ filter-toolbar
→ data-table
→ pagination
→ detail-drawer
```

### 3. Handoff Pack

让 AI coding agent 真正可用。

包含：

- project spec
- page spec
- token spec
- agent instructions
- adapter guidance

它回答：

```text
怎么把 AIUI 交给 Codex、Claude Code、Cursor？
```

### 4. Adapter

把框架无关的 AIUI 转成某个技术栈里的实现约束。

v0.1 只做：

```text
React + Tailwind
```

Adapter 不应该改变 AIUI Core。

### 5. Validate

轻量校验模块。

它回答：

```text
这份 AIUI 文件结构是否正确？
```

它不回答：

```text
这个页面漂不漂亮？
```

### 6. Benchmark

证明产品价值。

它回答：

```text
AIUI 是否真的让 AI 写出的页面更好？
```

## CLI 设计

第一版 CLI 可以很简单。

```bash
aiui init
aiui add-page order-management
aiui validate
aiui handoff codex
aiui handoff claude-code
```

### aiui init

创建 `.aiui/` 目录。

输出：

```text
.aiui/
  project.aiui.yaml
  tokens.aiui.yaml
  agent-instructions.md
```

### aiui add-page

根据页面类型生成 page spec。

示例：

```bash
aiui add-page order-management
```

输出：

```text
.aiui/pages/order-management.aiui.yaml
```

### aiui validate

检查 AIUI 文件。

### aiui handoff

生成适配不同 agent 的说明。

示例：

```bash
aiui handoff codex
```

输出：

```text
.aiui/handoff/codex.md
```

## 未来 Web 产品形态

Web 产品不应该从第一天开始做，但可以提前设计。

### 页面 1：Project Dashboard

展示：

- 当前项目使用的 brand profile
- 当前项目已有 pages
- 当前项目已有 patterns
- Validate 状态
- 最近 handoff 记录

### 页面 2：Spec Editor

编辑：

- tokens
- brand profile
- page spec
- pattern spec

要求：

- 结构化编辑
- YAML 预览
- 错误提示

### 页面 3：Pattern Library

展示：

- 常见 page patterns
- 每个 pattern 的适用场景
- 每个 pattern 的 avoid rules
- 关联 components

### 页面 4：Page Builder

用户选择：

- 页面类型
- 用户目标
- 产品类型
- style profile
- 必要区域

输出：

- page.aiui.yaml
- agent handoff prompt

### 页面 5：Handoff Center

生成：

- Codex prompt
- Claude Code prompt
- Cursor prompt
- Gemini CLI prompt

## 数据结构设计

### Project

```yaml
project:
  id: example-product
  name: Example Product
  register: product
  primary_users:
    - operations-user
  stack:
    frontend: react-tailwind
```

### Style

```yaml
style:
  brand_profile: precise-product-ui
  density: compact
  color_strategy: restrained
  surface_style: flat
```

### Page

```yaml
page:
  id: order-management
  type: management-list
  goal: "Find, filter, inspect, and update orders"
  patterns:
    required:
      - app-shell
      - management-list
```

### Rules

```yaml
rules:
  avoid:
    - "marketing hero in product pages"
    - "generic gradient backgrounds"
    - "unrelated stats cards"
```

## v0.1 产品边界

第一版只要能完成这件事：

```text
用户选择一个页面类型
→ 生成 AIUI page spec
→ handoff 给 AI coding agent
→ AI agent 生成更好的前端页面
```

就已经足够。

不要在 v0.1 追求：

- 自动设计
- 自动审美
- 自动修图
- 自动生成完整项目
- 自动学习全网 UI

## 产品成功标准

v0.1 成功不看功能数量。

只看：

- AIUI 是否让 AI 第一稿更好
- 是否减少用户说“再好看点”的次数
- 是否让不同 agent 生成更一致的页面结构
- 是否让开发者愿意在项目里保留 `.aiui/`

