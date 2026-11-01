# ALOS Security and Operational Requirements

## Security baseline

- Authenticate every user, service and partner integration.
- Enforce tenant isolation and least-privilege authorization.
- Keep credentials, tokens and private keys outside source control.
- Integrate with the approved b3Ɛq secrets architecture when available.
- Validate, normalize and constrain all external partner payloads.
- Protect shipment location, customer, commercial and personnel data according to classification and applicable jurisdiction.
- Audit privileged actions, approvals, dispatch commands and administrative changes.
- Define retention and deletion rules for telemetry, events, location and proof-of-delivery evidence.
- Apply rate limits, replay protection and abuse detection to partner-facing interfaces.

## Action safety

Recommendations must be distinct from commands. A command that changes dispatch, carrier assignment, route, custody, inventory or delivery promise must:
1. identify the authoritative target system;
2. validate permissions and business policy;
3. require human approval where risk thresholds demand it;
4. carry idempotency and correlation identifiers;
5. record the request, approval, execution response and reconciliation outcome.

## Reliability

Design for delayed, duplicate, out-of-order and missing events; partner outages; intermittent connectivity; retry storms; and partial completion. Define back-pressure, dead-letter handling, replay and recovery procedures before production.

## Operational evidence required

- Threat model and security test results.
- Service-level objectives and alert thresholds.
- Backup, restore and disaster-recovery test evidence.
- Load and resilience tests.
- Dependency and container image scanning.
- Software bill of materials (SBOM) and release provenance.
- Incident response and escalation playbooks.

No production security or reliability posture is claimed by this requirements document.
