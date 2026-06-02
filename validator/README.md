# AIUI Validate

AIUI Validate 用来检查 AIUI 文件的结构和一致性。

v0.1 不判断视觉美丑。

## 目标

防止 AIUI spec 随着增长变得不一致。

## 命令设计

```bash
aiui validate
```

## Validation Scope

Validate 应检查：

- File structure
- Required fields
- Naming conventions
- References
- Duplicate ids
- Circular dependencies
- Page completeness
- Brand profile completeness

## 不在范围内

Validate 不检查：

- 页面是否漂亮
- Screenshot quality
- 渲染后 UI 的视觉层级
- 代码实现质量

这些未来可以成为独立模块。

