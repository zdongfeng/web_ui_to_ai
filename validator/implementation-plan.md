# Validator 实现计划

Validator 应该在 v0.1 spec 基本稳定后实现。

## 推荐技术栈

第一版使用 Node.js。

原因：

- 方便通过 npm 分发 CLI
- YAML 解析简单
- 大多数前端开发者已有 Node 环境
- 与 React + Tailwind 验证实验天然匹配

## 推荐 Packages

- `yaml` 用于 YAML parsing
- `zod` 或 JSON Schema 用于结构校验
- 自定义小型 graph checker 用于依赖检查

## CLI 形态

```bash
aiui validate
aiui validate --path .aiui
aiui validate --strict
```

## 实现步骤

1. 加载 `.aiui/` 文件
2. 解析 YAML
3. 校验必填字段
4. 校验命名
5. 加载内置 library ids
6. 检查引用
7. 构建 graph
8. 检测 cycles
9. 打印错误
10. 校验失败时以 non-zero status 退出

## 第一批 Tests

创建 fixtures：

- valid project
- missing project fields
- unknown component reference
- unknown pattern reference
- circular pattern dependency
- invalid naming

## Future Strict Mode

Strict mode 可以检查：

- 每个 page 都有 avoid rules
- 每个 pattern 都有 usage 和 non-usage rules
- 每个 component 都有 states
- 每个 brand profile 都定义 motion

