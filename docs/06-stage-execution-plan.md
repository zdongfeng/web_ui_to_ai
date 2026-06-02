# AIUI 阶段执行总纲

这份文档用于指导我们从 0 到 1 开发 AIUI。它比路线图更偏执行，明确每个阶段要做什么、谁负责什么、产出什么、什么时候进入下一阶段。

## 总体原则

AIUI 的第一版不要做大平台。

我们先验证一个核心假设：

> 给 AI coding agent 一份结构化 UI 意图规范，是否能显著改善它生成前端页面的质量。

所以第一版只做：

- AIUI Spec
- Pattern Graph
- Agent Handoff Pack
- React + Tailwind Adapter
- 轻量 Validate
- 3 个真实页面验证案例

第一版不做：

- 可视化画布
- 自动截图审美评分
- Figma 替代品
- 多框架代码生成
- 自动全网学习
- 完整组件库

## 阶段 0：产品边界确认

时间建议：1 到 2 天。

目标：

确认 AIUI 到底是什么，以及不是什么。

要做的事：

- 明确第一批用户：使用 AI coding agent 写前端的开发者
- 明确核心痛点：AI 写出来的 UI 丑、泛、乱、不像真实产品
- 明确产品边界：AIUI 是 UI 意图协议，不是 UI 框架
- 明确第一版技术栈：React + Tailwind adapter
- 明确验证指标：有 AIUI 是否比无 AIUI 更好

人负责：

- 定位
- 取舍
- 命名
- 产品边界

AI 负责：

- 总结竞品
- 整理用户痛点
- 草拟文档
- 生成验证问题清单

阶段产出：

- `docs/00-vision.md`
- `docs/04-v0.1-scope.md`
- `docs/02-product-architecture.md`

进入下一阶段的条件：

团队能用一句话说清楚 AIUI：

```text
AIUI 是让 AI coding agent 在写前端代码前先理解页面结构、设计约束和组件组合的 UI 意图协议。
```

## 阶段 1：设计知识研究

时间建议：3 到 7 天。

目标：

从优秀产品中提炼可复用的设计决策，而不是模仿具体品牌。

要做的事：

- 选择 10 个优秀产品或页面作为研究对象
- 拆解它们的布局、密度、导航、组件组合、层级、色彩策略
- 提炼 10 个常见页面 pattern 候选
- 提炼 20 个 component 候选
- 提炼 3 个 style profile 候选
- 整理第一批 AI UI 反模式

推荐研究对象：

- Linear
- Notion
- Vercel
- Stripe
- GitHub
- Raycast
- Figma
- Supabase
- Shopify
- Retool

研究时不要输出：

```yaml
brand: linear
```

应该输出：

```yaml
style_profile:
  id: precise-product-ui
  density: compact
  surface_style: flat
  border_strategy: subtle-lines
  color_strategy: restrained
  hierarchy: typography-and-spacing
```

人负责：

- 判断哪些规律值得进入 AIUI
- 去掉品牌模仿
- 统一命名
- 决定 v0.1 范围

AI 负责：

- 拆解参考页面
- 归纳页面结构
- 生成候选 pattern
- 整理差异和共性

阶段产出：

- 10 份设计案例笔记
- 第一批 component list
- 第一批 pattern list
- 第一批 brand profile list
- 第一批 anti-pattern list

进入下一阶段的条件：

我们不再凭空设计 AIUI，而是有足够真实产品规律作为输入。

## 阶段 2：AIUI Core Spec v0.1

时间建议：5 到 10 天。

目标：

建立第一版核心规范，让 AI 可以读懂页面意图。

要做的事：

- 定义 Foundation
- 定义 Tokens
- 定义 Components
- 定义 Patterns
- 定义 Pages
- 定义 Brand Profiles
- 定义 Rules 和 Avoid
- 定义命名规范
- 定义 Pattern Graph 依赖关系

核心文件：

- `spec/aiui-core-schema.md`
- `spec/naming-conventions.md`
- `spec/pattern-graph.md`
- `library/components.md`
- `library/patterns.md`
- `library/pages.md`
- `library/brand-profiles.md`

v0.1 数量目标：

- 20 个 components
- 10 个 patterns
- 5 个 pages
- 3 个 brand profiles

人负责：

- 决定核心对象模型
- 决定字段是否必要
- 决定抽象层级
- 决定什么太模糊、什么太具体

AI 负责：

- 补全 spec 草案
- 生成 YAML 示例
- 检查命名冲突
- 检查字段缺失
- 生成说明文档

阶段产出：

- 可阅读的 AIUI Core Spec
- 第一批 library 文档
- 第一批页面 YAML 示例

