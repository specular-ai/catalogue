# Domain model

[Catalogue](../README.md)

A class diagram representing domain concepts, attributes, and relationships.

| Property | Description |
| --- | --- |
| Subject | Project |
| Purpose | Descriptive, constructive |
| Required models | [Semantic model](../models/semantic.md) |

## Developer question

What are the domain concepts, properties, and relations underlying the application?

## Representation and interaction

Inspect concepts and their sources; in an editable implementation, change model elements and review the resulting artefact updates.

## Information and evidence

Diagram elements and relationships, source mappings, and, for editing, a supported notation and update policy. The view should preserve navigation to supporting evidence and make unavailable information explicit.

## Example

A domain diagram relates Project, Requirement, and Task. A developer adds an owner property to Task and reviews the corresponding diagram-source change.

This example is illustrative.

## Limitations

A domain concept need not correspond directly to an implementation class. Constructive use requires an injector; viewing a diagram does not imply editing support.

## Scope

This entry describes an abstraction concept. It does not claim that a particular tool implements every interaction described here.
