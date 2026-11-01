# ALOS Domain Model — Initial Vocabulary

This is a starter vocabulary, not a finalized database schema.

| Concept | Meaning | Ownership guidance |
|---|---|---|
| Logistics Network | A coordinated set of participants, nodes, lanes and services | ALOS network context |
| Network Participant | Shipper, consignee, carrier, broker, 3PL, supplier or service partner | External identity mastered by source; ALOS maintains linked participant profile |
| Node | Operational location or transfer point | Source facility master remains authoritative |
| Lane | Permitted or planned connection between nodes | ALOS logistics network context |
| Shipment | Coordinated movement requirement or consignment grouping | Source order/transport system remains authoritative; ALOS links and projects |
| Consignment | Goods entrusted for transport under defined terms | Transport execution authority |
| Load | Capacity allocation to a vehicle/container/trip | TMS or transport execution authority |
| Stop | Planned or actual visit in a route | TMS/route execution authority |
| Handoff | Transfer of custody or responsibility between parties/nodes | ALOS coordinates evidence; source transaction remains authoritative |
| Milestone | Business-significant progress event | Source event with provenance; ALOS normalized projection |
| Exception | Deviation, risk or disruption requiring attention | ALOS coordination record linked to source case |
| Proof of Delivery | Evidence that delivery conditions were met | Delivery execution authority; ALOS evidence reference |
| Capacity | Available or committed resource capability | Owning fleet, carrier, warehouse or planning system |
| Recommendation | Proposed decision with rationale and confidence | ALOS intelligence output; not an executed action |
| Action | Authorized command to an owning system | Executed by authoritative target through controlled contract |

## Required identifiers

Use stable, namespaced identifiers for ALOS-owned records and retain source-system identifiers with source-system name, tenant, object type and version. Never overwrite a source identifier with an ALOS identifier.

## Event envelope requirements

Every normalized event should carry:
- event identifier and event type/version;
- source system and source record identifier;
- tenant or security boundary;
- occurred-at and received-at timestamps with timezone semantics;
- aggregate/entity identifier;
- correlation and causation identifiers where available;
- schema version and provenance;
- payload classification and integrity metadata.

## Lifecycle vocabulary

Shipment lifecycle states must be agreed with transport and order authorities. ALOS should not invent a competing transactional lifecycle. Its own coordination states may include observed, planned, at-risk, exception-open, awaiting-approval, action-dispatched, reconciled and closed, each with explicit transition rules.
