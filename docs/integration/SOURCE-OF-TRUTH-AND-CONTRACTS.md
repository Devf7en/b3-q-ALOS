# ALOS Source-of-Truth and Integration Contract Register

## Principles

- ALOS coordinates across domains; it does not silently seize ownership.
- Each entity and transaction has one declared authority per deployment.
- Integrations use documented, versioned APIs, events or explicit synchronization mappings.
- A projection is not an authoritative source record.
- Contract changes require consumer impact analysis, compatibility and migration notes.

## Initial ownership matrix

| Data / capability | Expected authority | ALOS responsibility |
|---|---|---|
| Customer, commerce order and customer-facing offer | ComOS or designated Core domain | Link to logistics execution context; show status |
| Inventory balance and stock transaction | Core SCM/WMS or designated inventory system | Consume availability/commitment events |
| Procurement and supply planning | Core SCM / future SCM Ultimate | Coordinate shipment and network context |
| Transport order, dispatch and freight execution | Core TMS / future TMS Ultimate | Correlate, visualize and coordinate exceptions |
| Warehouse receipt, pick, pack and shipment execution | Core WMS | Coordinate handoffs and consume milestones |
| Logistics network and cross-party visibility | ALOS | Own network coordination metadata and derived projections |
| Route/capacity optimization | TMS or ALOS by explicit deployment contract | Never allow two uncoordinated dispatch authorities |
| Accounting, invoice and settlement ledger | Finance authority | Consume references/status; no duplicate ledger posting |
| Workflow execution | n8n | Submit approved workflow requests and receive outcomes |
| Cross-system task synchronization | TaskBridge | Use only explicit mappings and conflict rules |

## Contract register (initial placeholders)

| Contract | Producer → consumer | Required semantics | Status |
|---|---|---|---|
| Commerce logistics context | ComOS → ALOS | Order reference, destination, service promise, consent/data policy | To define |
| Shipment milestone events | TMS/WMS/carrier → ALOS | Idempotent event IDs, provenance, timestamps, schema version | To define |
| Network participant and node references | Core/master data → ALOS | Stable IDs, ownership and lifecycle | To define |
| Planning request/result | ALOS ↔ TMS/SCM | Constraints, versioned request, explainable result | To define |
| Governed action command | ALOS → owning execution system | Authorization, idempotency, approval and outcome | To define |
| Workflow trigger/outcome | ALOS ↔ n8n | Correlation, retries, audit and no secret leakage | To define |
| Task/work synchronization | ALOS ↔ TaskBridge | Explicit field mapping, loop prevention, conflict policy | Optional; not designed |

No contract in this register should be treated as implemented until an interface definition, consumer/producer ownership and test evidence are committed.
