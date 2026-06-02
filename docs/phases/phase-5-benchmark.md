# Phase 5：Benchmark

## 目标

证明 AIUI 能改善 AI 生成前端页面的质量。

## 测试方法

对每个 benchmark task：

```text
1. 不给 AIUI，让 AI agent 直接构建页面
2. 给同一个 agent AIUI，再构建同一页面
3. 用人工 rubric 比较结果
4. 记录失败
5. 把失败转成 spec 改进
```

## 第一批 Benchmark Tasks

- Order management page
- SaaS settings page
- AI tool landing page

## 测试 Agents

先测试：

- Codex
- Claude Code

之后再测试：

- Cursor
- Gemini CLI
- Windsurf
- Augment

## 评分

使用 `docs/05-validation-plan.md` 中的 rubric。

## 产出

- Benchmark prompts
- Generated outputs
- Human scores
- Failure notes
- Spec improvements

## 退出标准

AIUI-assisted 输出比 direct prompts 得分更高，且足以证明继续做 tooling 有价值。

