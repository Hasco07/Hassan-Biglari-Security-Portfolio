# IA-2 — Identification and Authentication

## Summary
Kitsune uniquely identifies and authenticates users and administrators before granting access.

## Implementation
- **What:** Users authenticate via the fictional IdP; privileged access uses stronger authentication requirements.
- **How:** Role-based access is enforced after authentication; sessions are time-limited.
- **Where:** Authentication occurs at the IdP and is consumed by the web app.
- **Who:** Admins manage auth settings; ISSO verifies evidence; SecOps monitors anomalies.
- **When / cadence:** Authentication settings reviewed quarterly and after major changes.

## Evidence
- `../evidence/authentication-sample/auth-flow-description.md`
- `../evidence/authentication-sample/mfa-policy-summary.md`

## Common failure modes
- MFA policy not applied to privileged roles
- Missing proof of unique user IDs
- Session handling not documented
