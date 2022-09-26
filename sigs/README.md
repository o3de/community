# O3DE Special Interest Groups

O3DE is a very large project. Special Interest Groups (SIGs) are the way we divide up the planning and communication for the different areas and responsibilities around developing and maintaining O3DE. 

## SIGs

Currently, O3DE has the following active SIGs:

|                                                                  |                                                                  |                                                          |
|------------------------------------------------------------------|------------------------------------------------------------------|----------------------------------------------------------|
| [SIG-Build](https://github.com/o3de/sig-build)                   | [SIG-Content](https://github.com/o3de/sig-content)               | [SIG-Core](https://github.com/o3de/sig-core)             |
| [SIG-Docs-Community](https://github.com/o3de/sig-docs-community) | [SIG-Network](https://github.com/o3de/sig-network)               | [SIG-Operations](https://github.com/o3de/sig-operations) |
| [SIG-Platform](https://github.com/o3de/sig-platform)             | [SIG-Graphics-Audio](https://github.com/o3de/sig-graphics-audio) | [SIG-Release](https://github.com/o3de/sig-release)       | 
| [SIG-Security](https://github.com/o3de/sig-security)             | [SIG-Simulation](https://github.com/o3de/sig-simulation)         | [SIG-Testing](https://github.com/o3de/sig-testing)       |
| [SIG-UI-UX](https://github.com/o3de/sig-ui-ux)                   ||                                                                  |                                                             | 

### How do I find out what a SIG owns?

To identify what a SIG owns or is working on, you can:
* Use the [Contributing](../CONTRIBUTING.md) guide for a quick overview of areas a SIG owns.
* Use the [Feature Grid](https://github.com/o3de/community/blob/main/features/Sample-FeatureMarkdown.md) to see areas of ownership and where a SIG may need help.
* Use the GitHub [Code Owners](https://github.com/o3de/o3de/blob/development/.github/CODEOWNERS) file, which shows the reviewer or maintainer groups that owns a particular area of O3DE.
* Or use the links above to look at the SIGs own documentation.
    * All SIGs have a **charter** document that covers what they own directly, what they own in conjunction with other SIGs etc. All SIGs maintain a charter document in their repository, typically under the `governance` folder or use the quick links in the [Contributing](../CONTRIBUTING.md) guide. 

### How do I get involved?

SIGs are open to all. You can join the discussion on [Discord](https://discord.gg/o3de) or attend any of the public meetings. Use the [O3DE Calendar](https://lists.o3de.org/g/o3de-calendar/calendar) to find upcoming SIG meetings.

Many SIGs have further information in the README files at the root of their repository.

#### Contributors, Reviewers and Maintainers

Everyone can be a contributor or developer of O3DE. They can write code and documentation that change the project. However, SIGs rely on reviewers and maintainers to ensure contributions to the project have value and align with the needs of the project. Its expected that there will be more contributors than reviewers, and more reviewers than maintainers

**Reviewers** are expected to have expertize in some parts of the project owned by a SIG, and to guide contributions to that SIG. They have the power to review code on behalf of a SIG. Its expected that reviewers also help contributors find any related work, understand O3DE's development practices and any SIG specific requirements for contributions.

**Maintainers** have all the power of a reviewer but are also responsible for merging changes in O3DE including ensuring automated reviews are run on a code contributions. Maintainers have final responsibility for changes that are merged. Maintainers can, under special circumstances, [bypass Automated Review checks](/contributors/docs/override_pr_status_check.md) for code submissions.

To become a reviewer or a maintainer for a SIG, see the process in [community-membership.md](/community-membership.md). You may also want to reach out to the Chair(s) of the relevant SIG to understand their processes and expectations around reviewers and maintainers.

## Process documents

* General [GitHub issue triage guide](../sigs/docs/sig-issues-triage-guide.md) for SIG maintainers.
* How to become a [reviewer or maintainer](../community-membership.md) for a SIG.
* [SIG chair elections process](../O3DE%20Elections/O3DE%20Elections%20Guide.md).
