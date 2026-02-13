# AC-2 — Account Management

## Summary
Kitsune manages user and admin accounts through a defined process to ensure only authorized individuals have appropriate access.

## Implementation
- **What:** The system defines allowed vs. prohibited account types (e.g., allowed: individual user, privileged admin, auditor, service/DTA/L-DTA; prohibited by default: shared/group, anonymous, guest, temporary/emergency unless explicitly approved with conditions). 
- **How:** Accounts are requested, approved, provisioned, modified, disabled, and removed via a documented workflow with prerequisites for role/group membership (e.g., training, need-to-know, ticket/justification).
- **Where:** Central identity lifecycle is managed in the fictional IdP and enforced by the web application (role/attribute checks at authentication/authorization).
- **Who:** System Owner approves account creation and privileged role assignments; Account Managers/Admins execute changes; ISSO validates evidence and reviews compliance.
- **When / Cadence:** Accounts are reviewed at least annually (recommend quarterly for privileged/admin); accounts are disabled when no longer required, upon termination/transfer, policy violation, or inactivity.
- **Monitoring / Auditability** Accounts are reviewed at least annually (recommend quarterly for privileged/admin); accounts are disabled when no longer required, upon termination/transfer, policy violation, or inactivity (your 35-day rule fits here if documented).

## Evidence
- `../evidence/account-management-sample/access-review_{DATE}.md`
- `../evidence/account-management-sample/account-provisioning-workflow.md`

## Common failure modes
- Access reviews performed but not documented
- Privileged accounts not separated from standard user accounts
- Orphaned accounts after role changes

## Notes
All artifacts are fictionalized and demonstrate structure, not real system data.
