# Communication Guidelines

## Introduction

The purpose of this document is to describe best practices for communicating among project participants. We expect developers to adhere to these guidelines where applicable.

## README.md

All projects should include a README.md file that clearly and succinctly describes what the project is and how it is used. A visitor to the project should immediately be able to figure out

- what the project is
- who developed the project
- how to build the project, including supported development environments
- how to use the project
- supported features
- how to contribute, linking to a CONTRIBUTING.md file

### README badges

The README.md file should have information about the status of the project's code base. We recommend using badges to display this information. https://shields.io is a good place to generate badges from. Recommended badges include:

- code coverage
- continuous integration build status
- license SPDX identifier
- code quality report ie. OpenSSF scorecard and best practices

## CONTRIBUTING.md

All projects should include a CONTRIBUTING.md file that  specifies how a prospective contributor may get involved with the project. We recommend providing information about the following:

- Contributing code
- Contributing documentation
- Requesting features
- Reporting bugs
- Reviewing pull requests
- Participating in discussions

## Code contributor onboarding

All projects should have good first issues labeled so that prospective code contributors can onboard smoothly. We also recommend identifying in the documentation good entry points for stepping through the code base, such as specifying newcomer-friendly unit tests.

## Transparency

All projects should be unambiguously clear that they are open source. All projects should transparently and openly communicate development status as much as possible. Visitors should quickly know what the reality of the project's status is, how actively it is maintained, how often it puts out new releases, and how responsive it is to bug reports.

Developers should not inflate or hype the development status or misrepresent the project features. Open source projects set their own community expectations. Project owners should understand that conservatively managing expectation is always better for software and community health than risking not delivering on expectations. It's perfectly acceptable to state something along the lines of:

"This project is in alpha stage and is not representative of the final stage. Things may or may not work. We have a list of known bugs here \<LINK TO Github issues list\> and are still developing the project. We encourage users to raise issues and contribute by following our contributing guidelines at \<LINK TO CONTRIBUTING.MD\>."

Marketing should be mindful of its impact on the development community. Marketing should refrain from misleading project delivery dates, strengths, weaknesses, and attacking competitors.

## Handling security vulnerabilities

Security vulnerabilities should immediately be reported to the security response committee at [security@icon.foundation](mailto:security@icon.foundation). For more information about the security response committee and escalation process, check out their info [here](/committees/security-response-committee/SECURITY.md).

Unlike regular communications, security vulnerabilities should be discussed privately and handled silently to avoid alerting potentially malicious parties.

As demonstrated by [the Solana Wormhole exploit](https://research.kudelskisecurity.com/2022/02/03/quick-analysis-of-the-wormhole-attack/), even committing a fix announces the vulnerability's existence to the world. **The public should only be made aware of the security vulnerability after the fix is deployed to production.**

The formal announcement of the vulnerability should go out at the same time that the fix is released to the public.
