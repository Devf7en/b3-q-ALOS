# ADR-0001: ALOS Domain Boundaries and Execution Ownership

- **Status:** Accepted as initial design boundary; validate against actual Core contracts.
- **Date:** 2026-11-01
- **Portfolio ID:** B3EQ-PORT-0013

## Context

The ALOS charter describes a network-wide logistics operating system. The ecosystem already contains commerce, supply-chain, transport and warehouse capabilities in ComOS and b3Ɛq Core. Duplicating these functions would create competing sources of truth and operational risk.

## Decision

ALOS owns logistics network coordination, cross-party visibility, normalized event projections, logistics planning/simulation capabilities assigned by explicit contract, exception coordination and governed autonomy. ComOS owns commerce context and customer-facing offers. Core SCM/TMS/WMS remain the current specialized execution authorities in integrated deployments until separately governed successor products and migrations are approved.

## Consequences

- ALOS must declare data ownership and source provenance for every entity and event.
- It must not post duplicate accounting, inventory, transport or warehouse transactions.
- ALOS actions are dispatched to the authoritative target system through authorized, idempotent contracts.
- Core module extraction or replacement requires a separate migration and cutover decision.
- Contract definitions and integration tests are prerequisites to production integration.

## Review trigger

Revisit when Core SCM/TMS/WMS contracts are inspected, or when SCM Ultimate/TMS Ultimate establish their own verified service boundaries.
