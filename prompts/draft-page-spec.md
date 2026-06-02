# Prompt：起草 Page Spec

当你需要 AI 根据产品需求起草 AIUI page spec 时，使用这份 prompt。

```text
Draft an AIUI page spec for the following product requirement.

Requirement:
<paste requirement>

Use this structure:

page:
  id:
  type:
  register:
  primary_user:
  goal:

brand_profile:

layout:
  structure:
  density:

patterns:
  required:
  optional:

regions:
  required:
  optional:

components:
  recommended:

content_requirements:

avoid:

Rules:
- Keep the spec framework-neutral.
- Do not use brand imitation names such as apple, notion, or linear.
- Choose patterns from the AIUI library when possible.
- Add avoid rules that prevent generic AI UI output.
- Prefer product-specific structure over decorative layout.
```

