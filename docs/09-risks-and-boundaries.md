# 风险和边界

AIUI 很容易被做得过大。这份文档用于保持产品聚焦。

## 核心风险

最大的风险是：在证明 spec 有用之前，就把 AIUI 做成完整设计平台。

AIUI 第一阶段只需要证明：

```text
结构化 UI 意图能改善 AI 生成前端页面的质量。
```

其他能力都应该靠后。

## 风险 1：变成 UI Framework

AIUI 不应该和这些产品竞争：

- shadcn/ui
- Radix
- Ant Design
- Material UI
- Tailwind
- React Aria

边界：

```text
AIUI 描述设计意图，UI framework 负责实现组件。
```

## 风险 2：变成设计画布

AIUI 不应该一开始就竞争：

- Figma
- Claude Design
- Google Stitch
- v0
- Lovable

边界：

```text
AIUI 是 coding agent 可以读取的设计意图层。
```

## 风险 3：变成自动审美裁判

AIUI v0.1 不做截图审美评分。

边界：

```text
Validate 检查 spec 结构，不判断页面美不美。
```

视觉审查可以是未来可选模块，但必须等 spec 本身被证明有效之后。

## 风险 4：复制品牌

AIUI 可以学习优秀产品，但不能直接模仿品牌。

不推荐：

```yaml
brand: linear
```

推荐：

```yaml
brand_profile:
  id: precise-product-ui
  density: compact
  border_strategy: subtle-lines
```

边界：

```text
抽取设计决策，不复制品牌皮肤。
```

## 风险 5：过度抽象

如果 AIUI 太抽象，agent 会忽略它，或者随意解释。

不推荐：

```yaml
Card:
  radius: medium
```

更好：

```yaml
radius:
  md:
    value: 10
    usage: "cards, drawers, popovers"
    avoid:
      - "dense table rows"
      - "large landing hero regions"
```

边界：

```text
AIUI 应该框架无关，但不能模糊。
```

## 风险 6：让 AI 独自定义标准

AI 很适合研究和起草，但最终标准需要人的判断。

边界：

```text
AI 起草，人来裁决。
```

## v0.1 边界总结

要做：

- Spec
- Pattern graph
- Handoff pack
- React + Tailwind adapter
- 结构校验
- Benchmark

不要做：

- Visual canvas
- Screenshot beauty scoring
- Full code generation engine
- Figma replacement
- Multi-framework platform
- Brand-copy style packs

