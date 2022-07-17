## Introduction

The purpose of this document is to describe software architecture design and decision making best practices and guidelines.
We expect developers to adhere to these guidelines where applicable.

## What is software architecture?

We define software architecture as the important decisions to be made regarding how and why a body of code is implemented.

## What is the purpose of a software architecture design document?

The purpose of a software architecture design document is to explicitly declare why a body of code works in the way it does.
This provides a baseline to align all stakeholders in understanding the internal workings of how the software works, what was considered,
and what important decisions were made.

## When is a software architecture design document needed?

A software architecture design document is needed any time there involves coordination across teams for a feature or body of code, either now or in the future.
If you are fixing a bug or making minor changes, you do not need a design document.

## What should be in a software architecture design document?

The following subsections should all be declared in a software architecture design document. We provide a template document at [software-architecture-design-template.md](https://github.com/icon-project/community/blob/6-architecture-design-guidelines/guidelines/technical-development/software-design-architecture-template.md).

### Introduction

The introduction should include the purpose and overview for this technical design. It should detail the problem and the reason for proposing a solution.
This problem description should be centered on the user perspective. The problem description should be understandable to the layman.
The introduction should be 1-2 paragraphs, and should contain minimal technical terms.

### Terminology

All variables and unclear technical terms used should be defined in this section. Please note that you do not need to pre-emptively list every
technical term in this section. However, as you fill out this document, evaluate which terms may be unclear and add them to this section with a
brief definition. Additionally, a collaborator on this document may add terms to this list if they find that it may benefit viewers of the document.
The terminology list should include acronyms as well as technical words or phrases.

### Considerations

The considerations should include the assumptions that are made, and the constraints that are faced. There may be multiple different considerations.
Considerations can include technical topics, user-experience topics, or other topics that the collaborators of this document view as pertinent to
understanding the design selection process.

### Designs

The designs section should contain proposed solutions. There may be one or more proposed solutions. Each proposed solution should have its own design,
defined in bold font. It should be clear which design was selected to move forward with implementation. The steps of the proposed solution should be
laid out in full sentences and should cover all major logically likely outcomes, including corner cases. If the proposed solution’s flow branches,
all cases should be clearly defined and stepped through. The steps of the proposed solution should also be written as pseudocode where applicable.

### Comparisons

Comparisons should be made between the designs laid out in the “Designs” section. Comparisons should be formatted in a table with the
appropriate major design aspects represented by table columns.

### Discussions

Discussions are artifacts of the clarifying design points that should be left for other contributors, advisors, or general viewers to
gain context into the decision-making process. Discussions should take place on a Github Discussions topic. It is preferable to have one
Github Discussions topic per Architecture Design document, but there may be additional side-topics if something specific is to be
discussed and it would be simpler to understand in its own topic.

## When should a software architecture design document be an ICON Improvement Proposal?

If the body of code impacts the core ICON blockchain, or the ICON developer community, it should be formatted and submitted as an
[ICON Improvement Proposal](https://github.com/icon-project/IIPs).
