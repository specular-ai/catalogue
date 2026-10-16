# Semantic model

[Catalogue](../README.md)

Domain and behavioural concepts expressed in diagrams or other structured descriptions.

## Core information

Diagram types; concepts and properties; relationships; stories and journeys; states, transitions, events, and guards, according to the represented notation.

## Sources and extraction

Diagrammatic fenced blocks in Markdown and other sources interpreted by agents or parsers.

Parse supported diagram notations or use an agent to extract elements. Record the notation and distinguish explicitly stated elements from inferred ones.

## Evidence and refresh

Elements and relationships trace to diagram blocks or other supporting excerpts. Consumers should be able to identify the scope and version of the information they display. When sources change, affected information should be refreshed or marked as stale.

## Relationships to other models

Can link semantic concepts to project items and code elements when supported mappings exist.

## Consuming abstractions

- [Domain model](../abstractions/domain-model.md)
- [User stories](../abstractions/user-stories.md)
- [State machines](../abstractions/state-machines.md)

These are the consumers in the initial catalogue; other abstractions may reuse this model.

## Example

A state diagram defines Idle, AwaitingConfirmation, and Deleted and their transitions.

This example is illustrative.

## Limitations

Different notations express different semantics. An inferred model may require review before constructive use.

## Scope

This is a conceptual model description, not a formal schema or a required storage format. Extractors and implementations may use different internal representations.
