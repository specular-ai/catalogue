# Agent activity model

[Catalogue](../README.md)

Observable activity during coding-agent work sessions.

## Core information

Sessions, activity events, tool calls and results, resource reads/writes, command executions, and links to conversation turns.

## Sources and extraction

Agent trajectories, session logs, and tool-event streams.

Adapt agent-specific events to a common representation; preserve ordering, outcomes, and the original event references.

## Evidence and refresh

Each normalised event links to its originating log record or tool result when available. Consumers should be able to identify the scope and version of the information they display. When sources change, affected information should be refreshed or marked as stale.

## Relationships to other models

References the physical model for workspace resources and the chat model for human-agent interactions.

## Consuming abstractions

- [Agent activity map](../abstractions/agent-activity-map.md)

These are the consumers in the initial catalogue; other abstractions may reuse this model.

## Example

A session records a file read, an edit, and an unsuccessful test invocation associated with a request.

This example is illustrative.

## Limitations

Instrumentation may not expose every action. An absent event does not establish that an action did not occur.

## Scope

This is a conceptual model description, not a formal schema or a required storage format. Extractors and implementations may use different internal representations.
