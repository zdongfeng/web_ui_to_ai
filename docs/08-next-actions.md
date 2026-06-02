# 下一步行动

这是当前文档整理完成后的立即执行清单。

## 优先级 1：补全 Core Library

继续细化：

- 20 个 components
- 10 个 patterns
- 5 个 pages
- 3 个 brand profiles

当前文件已经有高层结构，下一步需要补充更具体的 usage rules、avoid rules 和 YAML examples。

## 优先级 2：运行第一轮 Benchmark

使用这些 benchmark tasks：

- `benchmarks/tasks/order-management.md`
- `benchmarks/tasks/saas-settings.md`
- `benchmarks/tasks/ai-tool-landing.md`

每个任务执行：

1. 用 direct prompt 跑一次 AI
2. 用 AIUI-assisted prompt 跑一次 AI
3. 使用 `benchmarks/scoring-rubric.md` 给两组结果评分
4. 记录失败点
5. 更新 AIUI rules

## 优先级 3：构建 Validator Prototype

先实现：

- Parse YAML
- Validate required fields
- Validate naming
- Validate known component and pattern ids

不要实现 visual audit。

## 优先级 4：创建第一个 Starter Repo

创建一个最小 React + Tailwind app，包含：

- `.aiui/`
- 一个 page task
- Agent instructions
- Example generated implementation

## 优先级 5：确认产品名和公开表达

AIUI 适合作为工作名，但公开发布前需要确认：

- AIUI 是否是最终名称？
- Tagline 是否是 “UI intent protocol for AI coding agents”？
- 第一版发布 spec、CLI，还是 starter kit？

## 推荐下一步

不要先做 CLI。

最好的下一步是：

```text
补全详细 component 和 pattern library，然后运行第一轮 benchmark。
```

