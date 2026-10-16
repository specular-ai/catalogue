# Implementation traceability

[Catalogue](../README.md)

A project map extended with links to implementation declarations, files, and relevant revisions.

| Property | Description |
| --- | --- |
| Subject | Project |
| Purpose | Descriptive |
| Required models | [Project model](../models/project.md), [Physical model](../models/physical.md), [History model](../models/history.md), [Code model](../models/code.md) |

## Developer question

Where is requirement X implemented?

## Representation and interaction

Follow requirement-to-code paths; inspect the evidence for a link; open source locations and associated changes.

## Information and evidence

Requirement/task identifiers, code declarations, revision data, and supported mappings between them. The view should preserve navigation to supporting evidence and make unavailable information explicit.

## Example

REQ-001 links through TASK-008 to confirmDeletion() and to the revision introducing the confirmation flow.

This example is illustrative.

## Limitations

A commit mentioning a requirement does not by itself establish that every changed declaration implements it. Distinguish explicit links from inferred ones.

## Scope

This entry describes an abstraction concept. It does not claim that a particular tool implements every interaction described here.
