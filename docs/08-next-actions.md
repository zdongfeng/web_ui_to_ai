# Next Actions

This is the immediate execution checklist after the current documentation pass.

## Priority 1: Complete Core Library

Fill in detailed specs for:

- 20 components
- 10 patterns
- 5 pages
- 3 brand profiles

Current files are high-level. They need concrete usage rules, avoid rules, and YAML examples.

## Priority 2: Run First Benchmark

Use the benchmark tasks:

- `benchmarks/tasks/order-management.md`
- `benchmarks/tasks/saas-settings.md`
- `benchmarks/tasks/ai-tool-landing.md`

For each task:

1. Run direct prompt with AI
2. Run AIUI-assisted prompt with AI
3. Score both using `benchmarks/scoring-rubric.md`
4. Record failures
5. Update AIUI rules

## Priority 3: Build Validator Prototype

Start with:

- Parse YAML
- Validate required fields
- Validate naming
- Validate known component and pattern ids

Do not implement visual audit.

## Priority 4: Create First Starter Repo

Create a minimal React + Tailwind app that includes:

- `.aiui/`
- One page task
- Agent instructions
- Example generated implementation

## Priority 5: Decide Product Name and Public Framing

AIUI is useful as a working name, but before public release decide:

- Is AIUI the final name?
- Is the tagline "UI intent protocol for AI coding agents"?
- Is the first release a spec, CLI, or starter kit?

## Recommended Next Step

Do not start with the CLI.

The next best step is:

```text
Complete the detailed component and pattern library, then run the first benchmark.
```

