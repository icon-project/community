This is a Work in Progress, documenting approximately how we have been operating up to this point.

# Principles

The ICON community adheres to the following principles:
* Open: ICON is open source. See repository guidelines, below.
* Welcoming and respectful: See Code of Conduct, below.
* Transparent and accessible: Work and collaboration should be done in public. See SIG governance, below.
* Merit: Ideas and contributions are accepted according to their technical merit and alignment with project objectives, scope, and design principles.

# Code of Conduct

The ICON community abides by the [ICON code of conduct](../code-of-conduct.md). Here is an excerpt:

_As contributors and maintainers of this project, and in the interest of fostering an open and welcoming community, we pledge to respect all people who contribute through reporting issues, posting feature requests, updating documentation, submitting pull requests or patches, and other activities._

As a member of the ICON project, you represent the project and your fellow contributors.
We value our community tremendously and we'd like to keep cultivating a friendly and collaborative
environment for our contributors and users. We want everyone in the community to have positive experiences.

# Community groups

The project is comprised of the following types of subgroups:
* Special Interest Groups, SIGs
  * Subprojects
* Working Groups, WGs
* Committees
* User Groups

![ICON Governance Diagram](../assets/structure/Group%20Relationship%20Diagram%20-%20ICON.jpg)

## SIGs

The ICON project is organized primarily into Special Interest
Groups, or SIGs. Each SIG is comprised of members from multiple
companies and organizations, with a common purpose of advancing the
project with respect to a specific topic, such as Networking or
Documentation. Our goal is to enable a distributed decision structure
and code ownership, as well as providing focused forums for getting
work done, making decisions, and onboarding new contributors. Every
identifiable subpart of the project (e.g., github org, repository,
subdirectory, API, test, issue, PR) is intended to be owned by some
SIG.

Areas covered by SIGs may be vertically focused on particular
components or functions, cross-cutting/horizontal, spanning many/all
functional areas of the project, or in support of the project
itself.

Examples:
* Project: Contributor Experience, Docs, Testing
* Horizontal: Interoperability
* Vertical: TBD

SIGs must have at least one and ideally two SIG chairs at any given
time. SIG chairs are intended to be organizers and facilitators,
responsible for the operation of the SIG and for communication and
coordination with the other SIGs, the Technical Steering Committee, and the
broader community.

Each SIG must have a charter that specifies its scope (topics,
subsystems, code repos and directories), responsibilities, areas of
authority, how members and roles of authority/leadership are
selected/granted, how decisions are made, and how conflicts are
resolved. SIGs should be relatively free to customize or change how they operate,
within some broad guidelines and constraints imposed by cross-SIG processes
(e.g., the release process) and assets (e.g., the ICON repo).

A primary reason that SIGs exist is as forums for collaboration.
Much work in a SIG should stay local within that SIG. However, SIGs
must communicate in the open, ensure other SIGs and community members
can find notes of meetings, discussions, designs, and decisions, and
periodically communicate a high-level summary of the SIG's work to the
community.

### Subprojects

Specific work efforts within SIGs are divided into **subprojects**.
Every part of the ICON code and documentation must be owned by
some subproject. Some SIGs may have a single subproject, but many SIGs
have multiple significant subprojects with distinct (though sometimes
overlapping) sets of contributors and owners, who act as
subproject’s technical leaders: responsible for vision and direction
and overall design, choose/approve change proposals (IIPs) ,
field technical escalations, etc.

Example subprojects for SIGs:
* SIG Interoperability: btp integration, ...

Subprojects for each SIG are documented in [sigs.yaml](../sigs.yaml).

## Working Groups

We need community rallying points to facilitate discussions/work
regarding topics that are short-lived or that span multiple SIGs.

Working groups are primarily used to facilitate topics of discussion that are in
scope for ICON but that cross SIG lines. If a set of folks in the
community want to get together and discuss a topic, they can do so without
forming a Working Group.

See [working group governance] for more details about forming and disbanding
Working Groups.

Working groups are documented in [sigs.yaml](../sigs.yaml).


## Committees

Some topics, such as Code of Conduct, require discretion. Whereas
SIGs are voluntary groups which operate in the open and anyone can join,
Committees do not have open membership and do not always operate in the open.
The steering committee can form committees as needed, for bounded or unbounded
duration.  Membership of a committee is decided by the steering committee,
however, all committee members must be community members.  Like a SIG, a
committee has a charter and a chair, and will report to the technical steering committee
periodically, and to the community as makes sense, given the charter.

## User groups
Some topics have long term relevance to large groups of ICON users, but
do not have clear deliverables or ownership of parts of the ICON
code base. As such they are neither good fits for SIGs or Working Groups.
An example of such a topic might be continuous delivery to ICON.

Though their central goal is not a deliverable piece of work, as contributing
members of the community user groups are expected to work with SIGs
to either identify friction or usability issues that need to be addressed,
or to provide or improve documentation in their area of expertise. However
these activities are covered under general code contributions to the relevant
SIGs (e.g. SIG Docs) rather than as part of the user group. These contributions
are expected to be more incremental and ad-hoc versus the more targeted
output of a user group.

User groups function as a centralized resource to facilitate communication and
discovery of information related to the topic of the user group. User groups
should not undertake to produce any deliverable, instead they should form
working groups under the auspices of some SIG for such work. Likewise they
shouldn't take ownership of anything in the ICON process, as that is a
role for SIGs. All user group chairs, and others that hold leadership positions
within a user group must be [community members].

See [user group governance] for more details about forming and disbanding
User Groups.

To facilitate discoverability and engagement,
user groups are documented in [sigs.yaml](../sigs.yaml)

## Cross-project Communication and Coordination

While most work shouldn’t require expensive coordination with other
SIGs, there will be efforts (features, refactoring, etc.) that cross
SIG boundaries.  In this case, it is expected that the SIGs coordinate
with each other and come to mutually agreed solutions. In some cases,
it may make sense to form a Working Group for joint work.  Cross-SIG
coordination will naturally require more time and implies a certain
amount of overhead.  This is intentional to encourage changes to be
well encapsulated whenever possible.

On the other hand, several SIGs do have project-wide impact, for
example Release, Testing, and API Machinery. Even those that do not
may sometimes need to make changes or impose new processes or
conventions that affect other SIGs. In these cases, project-wide
communication processes will need to be followed. For example,
proposals with project-wide impact will need to be announced more
broadly, with the opportunity for members of other SIGs to provide
feedback and guidance. However, the SIG that owns the area, according
to its charter, will own the decision. In the case of extended debate
or deadlock, decisions may be escalated to the Steering Committee,
which is expected to be uncommon.

The [IIP process](https://github.com/icon-project/iips) facilitates definition, agreement and communication of efforts that cross SIG boundaries.
SIGs are encouraged to use this process for larger efforts.
This process is also available for smaller efforts within a SIG.

# Repository guidelines

All new repositories under ICON github orgs should follow the process outlined in the [ICON technical development guidelines](../guidelines/technical-development/README.md).

Note that "ICON incubator" process has been deprecated in favor of the new guidelines.


[ICON code of conduct](../code-of-conduct.md)
[sigs.yaml](../sigs.yaml)