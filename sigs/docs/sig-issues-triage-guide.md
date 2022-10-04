# Overview

This guide covers the standard process SIGs should use to triage GitHub issues into their backlogs. Although the purpose of this guide is to set a standard process to be used across all SIGs, it is expected that SIGs will build off this guide where their triage process deviates. For example [SIG/network](https://github.com/o3de/sig-network) needs to look at issues in other repositories, so their [triage guide](https://github.com/o3de/sig-network/blob/main/TRIAGE_GUIDE.md) requires additional steps.

> Please note the triage of pull requests is outside the scope of this guide.

## Purpose

SIG issue triage is the process of reviewing issues that are newly assigned to your SIG, either declining or accepting them into your SIG's backlog, and ensuring each accepted issue contains sufficient information for the community to take action on.

# Meeting cadence

We recommend SIGs perform their triage at least once per week, at minimum. This is to ensure issues are reviewed in a timely manner.

SIG Triage should occur with the community present via a meeting in the SIG's [Discord](https://discord.gg/o3de) voice channel. To schedule a meeting with your SIG, list the meeting on the [O3DE Calendar](https://lists.o3de.org/g/o3de-calendar/calendar). It is also recommended to post a reminder about the upcoming triage in the SIG's Discord text channel the day before triage takes place.

For example:
```
"Hi all! We will be performing an issue triage today at [time]am PDT, [time]pm UTC until [time]am PDT, [time]pm UTC. Feel free to join and observe in the [sig-name] voice channel."
```

# GitHub labels
GitHub uses labels to categorize issues. Only a subset of the labels in the O3DE repo are used during triage, as indicated in the "Process" section below. A full list of labels, and their definitions, can be found [here](https://github.com/o3de/o3de/labels).

# Process

Filter the O3DE Backlog for issues that need a sig, by looking for the ["**needs-sig**"](https://github.com/o3de/o3de/issues?q=is%3Aissue+is%3Aopen+label%3Aneeds-sig) label. Ensure any relevant items are assigned to your SIG.
   * Encourage maintainers to regularly review the backlog of items so someone is always re-directing relevant issues to your SIG.

Filter the O3DE Backlog for open issues with the "**needs-triage**" label and your "**sig/**" label (e.g. [open issues with the "needs-triage" and "sig/release" labels](https://github.com/o3de/o3de/issues?q=is%3Aopen+label%3Asig%2Frelease+label%3Aneeds-triage+)). 

For each issue:

1.  Ensure the issue is appropriate for your SIG. If it is NOT appropriate for your SIG:
    1.  Remove your "**sig/**" label, and add a comment to the issue indicating why it is not appropriate for your SIG.
    2.  If the appropriate SIG is known, assign it to that SIG by applying the appropriate "**sig/**" label (e.g. sig/release, sig/core, sig/presentation, etc.). Otherwise, apply the "**needs-sig**" label (this will send the issue back for SIG assignment).
    3.  Do NOT remove the "**needs-triage**" label.
    
2.  Review the issue details and comments to determine if the issue should be declined or accepted into your SIG's backlog, or if more information is required prior to making this determination.  
    1.  To accept an issue into your backlog  
        1. Add the "**triage/accepted**" label to indicate the issue has been triaged and accepted into your backlog.
        2. Add a "**feature/**" label (e.g. feature/atom, feature/editor, feature/physics, etc.) to indicate the feature impacted.
        3. Add a "**priority/**" label (e.g. priority/minor, priority/major, etc.) to indicate the relative priority of the item with respect to other items in the backlog.
        4. (Optional) If the issue is a feature request, add a "**feature-need/**" label (e.g. **feature-need/immediate**, **feature-need/important-soon**, **feature-need/important-longterm**, etc.) to indicate the relative timeframe the SIG would like the feature to be delivered.
        5. If the issue is low complexity and a good issue for first time contributors, add the "**good-first-issue**" label.
        6. If your SIG would like help on this issue from a contributor, add the "**help-wanted**" label.
        7. If you are the only SIG impacted by the issue (if the only "sig/" label on the issue is for your SIG), or if you are the last SIG to triage the issue:
            1.  Remove the "**needs-triage**" label.   
        8. Otherwise, if another SIG is impacted by the issue:
            1.  Work with the impacted SIGs to identify the owning SIG for the issue, this SIG should be the one to ultimately accept the item.
            2.  DO NOT remove the "**needs-triage**" label or add "**triage-accepted**", unless you have agreement from impacted SIGs or they have removed their "sig/" label from the issue.
            3.  If you *need information from other SIG(s)* before acceptance - add a comment about what information is being sought and why, ensure the right SIG labels are assigned and wait for the other SIG(s) to complete their triage process. 
                1. If impacted SIGs are ok for issue to be accepted, they should provide an acceptance comment and then are free to remove their SIG label from the issue (ensuring that at least one SIG is still assigned). 
                2. If impacted SIGs have questions or challenges, they should provide a comment identifying their concerns or what information is required. Impacted SIGs should work with the owning SIG to find a resolution.
                3. Owning SIG should work proactively to reach cross-SIG agreement or identify next steps.
                4. If SIGs cannot reach an agreement on accepting an issue, then the [TSC](https://github.com/o3de/tsc) should be involved.
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

## Issues requiring UX help
For issues that may need [SIG/ui-ux] help, please refer to their [guide about getting UX assistance](https://github.com/o3de/sig-ui-ux/blob/main/governance/UX%20Intake%20Process.md).

# Updating this guide
Please update this guide with anything that is relevant to all SIGs. Expectation is that SIG Chair(s) or triage leaders will maintain this guide to ensure it stays relevant to common issue triage practices.