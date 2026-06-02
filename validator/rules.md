# Validator Rules v0.1

这份文档定义 AIUI 的第一批 validation rules。

## Rule Groups

### 1. File Rules

Project AIUI pack 中必需文件：

```text
.aiui/project.aiui.yaml
.aiui/tokens.aiui.yaml
.aiui/agent-instructions.md
```

推荐文件：

```text
.aiui/pages/*.aiui.yaml
```

### 2. Naming Rules

所有 ids 必须：

- 使用小写
- 使用 hyphen-separated words
- 避免空格
- 避免框架名
- 避免品牌模仿名

无效：

```text
LinearDashboard
react-button
purple glass panel
```

有效：

```text
management-list
settings-section
precise-product-ui
```

### 3. Project Rules

`project.aiui.yaml` 必须定义：

- `project.id`
- `project.name`
- `project.register`
- `project.primary_users`
- `stack.frontend`
- `style.brand_profile`
- `style.density`
- `style.color_strategy`

### 4. Token Rules

`tokens.aiui.yaml` 应定义：

- `tokens.spacing`
- `tokens.radius`
- `tokens.typography`

推荐：

- `tokens.surfaces`
- `tokens.motion`

### 5. Page Rules

每个 page spec 必须定义：

- `page.id`
- `page.type`
- `page.register`
- `page.primary_user`
- `page.goal`
- `layout.structure`
- `layout.density`
- `patterns.required`
- `regions.required`

### 6. Reference Rules

Validator 应检查：

- 引用的 patterns 存在于 AIUI library
- 引用的 components 存在于 AIUI library
- 引用的 brand profiles 存在于 AIUI library 或 project pack
- 当 spec 使用显式 token ids 时，引用的 tokens 存在

### 7. Graph Rules

Validator 应拒绝：

- 循环依赖
- Components 依赖 pages
- Patterns 依赖 pages
- Unknown graph nodes

### 8. Avoid Rule Completeness

每个 page 和 brand profile 至少应该包含一个 `avoid` rule。

这有助于减少 generic AI UI output。

## Error Format

```text
AIUI validation failed

<file>
  - [rule-id] Human-readable error message
```

示例：

```text
AIUI validation failed

.aiui/pages/order-management.aiui.yaml
  - [page.required] Missing page.goal
  - [reference.pattern] Unknown pattern: record-table
```

