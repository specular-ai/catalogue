# Catalogue of development abstractions

This catalogue introduces development abstractions for **abstraction-augmented agentic development (A³D)**: 
a method to help developers understand and steer software projects carried out with coding agents.

A **development abstraction** is a structured, task-oriented representation that selectively exposes relevant aspects 
of a software project or its development process. It may be visual and interactive. A **development model** supplies 
the information used by one or more abstractions, with traces to supporting evidence. Separating models from abstractions 
allows extraction to be reused across different views.

This repository contains an evolving catalogue of abstractions and development models. Entries describe 
concepts and illustrative interactions; they do not claim that all capabilities have been implemented in a 
supporting tool (like specular) or empirically validated. The catalogue is independent of a particular 
coding agent, development methodology, or plugin format. However, the plan is to provide support for this
catalogue in [specular's abstraction marketplace](https://github.com/specular-ai/specular-IDE).

## Conceptual model

The following Figure captures the main elements of abstractions and models.

```mermaid
classDiagram
    class DevelopmentAbstraction {
        name: String
        intent: String
        isReadOnly: Boolean
    }
    class Subject {
        <<enumeration>>
        PROJECT
        PROCESS
        BOTH
    }
    class Purpose {
        <<enumeration>>
        DESCRIPTIVE
        ANALYTICAL
        CONSTRUCTIVE
    }
    class DevelopmentModel
    class ModelExtractor
    class ProjectInjector
    class Trace
    class DevelopmentArtifact
    class CommitHistory
    class SourceFile
    class ChatHistory
    class MarkdownFile
    class AgentTrajectory

    DevelopmentAbstraction --> Subject : subject
    DevelopmentAbstraction --> Purpose : purposes
    DevelopmentAbstraction --> DevelopmentModel : requires
    DevelopmentModel --> ModelExtractor : built by
    ModelExtractor --> DevelopmentArtifact : extracts from
    DevelopmentModel *-- Trace : traces
    Trace --> DevelopmentArtifact : evidence
    DevelopmentModel --> ProjectInjector : optional update support
    ProjectInjector --> DevelopmentArtifact : updates
    DevelopmentArtifact <|-- CommitHistory
    DevelopmentArtifact <|-- SourceFile
    DevelopmentArtifact <|-- ChatHistory
    DevelopmentArtifact <|-- MarkdownFile
    DevelopmentArtifact <|-- AgentTrajectory
```

An abstraction requires one or more development models; each model can serve multiple abstractions. 
Extractors locate relevant information in development artefacts and populate models. Traces connect 
model information to its supporting evidence. Extractors may use configured algorithms, language models, 
or a combination of both.

An abstraction has a project, process, or combined subject and one or more purposes: 
**descriptive** (present selected information), **analytical** (derive findings), or 
**constructive** (express intended changes). Read-only abstractions can still support interaction 
and navigation. Editable abstractions delegate changes to models; where supported, project injectors 
propagate those changes to the corresponding artefacts.

For example, an extractor identifies requirements and tasks in Markdown specifications and records 
their relationships in a project model. A project map displays those relationships as a graph, 
while project cards display the same items as a dashboard. Both navigate back to the supporting sources.

## Development abstractions

The following table provides the current catalogue. 

| Abstraction | Developer question | Subject | Purpose | Required models |
| --- | --- | --- | --- | --- |
| [Project map](abstractions/project-map.md) | Which tasks implement requirement X? Which design decisions address it? | Project | Descriptive | [Project model](models/project.md) |
| [Project cards](abstractions/project-cards.md) | Where is requirement X defined or mentioned? What is its status and where was it set? | Project | Descriptive | [Project model](models/project.md) |
| [Evidence coverage](abstractions/evidence-coverage.md) | Are there gaps in documented evidence of achieved objectives? | Project | Analytical | [Project model](models/project.md), [Code model](models/code.md), [Physical model](models/physical.md) |
| [Feature dossier](abstractions/feature-dossier.md) | What is feature X about? | Project | Descriptive | [Project model](models/project.md), [Physical model](models/physical.md) |
| [Implementation traceability](abstractions/implementation-traceability.md) | Where is requirement X implemented? | Project | Descriptive | [Project model](models/project.md), [Physical model](models/physical.md), [History model](models/history.md), [Code model](models/code.md) |
| [Domain model](abstractions/domain-model.md) | What are the domain concepts, properties, and relations underlying the application? | Project | Descriptive, constructive | [Semantic model](models/semantic.md) |
| [User stories](abstractions/user-stories.md) | What user journeys are defined in the system? | Project | Descriptive, constructive | [Semantic model](models/semantic.md) |
| [State machines](abstractions/state-machines.md) | How does component X behave? | Project | Descriptive, constructive | [Semantic model](models/semantic.md) |
| [Evolution timeline](abstractions/evolution-timeline.md) | How did the project reach its current state? | Project and process | Descriptive, analytical | [Project model](models/project.md), [History model](models/history.md), [Code model](models/code.md), [Physical model](models/physical.md) |
| [Agent activity map](abstractions/agent-activity-map.md) | What is the agent doing, and where is it struggling? Is file X being read or written? Is tool X used routinely? | Process | Descriptive, analytical | [Agent activity model](models/agent-activity.md), [Chat model](models/chat.md) |

Each entry describes the developer question, representation and interaction, information and evidence, an illustrative example, and limitations. Constructive purposes describe intended editing capabilities, rather than a guarantee of editing support in any tool.

## Development models

| Model | Information represented |
| --- | --- |
| [Project model](models/project.md) | Specification items and their relationships, organisation, and stated progress. |
| [Physical model](models/physical.md) | The project’s file and folder structure and the locations of supporting artefacts. |
| [Semantic model](models/semantic.md) | Domain and behavioural concepts expressed in diagrams or other structured descriptions. |
| [Code model](models/code.md) | The implementation’s structural elements and dependencies. |
| [History model](models/history.md) | Repository evolution through revisions, changes, and development events. |
| [Agent activity model](models/agent-activity.md) | Observable activity during coding-agent work sessions. |
| [Chat model](models/chat.md) | Human-agent conversations from development sessions. |

Each model entry describes its core information, sources and extraction, evidence and refresh, relationships to other models, consuming abstractions, and limitations. These descriptions are conceptual and do not prescribe a formal schema or persistence format.

## Contributing to the catalogue

### How to read?

Start with the developer question closest to your task, then follow the required-model links to understand its 
information needs. 

### How to extend?

The catalogue is representative and open to extension. New abstractions should identify a concrete 
developer question, explain what they expose or allow a person to change, and state how their 
information traces to evidence. New models should explain what information they contribute and how 
it can be reused.

If you want to add a new abstraction or model, send a PR for us to review.

The plan is to provide support for this catalogue in [specular's abstraction marketplace](https://github.com/specular-ai/specular-IDE).


