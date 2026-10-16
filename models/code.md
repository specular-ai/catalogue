# Code model

[Catalogue](../README.md)

The implementation’s structural elements and dependencies.

## Core information

Declarations such as classes, functions, and variables; signatures; calls; references; inheritance; and source locations.

## Sources and extraction

Source files and language-aware analysis results.

Use parsers, language services, or other analyses appropriate to supported languages; state the analysis scope and refresh after changes.

## Evidence and refresh

Declarations and relationships identify their source locations and, where relevant, the analysis that produced them. Consumers should be able to identify the scope and version of the information they display. When sources change, affected information should be refreshed or marked as stale.

## Relationships to other models

Uses physical locations; can be linked to project items and historical revisions.

## Consuming abstractions

- [Evidence coverage](../abstractions/evidence-coverage.md)
- [Implementation traceability](../abstractions/implementation-traceability.md)
- [Evolution timeline](../abstractions/evolution-timeline.md)

These are the consumers in the initial catalogue; other abstractions may reuse this model.

## Example

confirmDeletion() is declared in a source file and called by a deletion handler.

This example is illustrative.

## Limitations

Static analysis may miss dynamic relationships. Structural links do not demonstrate satisfaction of a requirement.

## Scope

This is a conceptual model description, not a formal schema or a required storage format. Extractors and implementations may use different internal representations.
