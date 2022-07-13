## Introduction

The purpose of this document is to describe code development best practices and guidelines. We expect developers to adhere to these guidelines where applicable.

## Licensing

Unless otherwise stated, the ICON Foundation requires open source code. The code must include an MIT license, Apache 2.0, or another license explicitly approved by the ICON Foundation. For businesses, we prefer Apache 2.0. If you don’t know what to choose, pick the MIT license.

## Documentation

We expect all of the following to be documented:
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

## Code Formatting

We suggest adopting a code format style and adhering to it from project inception to maintain consistency in readability in your codebase.

We recommend the following styles:
* [Google (multiple languages)](https://google.github.io/styleguide/)
* [Uber's style guide for Golang](https://github.com/uber-go/guide/blob/master/style.md)
* [AirBnb’ style guide for React](https://airbnb.io/javascript/react/)
* [PEP-8, the official style guide for Python](https://peps.python.org/pep-0008/)

## Source Code Branching

We suggest to use [Feature Branching](https://martinfowler.com/bliki/FeatureBranch.html). The developer should follow these steps:
1. Create a new Git issue when there is a feature or fix to be written that clearly defines what is needed and why. The Git issue is appropriately labeled, assigned, and given a milestone.
2. Create a new branch referencing that Git issue to develop the feature or fix.
3. Submit a pull request to merge back to the main branch upon completion of the feature or fix.
4. If possible, assign a reviewer to review the code of the pull request.

To minimize divergence between main branch and feature branches, features should be small enough to be able to merge back to main branch quickly. Features should also be small enough that the pull request to be reviewed is not burdensome to the reviewer. Large features can be broken into many smaller features.

You may find that another source code branching pattern works better for you. The important thing is that development is tracked publicly via Git issues and pull requests.

## Versioning

We use [semantic versioning](https://semver.org) and expect all releases to be tagged.

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

### Acceptance tests

## Deployment

We prefer docker

## Security Auditing

dApp code bases should be audited to minimize risk to the end user. Note that the operative word here is "minimizes," as it cannot be 100% guaranteed that a dApp will work as intended and not impact the end user negatively.
