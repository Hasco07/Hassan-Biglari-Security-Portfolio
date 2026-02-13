# CM-2 — Baseline Configuration

## Summary
Kitsune maintains documented baselines for system components to reduce configuration drift and enable repeatable compliance.

## Implementation
- **What:** Baselines exist for OS configuration, installed software, and application settings (public-safe summaries).
- **How:** Baselines are version-controlled; changes follow the CM plan and are validated post-change.
- **Where:** Baseline documents live in this repo and/or in the fictional CMDB.
- **Who:** Engineering maintains baselines; ISSO verifies evidence; ISSM reviews high-risk changes.
- **When / cadence:** Baselines reviewed quarterly; after significant changes.

## Evidence
- `../evidence/change-control-sample/baseline_version_history.md`
- `../evidence/change-control-sample/change-ticket-example.md`

## Common failure modes
- Baselines exist but are outdated
- Changes implemented without documentation
- No proof of post-change validation
