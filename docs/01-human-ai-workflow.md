# Human and AI Collaboration Workflow

AIUI should be developed through a clear division of labor.

The human defines taste, standards, naming, scope, and product direction. AI helps with research, drafting, extraction, consistency checks, examples, and implementation.

## Principle

```text
Human = architect and final judge
AI = researcher, drafter, analyst, documenter, engineer
```

AI can produce a lot of material quickly, but standards created entirely by AI tend to become generic and internally inconsistent.

## Collaboration Loop

```text
1. Human chooses a product area or page type
2. AI researches strong references and extracts patterns
3. Human accepts, rejects, renames, or reshapes the pattern
4. AI writes AIUI spec files and examples
5. AI checks for missing references and naming conflicts
6. Human tests the spec with real coding agents
7. Failures are converted into improved rules
```

## Work Modes

### Research Mode

Use AI to analyze existing products, design systems, screenshots, or interfaces.

Output should be structured around:

- Layout
- Component composition
- Typography
- Spacing
- Density
- Color strategy
- Navigation model
- Interaction model
- What to avoid

The output should not be "copy this product's style." It should be "extract the reusable decision pattern."

### Specification Mode

Use AI to turn approved decisions into AIUI files.

Human decides:

- Names
- Hierarchy
- Required fields
- Which patterns belong in v0.1
- What is too vague
- What is too implementation-specific

AI writes:

- YAML examples
- Markdown references
- Field descriptions
- Consistency checks

### Agent Test Mode

Use AI coding agents to generate frontend pages with and without AIUI.

Compare:

- Layout quality
- Visual consistency
- Code maintainability
- Number of manual fixes
- Whether the page feels like a real product

### Improvement Mode

When an AI-generated UI fails, do not only fix the UI. Fix the missing AIUI rule.

Example:

```text
Failure:
The settings page used large marketing cards and a hero-style header.

AIUI improvement:
Add a product settings pattern with compact sections, inline descriptions, and no hero region.
```

