# Phase 5: Benchmark

## Goal

Prove that AIUI improves AI-generated frontend output.

## Test Method

For each benchmark task:

```text
1. Ask an AI agent to build the page without AIUI
2. Ask the same agent to build the page with AIUI
3. Compare outputs with a human rubric
4. Record failures
5. Convert failures into spec improvements
```

## First Benchmark Tasks

- Order management page
- SaaS settings page
- AI tool landing page

## Agents to Test

Start with:

- Codex
- Claude Code

Later:

- Cursor
- Gemini CLI
- Windsurf
- Augment

## Scoring

Use the rubric in `docs/05-validation-plan.md`.

## Deliverables

- Benchmark prompts
- Generated outputs
- Human scores
- Failure notes
- Spec improvements

## Exit Criteria

AIUI-assisted outputs score higher than direct prompts often enough to justify building tooling.

