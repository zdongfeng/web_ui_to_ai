# AIUI Agent Instructions

写前端代码前先读取这些说明。

## Priority

遵循这个优先级：

1. 现有项目组件和约定
2. `.aiui/project.aiui.yaml`
3. `.aiui/pages/` 中的相关 page spec
4. `.aiui/tokens.aiui.yaml`
5. React + Tailwind adapter guidance
6. 通用前端判断

## Core Rules

- 先用 page spec 决定结构，再写 JSX。
- 优先使用现有项目组件。
- Product pages 应实用、聚焦任务。
- 不要把 product pages 做成 marketing pages。
- 不要添加 page spec 没要求的装饰性 sections。
- 不要使用 generic AI visual cliches，例如 purple gradients、glass panels、identical feature-card grids。
- 同时考虑 mobile 和 desktop。
- 如果 spec 不完整，做最小合理假设并说明。

## Implementation Flow

1. 识别 page type。
2. 识别 required patterns。
3. 识别 required regions。
4. 把 recommended components 映射到项目组件。
5. 按顺序实现 regions。
6. 完成前检查 avoid rules。

