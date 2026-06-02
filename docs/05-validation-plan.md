# Validation Plan

The first validation should prove that AIUI improves AI agent frontend output.

## Experiment Design

Use the same page requirement in two groups.

```text
Group A:
Prompt AI directly without AIUI.

Group B:
Give AI the AIUI spec, adapter instructions, and page spec first.
```

Each task should be run multiple times with the same agent or across different agents.

## First Benchmark Tasks

1. Order management page
2. SaaS settings page
3. AI tool landing page

These cover:

- Product UI
- Dense data UI
- Settings information architecture
- Brand/landing UI

## Evaluation Rubric

Score each output from 1 to 5.

### Layout Appropriateness

Does the page structure fit the task?

### Visual Hierarchy

Can users understand what matters first?

### Density Control

Is the page too empty, too crowded, or appropriate?

### Component Consistency

Are repeated elements visually and behaviorally consistent?

### AI Slop Avoidance

Does the page avoid generic AI visual patterns?

### Implementation Readiness

Is the code clean enough to continue building on?

## Success Criteria

AIUI succeeds if:

- Group B consistently scores higher
- Group B needs fewer manual design corrections
- Group B pages feel more like real product UI
- Different agents produce more similar structure when using the same AIUI spec

## Failure Analysis

Every failure should become a spec improvement.

Example:

```text
Observed failure:
The AI generated four identical cards for unrelated settings.

Spec improvement:
Add settings-section pattern with rows, grouped fields, inline descriptions, and optional danger zone.
```

