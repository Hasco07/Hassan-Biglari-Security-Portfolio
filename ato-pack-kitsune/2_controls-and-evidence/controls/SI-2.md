# SI-2 — Flaw Remediation (Patching)

## Summary
Kitsune remediates software and OS flaws in a timely manner and tracks remediation status.

## Implementation
- **What:** Patch compliance is monitored and exceptions are tracked.
- **How:** Findings from scans and patch reports feed the POA&M; remediation is validated and documented.
- **Where:** Patch compliance reporting is stored as evidence; POA&M tracks status.
- **Who:** Engineering implements patches; ISSO tracks POA&M; ISSM escalates overdue risk.
- **When / cadence:** Patch compliance checked monthly; critical fixes prioritized (fictional policy).

## Evidence
- `../evidence/patch-compliance-sample/patch-compliance-summary.md`
- `../../3_poam/poam-sample.csv`

## Common failure modes
- “Patched” with no proof
- Exceptions not documented
- Scan results not reconciled with POA&M
