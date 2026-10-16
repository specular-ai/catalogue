# Project cards

[Catalogue](../README.md)

A dashboard of cards showing an item’s definition, occurrences, status, features, and modules.

| Property | Description |
| --- | --- |
| Subject | Project |
| Purpose | Descriptive |
| Required models | [Project model](../models/project.md) |

## Developer question

Where is requirement X defined or mentioned? What is its status and where was it set?

## Representation and interaction

Search and filter cards; open definitions and references; navigate to the location assigning a status.

## Information and evidence

ID categories, definition rules, status rules, and feature/module assignments. The view should preserve navigation to supporting evidence and make unavailable information explicit.

## Example

The REQ-001 card lists its definition in requirements.md, its references in design.md, and the task entry that declares it implemented.

This example is illustrative.

## Limitations

Different sources may assign conflicting statuses. Preserve those sources rather than silently choosing one.

## Scope

This entry describes an abstraction concept. It does not claim that a particular tool implements every interaction described here.
