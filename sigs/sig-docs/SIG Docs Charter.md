# Documentation and Community SIG Charter

## Overview of SIG

The Documentation and Community SIG (“the SIG”) maintains the content of the official O3DE website, the publishing infrastructure for the site, API reference building pipelines, and other community resources. Broadly, the team is responsible for:

* Contents of the Open 3D Engine user guide
* Documentation for core Gems that ship with Open 3D Engine, including the Atom renderer
* Minimum viable API documentation standards
* Documentation requirements for engineering contributions
* Official blogs, samples, demos, tutorials, and training
* Managing forums, Discord, and other community engagement channels

The SIG is *not* responsible for maintaining and writing all documentation. It's expected that engineers will write appropriate minimum viable documentation for each feature that they submit, though the SIG members may assist with review, editorial, and cleanup after the initial draft.


## Goals

Goals are divided by category.


### Documentation goals

* Handle issues reported with the documentation of O3DE.
* Produce and manage official blog posts, samples, tutorials, demos, and training.
* Manage official documentation releases.
* Maintain infrastructure related to the O3DE site such as publishing pipelines and analytics.
* Maintain documentation build tasks contained in the main O3DE repo, for APIs and other supplementary documentation.
* Lead cross-cutting efforts requiring the involvement of other SIGs in review and accuracy of documentation.

### Community goals

* Maintain and moderate community communication channels such as forums and Discord.
* Represent the interests of the community at large in all official O3DE business.
* Maintain the website UX.
* Manage contests, events, meetups, conferences, webinars, and other community-focused engagements.

## Scope

* Sets the standards for feature documentation and provides clear paths for docs contribution.
* Establishes, coordinates, and maintains documentation review processes including the participation of other SIGs in technical review.
* Maintains the Open 3D Engine website's infrastructure, tooling, and analytics.
* Responsible for maintaining core content and UX for the site.
* Maintains the official samples, tutorials, and demos for Open 3D Engine.
* Assist in the submission of 3rd party Open 3D Engine components for indexing.
* Creates subprojects or sub-SIGs to handle specific parts of the Open 3D Engine documentation and community resources as necessary.
* Ensures the availability of resources to perform SIG work.

## In scope

* O3DE Website
* Site UX
* Site deployment and build pipelines
* Site versioning
* Analytics tools and data analysis
* Non-documentation content:
    * Blogs
    * Community engagement
    * Soliciting contributions and general contrib guidelines (cross-cut)
    * Content (ex: general announcements, upcoming events) on channels such as O3DE Forums and O3DE Discord
    * O3DE YouTube Channel videos
* Documentation content:
    * Core O3DE engine
    * Core O3DE tools (asset building/processing, project config, etc.)
    * O3DE Editor
    * Screenshot maintenance (cross-cut)
    * Official samples, tutorials, and demos
    * 3rd party shepherding
    * 3rdparty gem index guidelines
    * 3rdparty samples/tutorials/demos index guidelines
    * Generated references (API reference, manpages, etc.)
* Community contributions
* Guidelines for documentation submissions such as minimum viable content, screenshot requirements, etc.
* Guidelines for minimum viable API reference.
* Guidelines for manpages or other standalone tools documentation.
* Guidelines for video content submissions
* Maintenance of a style guide
* Review of documentation pull requests.
    * Maintain and manage the usual SIG group of contributors and approvers for PR review, in addition to a group of approved technical reviewers from other teams.
    * Pull request review automation and approval workflows (cross-cut)
    * Standards and guidelines for review process
    * Editorial support
* Maintain a public roadmap for SIG work.
* Manages releases of documentation for bundled versions of O3DE.
* Track and report on milestones.
* Participate in binary releases by updating relevant materials on the site (i.e. download links, version number updates, etc.)
* Processes and improvements
* Work with other SIGs regarding contribution processes to help with messaging and standardized criteria.
* Work with 3rd parties to ensure O3DE users can find their resources
* Continually evaluate SIG processes against work and feedback to provide concrete improvements.
* Provide templates and general guidance for Request For Feature (RFF) documents
* Localization support

