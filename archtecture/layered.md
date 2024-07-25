# Layered (or n-tiered) architecture

## Conway's law

Software architecture/design in an organization mimics the communication structures of the organization.

## General design

- n layers/tiers. Example: A web application with UX, business logic, persistence, and database layer.
  - natural separation of concerns.
- Technically-patitioned vs domain-partitioned architecture.
  - Each layer have a strict technical function.
  - The business domain logic (say checkout workflow) may be spread across multiple tiers and problems may be hard to debug.
- The layers could be closed or open. A closed layer means that a request must pass the layer when moving top to down i.e. a closed layer cannot be skipped even when it is acting just as a pass-through conduit. A open layer means that a request can skip the layer. An architecture can contain both closed and open layers but it is ideal to have most of the layerds as closed.

## Good

- Simple
- Well understood
- Low cost

## Anti-pattern

- Architecture by implication
- Accidental architecture
- Architecture sinkhole - majority of the requests are just passing through the layer without any functional impact.