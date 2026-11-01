# b3Ɛq ALOS™ Roadmap

## P0 — Domain foundation and ownership map
- [x] Recover and incorporate the existing ALOS charter from b3Ɛq Core portfolio documentation.
- [x] Establish product scope, exclusions and source-of-truth boundaries.
- [ ] Complete logistics domain ontology and canonical identifiers.
- [ ] Reconcile Core SCM, TMS and WMS capabilities and authoritative interfaces.
- [ ] Reconcile ComOS commerce-order and customer-facing logistics ownership.
- [ ] Complete EBMA capability-to-organ-system profile with evidence.

## P1 — Network and shipment event model
- [ ] Define network, node, partner, carrier, facility, asset, shipment, consignment, stop and handoff entities.
- [ ] Define canonical event envelope, event identity, ordering, timestamps, provenance and correlation.
- [ ] Define shipment lifecycle, milestone and exception state machines.
- [ ] Define event retention, replay and reconciliation policies.

## P2 — Visibility and exception management
- [ ] Build shipment/network visibility projections.
- [ ] Define milestone ingestion and partner event normalization.
- [ ] Implement exception classification, assignment, escalation and resolution.
- [ ] Establish proof-of-delivery and evidence capture contracts.

## P3 — Planning and simulation
- [ ] Define route, load, capacity and resource constraints.
- [ ] Add ETA and service-level prediction with uncertainty.
- [ ] Add scenario simulation and optimization benchmarks.
- [ ] Validate recommendations against operational constraints.

## P4 — Governed action orchestration
- [ ] Define action catalogue, policy gates and authorization model.
- [ ] Implement approval thresholds and human-in-the-loop controls.
- [ ] Define idempotency, retries, compensation and rollback for dispatched actions.
- [ ] Integrate approved actions through Core and n8n contracts.

## P5 — Partner APIs and adapters
- [ ] Define external partner API and event adapter standards.
- [ ] Implement Core SCM/TMS/WMS adapters only after contract verification.
- [ ] Define ComOS integration for customer order and service context.
- [ ] Add TaskBridge connectors only for explicit synchronization cases.

## P6 — Security, reliability and EBMA conformance
- [ ] Threat model and data classification.
- [ ] Identity, tenant isolation, authorization and secrets integration.
- [ ] Observability, service-level objectives and incident playbooks.
- [ ] Load, resilience, recovery and security tests.
- [ ] Evidence-backed EBMA conformance review.
- [ ] Release, upgrade, backup and rollback verification.

**Delivery rule:** roadmap completion requires committed artefacts and verifiable test or operational evidence. Documentation alone does not mean implementation is complete.
