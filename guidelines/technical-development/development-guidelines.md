## Licensing

Unless otherwise stated, the ICON Foundation requires open source code. The code must include an MIT license, Apache 2.0, or another license explicitly approved by the ICON Foundation. If you don’t know what to choose, pick the MIT license.

## Deliverables

We value high-quality open source code, but even the most performant code is of little use if it lacks proper documentation.

We require that you document (where applicable):

API calls
Architecture overview and individual component details
Algorithms and protocols that are core to your project
Any other fundamental building blocks to your technology
Unless absolutely necessary, make the documentation public as well, ideally as part of the appropriate code repository. This will make it easier for the community to use or adapt your project.

Note: Only focus on your own contributions. Do not write detailed explanations of already existing components, e.g. IPFS.

For more information on our documentation standards, see documentation

## Source Code Branching

We suggest to use [Feature Branching](https://martinfowler.com/bliki/FeatureBranch.html). The developer should follow these steps:
1. Create a new Git issue when there is a feature or fix to be written that clearly defines what is needed and why. The Git issue is appropriately labeled, assigned, and given a milestone.
2. Create a new branch referencing that Git issue to develop the feature or fix.
3. Submit a pull request to merge back to the main branch upon completion of the feature or fix.
4. If possible, assign a reviewer to review the code of the pull request.

To minimize divergence between main branch and feature branches, features should be small enough to be able to merge back to main branch quickly. Features should also be small enough that the pull request to be reviewed is not burdensome to the reviewer. Large features can be broken into many smaller features.

You may find that another source code branching pattern works better for you. The important thing is that development is tracked publicly via Git issues and pull requests.

## Versioning

## Testing
