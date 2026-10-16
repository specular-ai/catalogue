# Physical model

[Catalogue](../README.md)

The project’s file and folder structure and the locations of supporting artefacts.

## Core information

Folders, files, paths, file types, and locations or ranges within files.

## Sources and extraction

The project workspace and relevant repository snapshots.

Discover files within a defined scope; track creations, changes, renames, and deletions; make ignore rules explicit.

## Evidence and refresh

Locations identify the supporting file and range, with a revision or content version where needed. Consumers should be able to identify the scope and version of the information they display. When sources change, affected information should be refreshed or marked as stale.

## Relationships to other models

Provides location references for other models, especially project, code, and history.

## Consuming abstractions

- [Evidence coverage](../abstractions/evidence-coverage.md)
- [Feature dossier](../abstractions/feature-dossier.md)
- [Implementation traceability](../abstractions/implementation-traceability.md)
- [Evolution timeline](../abstractions/evolution-timeline.md)

These are the consumers in the initial catalogue; other abstractions may reuse this model.

## Example

requirements.md contains the definition of REQ-001 at an indexed source range.

This example is illustrative.

## Limitations

Paths and line ranges can become stale after edits or renames; historical locations require a revision context.

## Scope

This is a conceptual model description, not a formal schema or a required storage format. Extractors and implementations may use different internal representations.
