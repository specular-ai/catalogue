# Project model

[Catalogue](../README.md)

Specification items and their relationships, organisation, and stated progress.

## Core information

ID categories and roles; IDs; definitions and references; relationships; features; modules; statuses and the occurrences assigning them.

## Sources and extraction

Markdown specifications, plans, task lists, and project conventions.

Configure ID patterns, definition/reference rules, relationship rules, status mappings, and feature/module membership. Configuration may be authored manually or proposed by an agent for review.

## Evidence and refresh

Each occurrence retains its file and source range. Definition, relationship, and status evidence should be inspectable. Occurrence indexes can be rebuilt when files change. Consumers should be able to identify the scope and version of the information they display. When sources change, affected information should be refreshed or marked as stale.

## Relationships to other models

References the physical model for locations and can link items to the code model.

## Consuming abstractions

- [Project map](../abstractions/project-map.md)
- [Project cards](../abstractions/project-cards.md)
- [Evidence coverage](../abstractions/evidence-coverage.md)
- [Feature dossier](../abstractions/feature-dossier.md)
- [Implementation traceability](../abstractions/implementation-traceability.md)
- [Evolution timeline](../abstractions/evolution-timeline.md)

These are the consumers in the initial catalogue; other abstractions may reuse this model.

## Example

REQ-001 is a requirement defined in requirements.md, referenced by TASK-008, assigned to the deletion feature, and marked implemented in tasks.md.

This example is illustrative.

## Limitations

Identifiers can be ambiguous or reused. Stated status is not verified implementation status.

## Scope

This is a conceptual model description, not a formal schema or a required storage format. Extractors and implementations may use different internal representations.
