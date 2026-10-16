# Evidence coverage

[Catalogue](../README.md)

A coverage matrix relating objectives or requirements to documented implementation evidence.

| Property | Description |
| --- | --- |
| Subject | Project |
| Purpose | Analytical |
| Required models | [Project model](../models/project.md), [Code model](../models/code.md), [Physical model](../models/physical.md) |

## Developer question

Are there gaps in documented evidence of achieved objectives?

## Representation and interaction

Filter uncovered items; inspect the rule behind a finding; drill down to the exact source locations.

## Information and evidence

A stated coverage policy and trace links between specification items, code elements, and source locations. The view should preserve navigation to supporting evidence and make unavailable information explicit.

## Example

REQ-001 is marked implemented, but no linked declaration or other configured evidence is found. The matrix marks an evidence gap for investigation.

This example is illustrative.

## Limitations

Evidence coverage is not proof of correctness or completeness. Missing evidence and a failed requirement are distinct findings.

## Scope

This entry describes an abstraction concept. It does not claim that a particular tool implements every interaction described here.
