# 验证计划

第一轮验证要证明：AIUI 是否真的能改善 AI agent 的前端输出。

## 实验设计

同一个页面需求分成两组。

```text
Group A:
直接给 AI prompt，不提供 AIUI。

Group B:
先提供 AIUI spec、adapter instructions 和 page spec，再让 AI 实现。
```

每个任务可以用同一个 agent 多跑几次，也可以跨 agent 对比。

## 第一批 Benchmark Tasks

1. 订单管理页
2. SaaS 设置页
3. AI 工具 landing page

这三类覆盖：

- Product UI
- 高密度数据 UI
- Settings information architecture
- Brand / landing UI

## 评分维度

每项 1 到 5 分。

### Layout Appropriateness

页面结构是否适合任务？

### Visual Hierarchy

用户能否快速看出重点？

### Density Control

页面是否过空、过挤，或者密度合适？

### Component Consistency

重复元素是否一致？

### AI Slop Avoidance

是否避免了典型 AI 味？

### Implementation Readiness

代码是否足够清晰，能继续维护？

## 成功标准

AIUI 成功需要满足：

- Group B 持续高于 Group A
- Group B 需要更少手动设计修正
- Group B 页面更像真实产品
- 不同 agent 使用同一 AIUI spec 时结构更接近

## 失败分析

每个失败都应该变成一个 spec 改进。

示例：

```text
观察到的失败：
AI 把设置页做成了四个相同的大卡片。

Spec 改进：
增加 settings-section pattern，要求 rows、grouped fields、inline descriptions 和 optional danger zone。
```

