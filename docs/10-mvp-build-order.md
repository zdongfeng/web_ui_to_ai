# MVP 构建顺序

这份文档定义文档阶段之后的实际构建顺序。

## MVP 原则

只构建能回答这个问题的东西：

```text
AIUI 是否能让 AI 生成的前端页面变好？
```

## Step 1：冻结 v0.1 核心对象

确认核心对象模型：

- Foundation
- Tokens
- Components
- Patterns
- Pages
- Brand Profiles

产出：

- 定版 `spec/aiui-core-schema.md`
- 更新命名规范

## Step 2：补全 Library 细节

当前 YAML 文件已经是 v0.1 draft。

下一步给每个文件补充：

- `use_when`
- `avoid_when`
- `related_patterns`
- `implementation_notes`
- `accessibility_notes`

产出：

- 完整 component specs
- 完整 pattern specs
- 完整 page specs

## Step 3：实现 Validator Prototype

实现：

- YAML parsing
- Required field validation
- Naming validation
- Reference validation
- Basic cycle detection

产出：

```bash
aiui validate
```

## Step 4：创建 Starter Project

创建一个小型 React + Tailwind 项目，包含：

- `.aiui/`
- 一个 order management 任务
- agent instructions
- 空实现区域

产出：

- 可复现 benchmark project

## Step 5：运行 Benchmark 1

运行：

- Without AIUI
- With AIUI

Agents：

- Codex
- Claude Code

产出：

- Screenshots
- Scores
- Failure notes

## Step 6：从失败中改进 Spec

每个失败都应该变成：

- 更好的 avoid rule
- 更清晰的 pattern
- 缺失的 component
- 更好的 adapter instruction

产出：

- AIUI v0.1 revision

## Step 7：决定产品化方向

如果 benchmark 证明有效：

- 做 CLI
- 做文档站
- 发布 starter kit

如果 benchmark 没证明有效：

- 降低抽象程度
- 改进 handoff instructions
- 增加更具体的 pattern examples

## MVP 退出标准

AIUI 满足这些条件后，才适合发布 public v0.1：

- Validator 能抓住常见 spec 错误
- 至少 3 个 benchmark tasks 证明有效
- Codex 和 Claude Code 能使用同一份 AIUI specs
- 新开发者能根据文档独立使用

