# Software Development Guidelines

The key words "MUST", "MUST NOT", "REQUIRED", "SHALL", "SHALL
      NOT", "SHOULD", "SHOULD NOT", "RECOMMENDED",  "MAY", and
      "OPTIONAL" in this document are to be interpreted as described in
      [RFC 2119](https://www.ietf.org/rfc/rfc2119.txt).

## Introduction

The purpose of this document is to describe code development best practices and guidelines. We expect developers to adhere to these guidelines where applicable. Deviations from these guidelines should be explicitly stated.

## Table Of Contents

* [Licensing](#licensing)

* [Repository hosting and status](#repository-hosting-and-status)

* [Documentation](#documentation)
  * [How to write good narrative documentation](#how-to-write-good-narrative-documentation)
  * [How to write good code documentation](#how-to-write-good-code-documentation)

* [Code formatting](#code-formatting)

* [Source code branching](#source-code-branching)

* [Versioning](#commit-messages)

* [Commit messages](#commit-messages)

* [Testing](#testing)
  * [Unit tests](#unit-tests)
  * [Integration tests](#unit-tests)
  * [End-to-end tests](#end-to-end-tests)

* [Code reviews](#code-reviews)

* [Definition of done](#definition-of-done)

* [Deployment](#deployment)

* [Security auditing](#security-auditing)

## Licensing

Unless otherwise stated, the ICON Foundation requires open source code. The code must include an MIT license, Apache 2.0, or another license explicitly approved by the ICON Foundation. Businesses should use the Apache 2.0 license. If you don’t know what to choose, pick the MIT license.

## Repository hosting and status

Code repositories should be hosted on Github. Issue tracking must be made public. Rare exceptions may be made for security vulnerabilities or other sensitive matters. Public code repositories should be pushed to regularly.

## Documentation

All of the following must be documented:
* Classes, constructors, and functions
  * Describe inputs/arguments
  * Describe outputs/returns
  * Brief narrative description
* Architectures, algorithms, and services
  * Extensive narrative description of how they work
  * Diagrams where applicable

Code documentation lives in the code files, for example above a function. Narrative documentation lives outside the code files, for example a general knowledge base.

### How to write good narrative documentation

**Do**
* Keep the audience in mind.
* Treat the audience as you would a close friend. Tell them a story.
* Write succinctly and directly.
* Link to other pages for glossary terms and other supplementary information.
* Use analogy, example, and comparison to get points across.
* Think about how pages flow from one to the next.

**Don’t**
* Talk down to the audience.
* Assume the audience has prior knowledge on the subject.
* Require the audience to navigate through multiple pages to reach the important information.

### How to write good code documentation

**Do**
* Think of code documentation as a short guide on how to use a function.
* Apply [rubberducking](https://rubberduckdebugging.com) to documentation when explaining what the function does.
* Add a minimal code example showing how the function would be used.

**Don’t**
* Assume a vague description and type signature is sufficient.
* Assume that the code should speak for itself.

**Examples**
* [Tensorflow's Python3 implementation of tensorflow::softmax()](https://github.com/tensorflow/tensorflow/blob/v2.9.1/tensorflow/python/ops/nn_ops.py#L3829-L3867)

## Code formatting

Projects should adopt a code format style and adhere to it from project inception to maintain consistency in readability in the codebase. The adopted code format style should be explicitly stated somewhere in the project, such as the CONTRIBUTING.md file.

We recommend using one of the following styles:

* [Google (multiple languages)](https://google.github.io/styleguide/)
* [Uber's style guide for Golang](https://github.com/uber-go/guide/blob/master/style.md)
* [AirBnb’ style guide for React](https://airbnb.io/javascript/react/)
* [PEP-8, the official style guide for Python](https://peps.python.org/pep-0008/)

## Source code branching

Projects should adhere to a well-formed source code branching pattern. Projects should explicitly state their pull request submission, review, and approval process somewhere in the project, such as the CONTRIBUTING.md file.

We recommend using [Feature Branching](https://martinfowler.com/bliki/FeatureBranch.html). In this pattern, developers should follow these steps when branching:
1. Create a new Git issue when there is a feature or fix to be written that clearly defines what is needed and why. The Git issue is appropriately labeled, assigned, and given a milestone.
2. Create a new branch referencing that Git issue to develop the feature or fix.
3. Submit a pull request to merge back to the main branch upon completion of the feature or fix.
4. If possible, assign a reviewer to review the code of the pull request.

To minimize divergence between main branch and feature branches, features should be atomic and small enough to be able to merge back to main branch quickly. Features should also be small enough that the pull request to be reviewed is not burdensome to the reviewer. Large features can be broken into many smaller features.

For working within a given repository, please follow the branching conventions of that repository.

You may find that another source code branching pattern works better for you. The important thing is that development is tracked publicly via Git issues and pull requests.

### Branch protection

We recommend protecting long lived branches such that all changes require at least one reviewer and one approver. It may be the case that this requirement is too restrictive if changes take too long to get reviewed. For example, if a typo is being fixed, it probably doesn't need a review or approval. The [ship/show/ask](https://martinfowler.com/articles/ship-show-ask.html) methodology decreases restrictions so that changes to mainline are not always blocked pending review, but increases instability risk because it is up to the author to request for review and approval. For more information on code reviews, see [code reviews](#code-reviews).

### Example

__Issue__: "Architecture Diagram Guidelines #6"

__Branch name__: "feature/architecture-diagram-guidelines"

__Pull Request header__: "feature/architecture-diagram-guidelines" -> "main" => "#6 Create architecture diagram guidelines #7"

_Note that the first number in the Pull Request header references the issue number. The second number is associated with the Pull Request itself_

## Versioning

We use [semantic versioning](https://semver.org) and expect all releases to be tagged. See [version bumps](#version-bumps) for more information on how we do versioning.

We sometimes use pre-release labels to indicate that a version is unstable and might not satisfy the intended compatibility requirements. The pre-release labels we use include:

| Version state | Notation | Explanation |
| ------------- | -------- | ----------- |
| Alpha | -alpha | Testing phase. Sandbox usage. Breaking issues expected |
| Beta | -beta | Testing phase. Real-world usage. Breaking issues expected |
| Release candidate | -rc | Pre-release phase. Real-world usage. Breaking issues may be expected but are not identified |
| Release | _No extra notation_ | Release / ready phase. Real-world usage. No further changes expected to this version |

You may find that another versioning convention works better for you. The important thing is that releases are clearly and consistently tagged, and that versioning methodology is explicit. One alternative we recommend to consider is [calendar versioning](https://calver.org/).

## Commit Messages

We recommend to squash the commit history of a short-lived branch when merging to a long-lived branch.

We adopt our commit message format from [conventional commits](https://www.conventionalcommits.org/en/v1.0.0/). Commits MUST follow this format because it makes commit history easy to understand.

```
<type>(<optional scope>): <subject>
<BLANK LINE>
<body>
<BLANK LINE>
<footer>
```

Commit messages should use the [imperative mood](https://web.mit.edu/course/21/21.guide/m-impera.htm).

### Types

- **build**: Changes that affect the build system or external dependencies
- **chore**: Changes to the build process or auxiliary tools and libraries such as documentation generation
- **ci**: Changes to CI configuration files and scripts
- **docs**: Changes to the documentation
- **feat**: A new feature
- **fix**: A bug fix
- **perf**: A code change that improves performance
- **refactor**: A code change that neither fixes a bug nor adds a feature
- **revert**: Commit that reverts a previous commit
- **style**: Changes that do not affect the meaning of the code (white-space, formatting, missing semi-colons, etc.)
- **test**: Adding missing or correcting existing tests

### Scope

Scope is a section of the codebase, such as a package, as perceived by the person reading the changelog generated from commit messages. The list of supported scopes should be specified by the project.

#### Version bumps

Breaking changes append `!` to the type.

A release should only increase either SemVer major, SemVer minor, or SemVer patch. The SemVer number that gets increased by a release should only ever increase by 1.<br>
A release that contains one or more breaking changes increases SemVer major.<br>
A release that contains one or more `feat` commits increases SemVer minor.<br>
A release that contains one or more `fix` commits increases SemVer patch.

### Body

The purpose of the body is to provide context and relevant information for reviewers and future readers. The body should include the motivation for the change and contrast this with previous behavior.

### Footer
The footer should contain any information about **Breaking Changes** and is also the place to
reference GitHub issues that this commit **Closes**.

**Breaking Changes** should start with the word `BREAKING CHANGE:` with a space or two newlines. The rest of the commit message is then used for this.

### Examples

```
fix!(relay): fetch out of sync block

Receiver no longer assumes block confirmation occurs on a strict interval.

Closes #322
BREAKING CHANGE: Breaks client.PollingInterval
```

Reverts state the commit hash to be reverted in the commit message body.

```
revert(relay): fetch out of sync block

This reverts commit <hash>.
```

## Testing

We follow the [test pyramid scheme](https://martinfowler.com/articles/practical-test-pyramid.html) for testing. This includes unit tests, integration tests, and end-to-end tests.

**Note:** We require that each progress report and deliverable be comprehensively tested, complete with documentation describing how to reproduce test results.

### Unit tests

Unit tests ensure that individual units of code (ie method or class) work as intended. You should have a lot more unit tests than integration or end-to-end tests.

Every logical component should be tested. Tests should consider only the expected inputs and outputs, and not the internal implementation details. You do not need to test trivial code.

Unit tests should be written in isolation and run very fast so that they can be automated to run on commit. Any external dependency used by the system under test should be mocked.

A testing status badge at the top of the README.md file should be included that indicates the status of automated testing after automated build. We also recommend to include a code coverage badge.

### Integration tests

Integration tests ensure that individual modules work together as intended. Integration tests should be hermetic. To achieve this, we recommend only testing integration testing two individual modules and mocking any external dependencies of the two modules. Every interaction between two modules should be tested for every module.

### End-to-end tests

End-to-end tests automate user stories and should be designed to replicate as closely as possible what the user's way of interacting with the software is. Because end-to-end tests involve many interacting components, they may behave unexpectedly. They also may take significantly longer to run than unit or integration tests. Because they are slow and difficult to maintain, we recommend only having the bare minimum end-to-end tests and primarily relying on unit and integration tests. For frontend development, we prefer [Selenium](https://www.selenium.dev) or [Puppetteer](https://pptr.dev) for webdriver UI tests.

## Code reviews

Code reviews involve having another developer review code changes for the purpose of improving code health.

### What to look for

#### Style

Although CI automates away most style checks, the code review is one of the last quality gates before code gets merged into mainline.
Sometimes CI doesn't pick up on everything. The reviewer should check that the code is styled consistently with the rest of the project.

#### Functionality

Code changes should integrate well with the rest of the code base. They should logically flow and work as the author intends. The functionality should be properly tested and consider potential vulnerabilities and corner cases.

#### Documentation

The reviewer should ensure that the code is documented in accordance with the [documentation guidelines](#documentation) and the project-specific guidelines.

#### Complexity

Code changes should be as small and as simple as possible. The reviewer should consider whether the changes can quickly be understood, the likelihood that the changes introduce bugs when being called, whether the code is actually needed, and whether the code is over-engineering.

### How to review code

Reviewers should aim to improve code quality, but not so prohibitively that it discourages changes from being submitted. If the author can demonstrate that their changes are equally valid to a suggested alternative, the author's preference should be accepted.

#### Speed of code reviews

Code reviews turnaround should be within one business day. Slow code reviews decrease the speed of iteration and the entire project's development cycle.

#### Size of code reviews

Changes should be small and incremental enough that they can be reviewed quickly. 

## Definition of done

Feature addition code should be considered done **only after completing the following:**

- Code is [properly documented](#documentation)
- [All tests](#testing) are passed
- Code is [reviewed](#code-reviews) and approved
- Functional acceptance criteria are met
- Non-functional acceptance criteria are met
- Code is deployed to a specified environment

## Deployment

We prefer Docker containers to prevent issues with dependencies and versioning.

## Security Auditing

dApp code bases are not considered complete until audited by a reputable security auditor to minimize risk to the end user. Note that the operative word here is "minimizes," as it cannot be 100% guaranteed that a dApp will work as intended and not impact the end user negatively.
