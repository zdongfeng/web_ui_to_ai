# Phase 4：Validate

## 目标

保持 AIUI spec 内部一致。

## Validation Rules

v0.1 validation 应检查：

- 必填字段存在
- 名称符合约定
- 引用的 components 存在
- 引用的 patterns 存在
- 引用的 tokens 存在
- 没有重复 identifiers
- 没有循环依赖
- page specs 包含必要 regions
- brand profiles 定义 density、color strategy、surface strategy、typography 和 avoid rules

## Validate 不做什么

它不做：

- 判断美不美
- 读取截图
- 给视觉设计打分
- 自动修复前端代码

## CLI 概念

```bash
aiui validate
```

可能输出：

```text
AIUI validation failed

pages/order-management.aiui.yaml
  - Unknown component: status-badge
  - Missing required region: page-header

patterns/management-list.aiui.yaml
  - Circular dependency detected: management-list -> data-table-workspace -> management-list
```

## 产出

- Validation rule list
- Error message format
- Implementation plan
- Future JSON Schema plan

## 退出标准

Spec 可以继续增长，同时不容易出现内部不一致。

