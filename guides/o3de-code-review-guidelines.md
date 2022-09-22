# O3DE code review guidelines

This document contains a set of guidelines for code reviewers and change authors when contributing to Open 3D Engine (O3DE). The intention is to help pull requests (PRs) go smoothly and help the community share best practices and lessons learned when it comes to changes and reviews.

> Note: The guidance here applies primarily to PRs targeting the `development` branch.

## Useful related material

- [O3DE C++ Coding Standards](https://github.com/o3de/sig-core/blob/main/governance/Coding-Standards-and-Style-Guide.md#o3de-c-coding-standards-)
- [O3DE API Ref Guidelines](https://github.com/o3de/sig-core/blob/main/governance/API-Ref-Guidelines-Update.md)

## Change author guidelines

A set of guidelines for those making changes and creating PRs (the PR author).

> Note: There may be situations where the responsibility of shepherding a PR through review falls to someone who is not the originator of the change. For the purposes of this document all such roles fall under 'Change Author' as the individual is still responsible for the work being reviewed.

### Keep it short

This of course isn't always possible, there will be exceptions, but to get a PR approved and merged in a reasonable time-frame, try to keep changes as self contained and focused as possible. Small incremental progress is much safer and simpler than a single large change that contains many modified lines and files.

### Review your own PR

The best way to catch simple mistakes and small oversights is to read through your own PR in the GitHub UI before hitting the publish button. Viewing your own code through this slightly different lens often uncovers a lot more issues than you'd expect and can help save other reviewers time.

### Ensure PRs are ready for review

Try not to publish something for review when still making changes. This can lead to reviewers needing to re-review changes or confusion in what has changed or not. Try to only make requested changes in a PR to avoid unnecessary churn.

**Note**: Draft PRs - _This does not apply to 'Draft' PRs which are great to use to share early ideas/designs. The reviewer knows they aren't yet 'reviewing' the code, they're just giving initial feedback. Keeping a PR in a draft state also ensures it cannot accidentally be merged._

### Respond to comments

It's good practice to acknowledge you've read the reviewer's feedback. This can be as simple as leaving a 👍 or a brief comment and then resolving the conversation. If the comment was simple and has been fixed, it's usually fine to resolve the conversation. Try to avoid resolving conversations without acknowledging or responding to them either with a reply or emoji.

### Don't sweat the small stuff

Reviewers will sometimes leave optional/suggested feedback. Not everything has to be accepted, especially with certain stylistic choices (the Coding Standards should be the ultimate arbiter here to help resolve any conflicts). It's often appropriate to move some feedback to a follow-up PR that makes the relevant updates, or they can be rolled into a future change.

### Avoid mixing functional and formatting changes

When making updates to the code, try to avoid making numerous formatting only changes while also including functional updates. The best approach is to make the functional change with the most minimal, necessary changes, and create a separate PR that exclusively includes the formatting changes.

### A picture is worth a thousand words

If your change results in any kind of visual difference, to help reviewers quickly get context on the PR, please attach screenshots and/or videos/gifs of the change in action (including before/after is also very useful). This helps frame the change and can make reviewers' lives much easier to see what the effect of the change is. This goes for test output and things like Script Canvas graphs too.

### Engage UI/UX when needed

If your PR involves user interface (UI) or user experience (UX) changes, please ensure you have read how to get help from [SIG/UI-UX](https://github.com/o3de/sig-ui-ux/blob/main/governance/UX%20Intake%20Process.md). SIG maintainers can help you connect and engage with the UI/UX team.

### Engage Docs when needed

If your PR requires changes to the O3DE documentation or tutorials, ensure you've reviewed [Issue 34](https://github.com/o3de/sig-docs-community/issues/43) (currently in review). SIG maintainers can help you connect and engage with the documentation experts.

### Nudges are okay

If your PR has been waiting a while and no one has looked at it, it's okay to start using gentle nudges to ask for feedback. This most likely will be on Discord but it's possible to also tag people in the PR comments (using the [@mention feature](https://github.blog/2011-03-23-mention-somebody-they-re-notified/)) and politely ask them to take a look. Code owners will be automatically notified but sometimes things can be missed.

> It's inevitable people get busy or will be away too, it happens. When faced with this, try and switch to something else or look for another code owner with domain knowledge who can approve the PR (it's possible to find such people in the relevant SIG channels on Discord).

## Code reviewer guidelines

A set of guidelines for those reviewing changes and commenting on/approving PRs (the PR reviewer)

### Be kind

> (Stolen from Google's excellent [engineering practices](https://google.github.io/eng-practices/review/reviewer/comments.html))

Writing code is hard and doing so in a new environment with unfamiliar faces can be even more daunting. As reviewers we want to encourage and support new contributors. We want to thank people for their efforts and offer constructive feedback where necessary. Remember to call out the highlights of a change as well as things that need improvement.

### It's about the code

When writing review feedback focus on what the code is doing, not what the change author did. Avoid 'you' if at all possible. Instead use 'we' to demonstrate our shared responsibility and ownership of the code base or refer to the code directly.

e.g.

Avoid: _"You should use a vector here has it will lead to better cache locality"_  
Prefer: _"A vector might be a good idea to use here to get better cache locality"_

### Include the _why_

When suggesting a change (unless it's something trivial) it's helpful to include the reason _why_ such a change is being proposed. This gives context to the request and can often act as a learning opportunity for the code author and other contributors who may be reviewing or observing the PR.

### Don't be late to the party

If a PR already has two or more approvals (from at least one code owner) be conscious that additional feedback can interrupt the flow of a PR. Feel free to still review, and if a serious issue is spotted do feel empowered to take the necessary steps (request changes), but try to avoid requiring minor changes to be made that could be addressed in a follow-up PR.

> Note: It is fine to leave additional comments, but the reviewer should be comfortable with them being moved to either a specific follow-up PR or grouped into a subsequent change.

### Keep feedback focused

Ensure feedback is targeted at the changed lines of code and not surrounding code. It isn't the change authors responsibility to fix a problem a reviewer sees that happens to be in that area of code. If something is spotted, make an issue, and follow-up with a separate PR.

### Be judicious with 'Request Changes'

Request changes is a powerful tool and shouldn't be used lightly. If an apparent bug, performance problem or architecture issue is spotted, then 'Request Changes' may be used. However, often simply not approving the PR and leaving a comment is sufficient to resolve whatever problem is detected, and does so in a softer and friendlier way. Prefer this option if you can.

### Be responsive

After reviewing a PR, keep an eye on when the change author has responded and do your best to reply to their responses promptly (ideally within a 24 hour window, though this isn't always possible). If you are delayed and don't have time to respond fully, leave a comment on the PR that you're busy and will get back to it as soon as you can.

### Approve if you can

> Note: This sentiment is also lifted from the excellent Google [engineering practices](https://google.github.io/eng-practices/review/reviewer/standard.html) page

_In general, reviewers should favor approving a [PR] once it is in a state where it definitely improves the overall code health of the system being worked on, even if the [PR] isn’t perfect._

It's inevitable all changes will not get everything right, but if what is there improves the software while keeping it maintainable and efficient, a reviewer should feel empowered to approve (don't let [perfect be the enemy of good](https://en.wikipedia.org/wiki/Perfect_is_the_enemy_of_good)).

### If you can't approve, take things offline

If there is a point of discussion on a PR that cannot be quickly resolved, consider reaching out directly to the change author to talk it over (either over Discord via a direct message or in the relevant SIG channel, a separate GitHub discussion or even an RFC - sometimes a voice call is even better if possible). In our experience this leads to better outcomes for both parties and avoids potential misunderstandings. Leaving a brief update on the PR with the resolution afterwards is good practice too.

> Note: If a discussion cannot be resolved between contributors it is possible to escalate to SIG chairs either through Discord or the public meetings (also held on Discord). The dates for these can be found [here](https://lists.o3de.org/g/o3de-calendar/calendar).

## Contributors, reviewers and maintainers

Once a PR is approved by two or more reviewers, an AR run can commence. Currently only [maintainers](https://github.com/orgs/o3de/teams/maintainers) can initiate builds so please feel free to ask for someone with access to start a build. The list of PRs can be found here - [Change Requests](https://jenkins.build.o3de.org/job/O3DE/view/change-requests/). Search for the PR number to review the current status of the build. Once AR has completed and there are no failures, a PR can be merged by a maintainer.
