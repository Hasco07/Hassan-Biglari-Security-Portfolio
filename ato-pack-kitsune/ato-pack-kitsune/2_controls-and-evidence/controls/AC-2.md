# AC-2 — Account Management

## Summary
Kitsune manages user and admin accounts through a defined process to ensure only authorized individuals have appropriate access.

## Implementation
- **What:** User and admin accounts are created, modified, and disabled through a documented request/approval workflow.
- **How:** Access is granted based on role, reviewed on a scheduled cadence, and removed promptly upon separation or role change.
- **Where:** Identity management occurs in the fictional IdP and is enforced by the web application.
- **Who:** System Owner approves role-based access; ISSO verifies evidence; Admins implement changes.
- **When / cadence:** Access reviews monthly; account disablement within a defined timeframe (fictional SLA).

## Evidence
- `../evidence/account-management-sample/access-review_{DATE}.md`
- `../evidence/account-management-sample/account-provisioning-workflow.md`

## Common failure modes
- Access reviews performed but not documented
- Privileged accounts not separated from standard user accounts
- Orphaned accounts after role changes

## Notes
All artifacts are fictionalized and demonstrate structure, not real system data.
