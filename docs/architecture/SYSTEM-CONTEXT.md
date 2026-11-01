# ALOS System Context and Architecture Boundaries

## Context

ALOS coordinates logistics across a network of shippers, consignees, carriers, warehouses, yards, ports, hubs, service providers, assets and enterprise systems. It correlates logistics activity into an operational view and supports planning, exception handling, simulation and governed actions.

## Logical capability layers

1. **Network registry:** participants, locations, facilities, nodes, lanes, capabilities and service calendars.
2. **Visibility and event ingestion:** normalize milestones and telemetry from internal and external sources.
3. **Operational coordination:** shipment lifecycle, handoffs, exceptions, escalation and work queues.
4. **Planning and optimization:** routing, load/capacity, resource allocation and scenario analysis.
5. **Intelligence:** ETA, risk, service-level prediction, recommendations and simulation.
6. **Action governance:** policy evaluation, approval, dispatch, outcome capture and reconciliation.
7. **Experience and integration:** user interfaces, APIs, event adapters and partner connectivity.

These are logical boundaries, not yet implemented deployable services.

## Integration context

- ComOS provides customer-facing commerce context and logistics offerings.
- Core provides shared enterprise capabilities and current SCM/TMS/WMS execution services.
- Future SCM Ultimate and TMS Ultimate products may provide specialized services after explicit contracts and migration decisions.
- n8n executes approved cross-system workflows.
- TaskBridge synchronizes records only where a defined mapping is preferable to native APIs/events.

## Design constraints

- Identify authoritative ownership for every entity and transaction.
- Distinguish source events from ALOS-derived projections.
- Use idempotent ingestion and action commands.
- Preserve event provenance, source timestamps and correlation identifiers.
- Treat external partner data as untrusted input.
- Separate recommendation from execution; require authorization and policy checks before consequential actions.
- Design for intermittent connectivity, delayed/out-of-order events and partner retries.
- Define tenant isolation and data residency before multi-tenant deployment.

## Deployment

The intended direction is self-hostable containerized services with independently scalable components. Nuxt 4 and Python are preferred technologies for relevant layers, not a mandate to force every component into one stack. Exact service topology and persistence technology require ADRs after workload and domain requirements are validated.
