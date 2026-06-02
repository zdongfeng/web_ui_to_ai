# MVP Build Order

This document defines the practical build order after the documentation phase.

## MVP Principle

Build only what is needed to answer one question:

```text
Does AIUI make AI-generated frontend pages better?
```

## Step 1: Freeze v0.1 Spec Objects

Confirm the core object model:

- Foundation
- Tokens
- Components
- Patterns
- Pages
- Brand Profiles

Output:

- Finalized `spec/aiui-core-schema.md`
- Updated naming rules

## Step 2: Complete Library Details

The current YAML files are good v0.1 drafts.

Next, improve each file with:

- `use_when`
- `avoid_when`
- `related_patterns`
- `implementation_notes`
- `accessibility_notes`

Output:

- Complete component specs
- Complete pattern specs
- Complete page specs

## Step 3: Build Validator Prototype

Implement:

- YAML parsing
- Required field validation
- Naming validation
- Reference validation
- Basic cycle detection

Output:

```bash
aiui validate
```

## Step 4: Create Starter Project

Create a small React + Tailwind project with:

- `.aiui/`
- one order management task
- agent instructions
- empty implementation area

Output:

- A reproducible benchmark project

## Step 5: Run Benchmark 1

Run:

- Without AIUI
- With AIUI

Agents:

- Codex
- Claude Code

Output:

- Screenshots
- Scores
- Failure notes

## Step 6: Improve Spec From Failures

Every failure should become:

- A better avoid rule
- A clearer pattern
- A missing component
- A better adapter instruction

Output:

- AIUI v0.1 revision

## Step 7: Decide Product Direction

If benchmark improves output:

- Build CLI
- Create docs site
- Publish starter kit

If benchmark does not improve output:

- Reduce abstraction
- Improve handoff instructions
- Add more concrete pattern examples

## MVP Exit Criteria

AIUI is ready for public v0.1 when:

- The validator catches common spec errors
- At least 3 benchmark tasks show improvement
- Codex and Claude Code can both use the same AIUI specs
- A new developer can follow the docs without asking the authors

