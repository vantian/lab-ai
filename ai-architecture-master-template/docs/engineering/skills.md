# Specialized Skills Registry

This registry maps task types to specialized agent workflows available in the
development environment. Remove entries that are unavailable.

| Task type | Skill or workflow | Required context | Expected output |
|---|---|---|---|
| Document creation | {{SKILL_NAME}} | Existing document and style requirements | Verified document artifact |
| Spreadsheet work | {{SKILL_NAME}} | Data source and expected calculations | Verified workbook |
| Presentation work | {{SKILL_NAME}} | Brief, audience, and brand requirements | Verified presentation |
| PDF work | {{SKILL_NAME}} | Source content and layout requirements | Rendered and verified PDF |
| Image generation | {{SKILL_NAME}} | Visual brief and reference images | Generated image asset |
| Browser testing | {{SKILL_NAME}} | Running application and target flow | Evidence-backed test result |

## Rules

- Use a skill only when it directly applies.
- Read the skill instructions before acting.
- Follow its required validation and delivery workflow.
- Keep task status and decisions in the existing task file.
- Do not copy full skill instructions into repository documentation.