## Cross-cutting Processes

Aside from site maintenance and direct community interactions, the Documentation and Community SIG is primarily responsible for being involved in other SIGs when they need a voice representing community interests. The SIG also provides editorial review and support for other SIGs when requested.

The SIG will also perform the occasional ad-hoc advisement or other work regarding community relations for the O3DE Foundation. The SIG may work with critical third parties on an as-needed basis provided availability.

### Documentation and Community output to other SIGs

* Minimum viable product standards for documentation, including API reference. Other SIGs are allowed to provide stricter standards, but should consult with Documentation and Community before doing so.
* UX advisement for new features, including in-editor text

### Documentation and Community input from other SIGs

* Community materials such as dev diaries, blog posts, and other technical-focused materials better written by engineers.
* Technical review on documentation pull requests
* Standards for content: style guide, contributor guide, PR reviews. We are sometimes informally invited to consult on branding and design decisions, but we have no formal responsibility for such work.
* Coordinating docs contributions for point releases
* O3DE blog: The O3DE blog is a subproject of SIG Docs. SIG Docs provides tooling and workflow support for publishing the blog, but does not directly review blog posts or work with blog contributors. The blog subproject provides its own approvers and reviewers, and sets independent standards for creation and review of blog content.
* Other project documentation: SIG Docs is sometimes advises on O3DE components outside of the Open 3D Foundation GitHub repository, or on other O3DE subprojects, but is not responsible for the documentation of any of these components or projects.

## Out of Scope

* Creating new feature documentation.
* Docs will advise on feature documentation, but committers are expected to produce appropriate minimum viable documentation for their feature at the time of code submission.
* End-user support.
* Docs and Community are not technical support teams, but will contribute to Foundation-wide efforts and policies regarding support.
* Branding, marketing, logos, or other website content which is not explicitly claimed by the SIG.
* Localization. Docs and Community are not localization teams, but will provide infrastructure to support localization and may create subprojects to target specific high-priority languages for i18n.
* RFF production, review, and technical requirements. The docs team helps create templates and guidance based on feedback from governance, and may provide writing or editorial assistance for high-priority internal RFFs.
* Release notes and changelog. These are materials that should be produced for each release by the Release SIG, although docs will post/host on the O3DE website.

## SIG Links and lists

* Joining
* Slack/Discord
* YouTube Channel
* Forums
* Mailing list
* Issues/PRs
* Meeting agenda & Notes

## Roles and Organization Management

The Documentation and Community SIG adheres to the standards for roles and organization management as specified by . This SIG opts in to updates and modifications to .

## Individual Contributors

If you are targeting a particular release, make sure the pull request and issue is marked with the corresponding release milestone. This must be the same release identifier for both docs and code commits.

## Maintainers

Each release cycle, the current SIG Chair(s) must update membership. Maintainers of the  GitHub team are defined as follows:

* SIG chair(s)
* Documentation lead / sub-chair
* Community lead / sub-chair

To request membership to  or update the team:

1. File a PR to o3de/org making changes to the o3de-docs-community-sig team config here. In your PR, include the reason you're requesting access in the description, as well as a comment next to your username in the team config e.g.,   * o3deusera # Gem / PM / Docs   * somefellowb # 1.14 Core / Testing
2. Assign an approver from the group you'll be joining. If you are an incoming chair, request from the current lead(s).
3. Once your request is approved by the appropriate group, you can now assign to the PR to a SIG Release Chair for final approval.

## Additional responsibilities of Chairs

Chairs also serve as Tech Leads. Chairs are responsible for coordinating efforts between the sub-SIGs as necessary.

## Subproject Creation

SIG Chairs can create subprojects without requiring member votes. Subprojects may be found in the subproject directory.

## Deviations from sig-governance

Per readme:

* Meetings are biweekly
* Once per month, weekly meeting time changes for easier attendance from APAC contributors
* Once per quarter, leads and other interested parties meet to discuss quarterly goals and achievements

