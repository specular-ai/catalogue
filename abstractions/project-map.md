# Project map

[Catalogue](../README.md)

A navigable graph linking requirements, design decisions, and implementation tasks.

| Property | Description |
| --- | --- |
| Subject | Project |
| Purpose | Descriptive |
| Required models | [Project model](../models/project.md) |

## Developer question

Which tasks implement requirement X? Which design decisions address it?

## Representation and interaction

Filter by category, feature, module, or status; expand neighbours; follow a node or relationship to its supporting specification.

## Information and evidence

Typed IDs and explicit or configured relationships. Co-occurrence alone should not be presented as a confirmed dependency. The view should preserve navigation to supporting evidence and make unavailable information explicit.

## Example

REQ-001 requires confirmation before deletion. The map connects it to DES-003 (confirmation dialogue) and TASK-008 (implement the dialogue).

This example is illustrative.

## Limitations

A missing edge can mean missing documentation or extraction coverage, rather than a missing implementation.

## Scope

This entry describes an abstraction concept. It does not claim that a particular tool implements every interaction described here.
