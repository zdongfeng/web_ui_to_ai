# AIUI Benchmark 评分表

每个维度 1 到 5 分。

1 表示很差，5 表示很强。

## 1. Layout Appropriateness

页面结构是否适合任务？

1 分：

- 页面类型错误
- Product UI 被做成 marketing layout
- 缺少关键区域

3 分：

- 结构大体正确
- 有些缺失或多余 section

5 分：

- 结构直接支持用户工作流
- Required regions 清晰
- 没有无关 section

## 2. Visual Hierarchy

用户能否理解什么最重要？

1 分：

- 所有元素权重接近
- 重要操作被埋没
- 标题和内容互相抢层级

3 分：

- 有基本层级
- 局部分组不清楚

5 分：

- 主任务明显
- Sections 易读
- 操作位置符合预期

## 3. Density Control

界面是否过空、过挤，或密度合适？

1 分：

- Product UI 过于稀疏
- 拥挤到难以扫描
- 间距随机

3 分：

- 可用，但 density 不均匀

5 分：

- Density 匹配任务和用户场景
- Spacing rhythm 有意图

## 4. Component Consistency

重复元素是否一致？

1 分：

- 按钮、卡片、字段、表格、badge 不一致
- 类似操作长得不一样

3 分：

- 大体一致
- 少数 variant 不匹配

5 分：

- Components 像同一个系统
- Variants 与语义对应

## 5. AI Slop Avoidance

是否避免了典型 AI UI 套路？

1 分：

- Generic gradient background
- Identical icon card grid
- Fake hero metrics
- Decorative glass panels

3 分：

- 有一些 generic choices，但不占主导

5 分：

- 界面针对具体产品任务
- 没有明显 AI 生成套话和视觉套路

## 6. Implementation Readiness

开发者是否能继续维护？

1 分：

- 结构混乱
- 视觉硬编码严重
- Responsive behavior 很差

3 分：

- 可用，但需要一些 cleanup

5 分：

- 结构清晰
- Components 和 regions 可维护
- 考虑了 responsive behavior

## 总分

最高分：

```text
30 points
```

如果 AIUI-assisted 输出稳定比 direct 输出高至少 5 分，可以认为 AIUI 有继续验证价值。