进入下一阶段的条件：

给 AI 一个 page spec，它能明显理解页面应该由哪些区域、pattern、component 组成。

## 阶段 3：Agent Handoff Pack

时间建议：3 到 5 天。

目标：

让 AIUI 可以被 Codex、Claude Code、Cursor 等真实 AI coding agent 使用。

要做的事：

- 设计 `.aiui/` 文件夹结构
- 写 agent instructions
- 写 React + Tailwind adapter
- 写 page spec 示例
- 写使用方式

建议结构：

```text
.aiui/
  project.aiui.yaml
  tokens.aiui.yaml
  page.aiui.yaml
  agent-instructions.md
  examples/
```

Agent 规则应该明确：

- 写代码前先读 AIUI
- 优先使用项目已有组件
- 不要自由改变页面结构
- 不要把产品页做成营销页
- 不要默认使用大卡片、渐变、玻璃拟态
- 遵守 density、layout、brand profile

阶段产出：

- `adapters/agent-handoff-template.md`
- `adapters/react-tailwind-adapter.md`
- `examples/order-management-page.aiui.yaml`
- `examples/saas-settings-page.aiui.yaml`
- `examples/ai-tool-landing-page.aiui.yaml`

进入下一阶段的条件：

开发者可以把 handoff pack 交给 AI agent，并让它根据 AIUI 实现页面。

## 阶段 4：轻量 Validate

时间建议：3 到 7 天。

目标：

确保 AIUI 规范本身不会乱。

这一阶段不是做审美审查。

Validate 只检查结构：

- 字段是否完整
- token 是否存在
- pattern 是否引用了不存在的 component
- page 是否缺少必要 region
- 是否有重复命名
- 是否有循环依赖
- brand profile 是否缺少关键字段

命令形态：

```bash
aiui validate
```

错误输出示例：

```text
AIUI validation failed

examples/order-management-page.aiui.yaml
  - Unknown component: status-badge
  - Missing required region: page-header
```

人负责：

- 决定哪些规则必须检查
- 决定错误信息是否清晰

AI 负责：

- 实现 validator
- 写测试用例
- 生成错误样例
- 检查 docs 和 examples 是否一致

进入下一阶段的条件：

AIUI 文件可以通过结构校验，后续扩展时不容易自相矛盾。

## 阶段 5：真实 Agent Benchmark

时间建议：5 到 10 天。

目标：

证明 AIUI 真的有用。

测试方式：

```text
A 组：直接让 AI agent 写页面
B 组：先给 AI agent AIUI spec，再让它写页面
```

第一批测试任务：

- 订单管理页
- SaaS 设置页
- AI 工具 landing page

评分维度：

- 页面结构是否合适
- 信息层级是否清晰
- 密度是否合理
- 组件是否一致
- 是否减少 AI 味
- 代码是否可继续维护

人负责：

- 盲评
- 记录主观但真实的设计问题
- 判断结果是否值得继续投入

AI 负责：

- 执行多轮生成
- 整理差异
- 归纳失败原因
- 把失败变成 spec 改进建议

阶段产出：

- benchmark prompts
- 有 AIUI 和无 AIUI 的输出对比
- 评分表
- 失败案例
- spec 改进列表

进入下一阶段的条件：

AIUI-assisted 结果明显更稳定，返工更少，页面更像真实产品。

## 阶段 6：产品化

时间建议：验证成功后再开始。

目标：

把 AIUI 从文档仓库变成开发者可用工具。

可能产品形态：

```bash
aiui init
aiui add-page order-management
aiui validate
aiui handoff codex
aiui handoff claude-code
```

可以做的模块：

- CLI
- Starter repo
- 文档站
- 示例项目
- Agent-specific handoff
- Project profile 生成

暂时仍然不建议做：

- 大型可视化编辑器
- 自动视觉审查平台
- Figma 替代品

阶段产出：

- CLI v0.1
- 文档站
- starter template
- AI agent 使用指南

进入下一阶段的条件：

一个新开发者可以在自己的项目里初始化 AIUI，并用 AI agent 基于 AIUI 生成更好的前端页面。

## 最小执行顺序

如果要尽快开始，不要同时做所有事情。

建议先做这 7 件：

1. 完成 `spec/aiui-core-schema.md`
2. 补全 20 个 components
3. 补全 10 个 patterns
4. 补全 3 个 brand profiles
5. 生成 3 个 page specs
6. 写 Codex / Claude Code handoff prompt
7. 做第一次有 AIUI 和无 AIUI 的对比实验

只要第 7 步证明有效，产品方向就成立。

