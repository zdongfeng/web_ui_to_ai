# 开发路线图

这份路线图用于控制第一版范围，让它足够小、可构建、可验证。

## 阶段总览

```text
Phase 0: Alignment
Phase 1: Design research
Phase 2: Core spec v0.1
Phase 3: Agent handoff pack
Phase 4: Validate
Phase 5: Benchmark
Phase 6: Productization
```

## Phase 0: Alignment

目标：

在写太多文件前定义产品边界。

产出：

- 产品定位
- 非目标
- 目标用户
- v0.1 成功指标
- 第一版支持的技术栈

决策：

AIUI v0.1 服务那些使用 AI coding agent 写前端页面、希望 UI 更好但不想成为设计师的开发者。

## Phase 1: Design Research

目标：

从优秀产品和常见前端页面中提取可复用的设计决策。

产出：

- 10 份 design case notes
- 10 个 page pattern candidates
- 3 个 style profile candidates
- 第一批 anti-pattern list

关键原则：

研究设计决策，不复制品牌名称。

## Phase 2: Core Spec v0.1

目标：

创建第一版稳定 AIUI schema 和 library。

产出：

- Core schema
- Naming conventions
- 20 个 component specs
- 10 个 pattern specs
- 5 个 page specs
- 3 个 brand profiles

输出格式：

- Markdown 用于解释
- YAML 用于示例
- 未来用 JSON Schema 做校验

## Phase 3: Agent Handoff Pack

目标：

让 AIUI 能被真实 AI coding agent 使用。

产出：

- Agent instruction template
- React + Tailwind adapter
- 示例 `.aiui/` pack
- Codex 和 Claude Code 使用说明

成功标准：

开发者可以把 handoff pack 放进项目，然后让 agent 基于 spec 实现页面。

## Phase 4: Validate

目标：

防止 AIUI 随着增长变得自相矛盾。

产出：

- CLI 命令设计
- Validation rules
- Error message format
- 第一版实现计划

v0.1 只检查结构正确性。

## Phase 5: Benchmark

目标：

证明 AIUI 能改善 AI 生成前端的质量。

产出：

- 3 个 benchmark tasks
- 有 AIUI 和无 AIUI 的对比
- Scoring rubric
- Human review notes
- Failure analysis

成功指标：

AIUI-assisted 输出需要更少设计修正，并且页面结构更稳定。

## Phase 6: Productization

目标：

把已经验证有效的 spec 变成开发者可用产品。

可能产出：

- `aiui init`
- `aiui add-page`
- `aiui validate`
- `aiui handoff codex`
- 文档站
- Starter repository

在 benchmark 没证明价值之前，不进入产品化阶段。

