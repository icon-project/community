# SIG Infrastructure and Indexing Charter

| Status        | (Accepted)                                          |
:-------------- |:----------------------------------------------------|
| **PR Link**     | [](https://github.com/icon-project/community/pull/) |
| **Author(s)** | Rob Cannon (rob@sudoblock.io)                       |
| **Sponsor**   | Cyrus Vorwald (cyrus@icon.foundation)               |
| **Updated**   | 19 December 2022                                    |

This charter adheres to the [SIG governance guidelines](/guidelines/governance/sig-governance-guidelines.md).

## Overview

The Infrastructure and Indexing SIG is in charge of maintaining critical infrastructure for supporting the network including public RPC nodes and developing the community tracker. 

## Scope

Specific planning items are laid out in the [icon-tracker](https://github.com/sudoblockio/icon-tracker/tree/main/planning) repo with the following serving as the broad scope of the SIG.  

### Infrastructure 

The SIG oversees the community's public RPC endpoints which are running in at:

- https://api.icon.community/
- https://api.sejong.icon.community/
- https://api.lisbon.icon.community/
- https://api.berlin.icon.community/

These endpoints are running on optimized hardware and are instrumented with observability tooling to ensure high reliability. The SIG will outline and implement any changes to these endpoints in an effort to keep costs as low as possible and uptime as high as possible. It is also overseeing the open sourcing of the infrastructure stack so that users are able to contribute to the stack along with running their own API endpoints. 

### Indexing

The SIG oversees the community trackers which are running in at:

- https://tracker.icon.community/
- https://tracker.sejong.icon.community/
- https://tracker.lisbon.icon.community/
- https://tracker.berlin.icon.community/

These trackers are running in 2 regions with both dev and prod environments allowing developers to push changes to the appropriate cluster and see changes before they are ultimately pushed up into production. This SIG oversees these environments along with coordinating long term changes to the tracker. These improvements will be done by various teams across the community with this SIG serving as the planning point for implementing these changes. 

## Governance

This SIG adheres to the [SIG governance guidelines](/guidelines/governance/sig-governance-guidelines.md). 

Regular meetings will be planned on a monthly / quarterly basis to engage with the community for planning / feedback purposes. Meeting agendas will be made public and can be contributed to via PR in the [meetings](meetings) directory. Announcements for actual meeting dates / times will be made on [twitter](https://twitter.com/sudoblockio), Discord, and the [ICON Community Forum](https://forum.icon.community/). 

## Contacts

SIG chair & technical lead: [Rob Cannon](https://github.com/robcxyz)

Tracker discussions take place on a private discord channel. To gain access to the channel, please raise a support ticket in the [official ICON discord support channel](https://discord.gg/umYWjqz8mF).

## Projects

- [icon-tracker](https://github.com/sudoblockio/icon-tracker)
  - All associated repos are linked to from that repo in the [planning section](https://github.com/sudoblockio/icon-tracker/tree/main/planning)
  - Production infrastructure as code is private 
  - Docker compose version of the tracker can be used for development and local deployments 
- ICON Community Endpoints 
  - Production infrastructure as code is private
