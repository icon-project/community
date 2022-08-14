# SIG Interoperability Charter

| Status        | (Accepted)       |
:-------------- |:---------------------------------------------------- |
| **PR Link**     | [PR 43](https://github.com/icon-project/community/pull/43)|
| **Author(s)** | Cyrus Vorwald (cyrus@icon.foundation) |
| **Sponsor**   | Cyrus Vorwald (cyrus@icon.foundation) |
| **Updated**   | 08 August 2022 |

This charter adheres to the [SIG governance guidelines](/guidelines/governance/sig-governance-guidelines.md).

## Overview

We contribute to cross-chain message transfer and communication services through technical development and advocacy.

## Scope

### Guidance and technical expertise of ICON based interoperability solutions

We assist projects and companies looking to build cross-chain services and integrations.

### Standardized frameworks and best practices

We standardize and modularize integrations with the ICON Bridge where applicable. These ongoing and completed efforts include

- Merged code bases
- [Generalized multi-chain build framework architecture and implementation](https://github.com/icon-project/icon-bridge/discussions/192)
- [Generalized multi-chain functional test framework architecture](https://github.com/icon-project/icon-bridge/discussions/134)
- [Generalized multi-chain end-to-end test framework architecture and implementation](https://github.com/icon-project/icon-bridge/discussions/141)

We plan to optimize and share the entire continuous delivery pipeline in such a way that any integrating project can quickly onboard. These future plans include:

- Generalized multi-chain functional test framework implementation
- Reference specification and implementation of the ICON Bridge project
- Generalized multi-chain mock test framework architecture and implementation
- Easy configurations change (ie. new environment, artifcat)
- Generalized mult-chain deployment architecture and implementation. Deployed releases should have minimal downtime in any configured environment
- Standardized chain integration roadmap and quality gates. Any new chain integration to BTP should follow the same steps where applicable.
- Manual release checklist and production release readiness review template
- Generalized multi-chain logging and monitoring framework
- Standardized rollback procedures

### Out of scope

This special interest group currently does not include efforts of the Blockchain Transmission Protocol (BTP).

## Governance

This SIG adheres to the [SIG governance guidelines](/guidelines/governance/sig-governance-guidelines.md). Any changes from the guidelines should be noted here.

## Contacts

SIG chair & technical lead: [Cyrus Vorwald](https://github.com/CyrusVorwald-ICON)

## Projects

- [ICON Bridge](https://github.com/icon-project/icon-bridge)
    - Project lead: [Cyrus Vorwald](https://github.com/CyrusVorwald-ICON)
- [Nexus](https://github.com/icon-project/Nexus)
    - Project lead: [Cyrus Vorwald](https://github.com/CyrusVorwald-ICON)
