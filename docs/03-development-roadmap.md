# Development Roadmap

This roadmap keeps the first version small enough to build and test.

## Phase Overview

```text
Phase 0: Alignment
Phase 1: Design research
Phase 2: Core spec v0.1
Phase 3: Agent handoff pack
Phase 4: Validate
Phase 5: Benchmark
Phase 6: Productization
```

## Phase 0: Alignment

Goal:

Define product boundaries before writing too many files.

Deliverables:

- Product positioning
- Non-goals
- Target users
- v0.1 success metric
- First supported stack

Decision:

AIUI v0.1 serves developers who use AI coding agents to create frontend pages and want better UI without becoming designers.

## Phase 1: Design Research

Goal:

Extract reusable design decisions from strong products and common frontend page types.

Deliverables:

- 10 design case notes
- 10 page pattern candidates
- 3 style profile candidates
- First anti-pattern list

Important:

Study design decisions, not brand names.

## Phase 2: Core Spec v0.1

Goal:

Create the first stable AIUI schema and library.

Deliverables:

- Core schema
- Naming conventions
- 20 component specs
- 10 pattern specs
- 5 page specs
- 3 brand profiles

Output format:

- Markdown for explanation
- YAML for examples
- Future JSON Schema for validation

## Phase 3: Agent Handoff Pack

Goal:

Make AIUI usable by real AI coding agents.

Deliverables:

- Agent instruction template
- React + Tailwind adapter
- Example `.aiui/` pack
- Usage guide for Codex and Claude Code

Success:

A developer can copy the handoff pack into a project and ask an agent to implement a page from the spec.

## Phase 4: Validate

Goal:

Prevent the spec from becoming inconsistent as it grows.

Deliverables:

- CLI command design
- Validation rules
- Error message format
- First implementation plan

The validator only checks structural correctness in v0.1.

## Phase 5: Benchmark

Goal:

Prove that AIUI improves AI-generated frontend output.

Deliverables:

- 3 benchmark tasks
- With-AIUI and without-AIUI comparison
- Scoring rubric
- Human review notes
- Failure analysis

Success metric:

AIUI-assisted outputs should need fewer design corrections and show stronger layout consistency.

## Phase 6: Productization

Goal:

Turn the validated spec into a usable developer product.

Possible deliverables:

- `aiui init`
- `aiui add-page`
- `aiui validate`
- `aiui handoff codex`
- Documentation site
- Starter repository

Do not start this phase before benchmark results show real value.

