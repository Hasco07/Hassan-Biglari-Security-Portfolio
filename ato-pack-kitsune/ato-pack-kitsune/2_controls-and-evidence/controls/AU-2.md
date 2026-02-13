# AU-2 — Event Logging

## Summary
Kitsune defines and logs security-relevant events to support accountability, investigations, and continuous monitoring.

## Implementation
- **What:** Logon events, privilege changes, administrative actions, and data access events are logged.
- **How:** The application and OS generate logs; logs are forwarded to a central SIEM for retention and review.
- **Where:** Logs are generated on the web host and forwarded to the fictional SIEM.
- **Who:** SecOps monitors alerts; ISSO reviews evidence; Admins maintain log forwarding.
- **When / cadence:** Log review is performed weekly; alert triage occurs daily.

## Evidence
- `../evidence/logging-config-sample/log-source-list.md`
- `../evidence/logging-config-sample/log-forwarding-config.md`
- `../evidence/logging-config-sample/log-review-checklist.md`

## Common failure modes
- Missing proof of log forwarding/retention
- Logs exist but do not cover admin actions
- “Review” is claimed but no tickets/records exist
