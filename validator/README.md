# AIUI Validate

AIUI Validate checks the structure and consistency of AIUI files.

It does not judge visual beauty in v0.1.

## Goal

Prevent the AIUI spec from becoming inconsistent as it grows.

## Proposed Command

```bash
aiui validate
```

## Validation Scope

Validate should check:

- File structure
- Required fields
- Naming conventions
- References
- Duplicate ids
- Circular dependencies
- Page completeness
- Brand profile completeness

## Not in Scope

Validate should not check:

- Whether a page looks beautiful
- Screenshot quality
- Visual hierarchy from rendered UI
- Code implementation quality

Those may become separate modules later.

