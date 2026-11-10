# Upstream Integration Policy

## Purpose

Keep the Master Skill maintainable while benefiting from specialist public skill repositories.

## Integration methods

Prefer, in order:
1. Link to the upstream skill and provide a local routing note.
2. Adapt a short, original checklist that captures the relevant principle.
3. Vendor a full skill only when there is a strong operational need and its license permits it.

Do not copy large upstream files into this repository without checking license, attribution, and compatibility.

## Required provenance for any vendored/adapted module

Record:
- Upstream repository URL.
- Exact file path.
- Commit SHA or tagged release.
- Date inspected.
- License and required notices.
- Whether the content is linked, summarized, adapted or vendored.
- Local changes and rationale.

## Maintenance

- Re-check version-sensitive technical guidance when dependencies or provider APIs change.
- Re-check upstream links periodically.
- Do not claim a skill is official, endorsed, or maintained by its upstream author unless verified.
- Do not claim that an upstream repository has been fully audited when only selected files were inspected.
