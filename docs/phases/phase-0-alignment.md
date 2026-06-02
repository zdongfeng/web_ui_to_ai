# Phase 0: Alignment

## Goal

Define the product boundary and avoid building a product that is too large too early.

## Key Questions

- Who is the first user?
- What exact pain do they have?
- What is AIUI not going to do?
- Which agent workflows should v0.1 support?
- Which frontend stack should be used for validation?

## Decisions

### First User

Developers who mainly care about product logic and use AI agents to build frontend pages.

### Pain

AI-generated frontend pages are often generic, visually weak, and inconsistent.

### Product Boundary

AIUI provides a design intent spec and agent handoff workflow.

It does not provide a visual design canvas in v0.1.

### First Stack

React + Tailwind.

## Deliverables

- Vision document
- v0.1 scope document
- Product architecture document
- Initial repository structure

## Exit Criteria

The team can explain AIUI in one sentence:

```text
AIUI is a UI intent protocol that helps AI coding agents generate better frontend pages before they write code.
```

