# Chat model

[Catalogue](../README.md)

Human-agent conversations from development sessions.

## Core information

Conversations, turns or messages, roles, ordering, content, and links to related activity where available.

## Sources and extraction

Conversation histories and agent-session records.

Import supported conversation formats while preserving roles, order, and message identifiers; record omissions and truncation.

## Evidence and refresh

Messages link to their originating conversation records and relevant excerpts. Consumers should be able to identify the scope and version of the information they display. When sources change, affected information should be refreshed or marked as stale.

## Relationships to other models

Connects conversational intent and explanations to events in the agent activity model.

## Consuming abstractions

- [Agent activity map](../abstractions/agent-activity-map.md)

These are the consumers in the initial catalogue; other abstractions may reuse this model.

## Example

A developer requests confirmation before deletion, and the agent explains its proposed change.

This example is illustrative.

## Limitations

An agent’s explanation is a recorded statement, not independently verified evidence of what was implemented.

## Scope

This is a conceptual model description, not a formal schema or a required storage format. Extractors and implementations may use different internal representations.
