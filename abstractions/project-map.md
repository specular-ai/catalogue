# Project map

[Catalogue](../README.md)

A navigable graph linking specifications, design decisions and implementation tasks through the references 
between their IDs.

| Property | Description |
| --- | --- |
| Subject | Project |
| Purpose | Descriptive |
| Required models | [Project model](../models/project.md) |

## Developer question

Which tasks implement requirement X? Which design decisions address it?

## Representation and interaction

The figures below show the Harbor example project, whose requirements, design decisions and delivery tasks are 
written in four Markdown files.

The focused view centres the graph on one ID and shows the IDs connected to it, as in the figure below. 
For example, REQ-001 is referenced by three design decisions (DD-001 to DD-003), which are in turn referenced by 
the delivery tasks that implement them (TASK-001 to TASK-005). The question "which tasks implement REQ-001?" is 
thus answered in two hops (task, design decision, requirement); a task that cites a requirement directly appears 
as a direct edge. Each node shows the ID's category and the file and line where it is defined, and its *Focus* 
action re-centres the graph on that ID. Below the graph, a connection list gives the same relations as text 
(e.g., "DD-001 references REQ-001 · 1 mention"); selecting a connection shows the lines that support it, each 
of which opens the source document.

![Focused project map centred on REQ-001, with three design decisions and five tasks](../figures/project_map_focus.png)

Additionally, an overview shows the entire graph: IDs are grouped by the document that defines them, and edges go 
from references to definitions.

![Project map overview with the IDs of the Harbor project grouped by file](../figures/project_map_overview.png)

## Information and evidence

Typed IDs and explicit or configured relationships. Co-occurrence alone should not be presented as a confirmed 
dependency. The view should preserve navigation to supporting evidence and make unavailable information explicit.

## Limitations

A missing edge can mean missing documentation or extraction coverage, rather than a missing implementation.

## Known implementations

This abstraction is currently implemented in [specular](https://github.com/specular-ai/specular).
