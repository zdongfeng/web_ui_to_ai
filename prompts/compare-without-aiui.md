# Prompt：对比有无 AIUI

在生成两个版本后，用这份 prompt 帮助整理 benchmark 分析。

```text
Compare these two AI-generated frontend outputs:

A: Generated without AIUI
B: Generated with AIUI

Use this scoring rubric:

- Layout appropriateness
- Visual hierarchy
- Density control
- Component consistency
- AI slop avoidance
- Implementation readiness

For each category:

1. Score A from 1 to 5
2. Score B from 1 to 5
3. Explain the difference
4. Identify which AIUI rule helped or failed

End with:

- Total score A
- Total score B
- Most important improvement from AIUI
- Missing AIUI rule that should be added
```

