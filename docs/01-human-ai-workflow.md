# 人和 AI 的协作流程

AIUI 应该通过清晰的人机分工来开发。

人负责品味、标准、命名、范围和产品方向。AI 负责研究、起草、抽取、检查一致性、写示例和实现工具。

## 原则

```text
人 = 架构师和最终裁决者
AI = 研究员、起草者、分析员、文档员、工程师
```

AI 可以快速生成大量材料，但完全由 AI 生成的标准很容易变得普通、空泛且不一致。

## 协作闭环

```text
1. 人选择一个产品领域或页面类型
2. AI 研究优秀参考并提取规律
3. 人接受、拒绝、重命名或重塑 pattern
4. AI 编写 AIUI spec 和 examples
5. AI 检查缺失引用和命名冲突
6. 人用真实 AI coding agent 测试
7. 把失败案例转成新的规范规则
```

## 工作模式

### Research Mode

用 AI 分析现有产品、设计系统、截图或界面。

输出应该围绕：

- Layout
- Component composition
- Typography
- Spacing
- Density
- Color strategy
- Navigation model
- Interaction model
- What to avoid

目标不是“复制某个产品风格”，而是“抽取可复用的设计决策”。

### Specification Mode

用 AI 把已经确认的设计决策转成 AIUI 文件。

人决定：

- 命名
- 层级
- 必填字段
- 哪些 pattern 进入 v0.1
- 哪些表达太模糊
- 哪些表达太依赖实现

AI 编写：

- YAML 示例
- Markdown 说明
- 字段解释
- 一致性检查

### Agent Test Mode

用 AI coding agent 在有 AIUI 和无 AIUI 两种情况下生成前端页面。

比较：

- 布局质量
- 视觉一致性
- 代码可维护性
- 手动修复次数
- 页面是否像真实产品

### Improvement Mode

当 AI 生成的 UI 失败时，不要只修页面，也要修缺失的 AIUI 规则。

示例：

```text
失败：
settings 页面用了大面积营销卡片和 hero 标题。

AIUI 改进：
增加 settings-section pattern，要求紧凑分组、行内说明，禁止 hero 区域。
```

