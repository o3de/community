  

# Overview

This guide covers the standard process SIGs should use to triage GitHub issues into their backlogs. Although the purpose of this guide is to level-set a standard process to be used across all SIGs, it is expected that SIGs will build off this guide to best suit their needs - i.e. use this guide as a starting point for your triage process - not as the end-all be-all for issue triage. Please note the triage of pull requests is outside the scope of this guide.

Purpose
=======

SIG Triage is the process of reviewing issues that are newly assigned to your SIG, either declining or accepting them into your SIG's backlog, and ensuring each accepted issue contains sufficient information for the community to take action on.

Meeting Cadence
===============

We recommend SIGs perform their triage at least once per week, at minimum. This is to ensure issues are reviewed in a timely manner.

SIG Triage should occur with the community present via a meeting in the SIG's [Discord](https://discord.gg/u7rSfSpvz2) voice channel. To schedule a meeting with your SIG, list the meeting on the [O3DE Calendar](https://lists.o3de.org/g/o3de-calendar/calendar?calstart=2021-07-22). It is also recommended to post a reminder about the upcoming triage in the SIG's Discord text channel the day before triage takes place (e.g. "Hi all! We will be performing an issue triage today at \[time\]am PDT, \[time\]pm UTC until \[time\]am PDT, \[time\]pm UTC. Feel free to join and observe in the\[sig-name\] voice channel.")

Labels
======

Github uses labels to categorize issues. Only a subset of the labels in the O3DE repo are used during triage, as indicated in the "Process" section below. A full list of labels, and their definitions, can be found [here](https://github.com/o3de/o3de/labels).

Process
=======

Filter the O3DE Backlog for issues that need a sig, by looking for the ["**needs-sig**"](https://github.com/o3de/o3de/issues?q=is%3Aissue+is%3Aopen+label%3Aneeds-sig) label. Ensure any relevant items are assigned to your SIG.
   * Encourage maintainers to regularly review the backlog of items so someone is always re-directing relevant issues to your SIG.

Filter the O3DE Backlog for open issues with the "**needs-triage**" label and your "**sig/**" label (e.g. [open issues with the "needs-triage" and "sig/release" labels](https://github.com/o3de/o3de/issues?q=is%3Aopen+label%3Asig%2Frelease+label%3Aneeds-triage+)). 

For each issue:

1.  Ensure the issue is appropriate for your SIG. If it is NOT appropriate for your SIG:
    1.  Remove your "**sig/**" label, and add a comment to the issue indicating why it is not appropriate for your SIG.
    2.  If the appropriate SIG is known, assign it to that SIG by applying the appropriate "**sig/**" label (e.g. sig/release, sig/core, sig/presentation, etc.). Otherwise, apply the "**needs-sig**" label (this will send the issue back for assignment).
    3.  Do NOT remove the "**needs-triage**" label.
2.  Review the issue details and comments to determine if the issue should be declined or accepted into your SIG's backlog, or if more information is required prior to making this determination.  
    1.  To accept an issue into your backlog  
        1.  Add the "**triage/accepted**" label to indicate the issue has been triaged and accepted into your backlog.
        3.  Add a "**feature/**" label (e.g. feature/atom, feature/editor, feature/physics, etc.) to indicate the feature impacted.
        4.  Add a "**priority/**" label (e.g. priority/minor, priority/major, etc.) to indicate the relative priority of the item with respect to other items in the backlog.
        5.  (Optional) If the issue is a feature request, add a "**feature-need/**" label (e.g. feature-need/immediate, feature-need/important-soon, feature-need/important-longterm, etc.) to indicate the relative timeframe the SIG would like the feature to be delivered.
        6.  If the issue is low complexity and a good issue for first time contributors, add the "**good-first-issue**" label.
        7.  If your SIG would like help on this issue from a contributor, add the "**help-wanted**" label.
        8.  If you are the only SIG impacted by the issue (i.e. if the only "sig/" label on the issue is for your SIG), or if you are the last SIG to triage the issue:
            1.  Remove the "**needs-triage**" label.   
        9.  Otherwise, if another SIG is impacted by the issue and hasn't completed triage:
            1.  Do NOT remove the "**needs-triage**" label.
            2.  Add a comment for the other SIGs indicating you have completed your triage, and they can remove the 'needs-triage' label once they have completed their triage.
    2.  To decline an issue:  
        1.  If the issue is for a "substantial" change that is not yet vetted through the RFC process (see [RFC Process](https://github.com/o3de/rfcs/blob/main/README.md) for additional information), decline it as follows:  
            1.  Add the "**status/invalid**" label.
            2.  Add a comment similar to the following: "This issue is for a substantial change that should be vetted through the RFC process. Please open an RFC, link it to this issue, and then close this issue."
            3.  Assign the issue to the person who opened it.
        2.  If the issue is a request for help, rather than an actual issue, decline it as follows:  
            1.  Add the "**status/invalid**" label.
            2.  Add a comment similar to the following: "This is a request for help. Please convert this issue to a 'Q&A' Discussion instead."
            3.  Assign the issue to the person who opened it.
            4.  Note: The issue will automatically close when it is converted to a Discussion.
        3.  If the issue is an idea that requires additional opinion / further refinement before it can be considered, decline it as follows:  
            1.  Add the "**status/invalid**" label.
            2.  Add a comment similar to the following: "This is an idea that needs requires additional opinion / further refinement before it can be considered. Please convert this issue to an 'Ideas' Discussion instead."
            3.  Assign the issue to the person who opened it.
            4.  Note: The issue will automatically close when it is converted to a Discussion.
        4.  If the issue is a duplicate, decline it as follows:  
            1.  Add the "**status/duplicate**" label.
            2.  Add a comment which references the duplicate issue.   
            3.  Close the issue.   
        5.  If the issue is something your SIG does not want to pursue, decline it as follows:
            1.  Add the "**triage/declined**" label.
            2.  Add the "**status/wont-do**" label.
            3.  Add a comment that politely indicates why the request will not be pursued by your SIG.
            4.  If you are the only SIG impacted by the issue (i.e. if the only "sig/" label on the issue is for your SIG), or if you are the last SIG to triage the issue:  
                1.  Remove the "**needs-triage**" label.
                2.  Close the issue.  
                    
            5.  Otherwise, if another SIG is impacted by the issue and hasn't completed triage:
                1.  Do NOT remove the "**needs-triage**" label.
                2.  Do NOT close the issue.
                3.  Add a comment for the other SIGs indicating you have completed your triage, and they can remove the 'needs-triage' label and close the issue once they have completed their triage.
    3.  To request additional information  
        1.  Do NOT remove the "**needs-triage**" label.
        2.  Add the "**triage/needs-information**" label.
        3.  Add a comment similar to the following: "The nature of this issue is not clear. Please add clarification."
        4.  Assign the issue to the person who opened it.