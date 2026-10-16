# Agent activity map

[Catalogue](../README.md)

Three complementary views: sessions with interactions and tool use; resources with read/write intensity; and executed commands.

| Property | Description |
| --- | --- |
| Subject | Process |
| Purpose | Descriptive, analytical |
| Required models | [Agent activity model](../models/agent-activity.md), [Chat model](../models/chat.md) |

## Developer question

What is the agent doing, and where is it struggling? Is file X being read or written? Is tool X used routinely?

## Representation and interaction

Expand sessions and tool calls; filter resources and commands; inspect unsuccessful attempts alongside the conversation.

## Information and evidence

Session identifiers, ordered activity events, tool arguments/results, resource accesses, and conversation links where available. The view should preserve navigation to supporting evidence and make unavailable information explicit.

## Example

Repeated unsuccessful test commands appear beside edits to a module, with links to tool results and the developer’s request.

This example is illustrative.

## Limitations

Repeated attempts are a signal for inspection, not proof of confusion. Logs can be incomplete and may contain sensitive content.

## Scope

This entry describes an abstraction concept. It does not claim that a particular tool implements every interaction described here.
