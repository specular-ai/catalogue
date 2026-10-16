# State machines

[Catalogue](../README.md)

A state machine showing states, transitions, events, and guards.

| Property | Description |
| --- | --- |
| Subject | Project |
| Purpose | Descriptive, constructive |
| Required models | [Semantic model](../models/semantic.md) |

## Developer question

How does component X behave?

## Representation and interaction

Select states and transitions to inspect evidence; in an editable implementation, change behaviour and review the corresponding artefact edits.

## Information and evidence

State and transition definitions, events and guards where available, and source mappings. The view should preserve navigation to supporting evidence and make unavailable information explicit.

## Example

A deletion flow moves from Idle to AwaitingConfirmation, then to Deleted on confirm or back to Idle on cancel.

This example is illustrative.

## Limitations

Distinguish specified behaviour from behaviour extracted from code. Editing a diagram alone does not reconcile an implementation.

## Scope

This entry describes an abstraction concept. It does not claim that a particular tool implements every interaction described here.
