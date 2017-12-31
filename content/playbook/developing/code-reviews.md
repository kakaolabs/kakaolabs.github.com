+++
title = "Code Reviews"
+++

Here's the flow. Read our git protocol for the git commands.

+ Create a local feature branch based off master.
+ When feature is complete and tests pass, stage the changes.
+ When you've staged the changes, commit them.
+ Write a good commit message.
+ Share your branch.
+ Submit a GitHub pull request.
+ Ask for a code review in Slack.
+ A team member other than the author reviews the pull request. They follow Code Review guidelines to avoid miscommunication.
+ They make comments and ask questions directly on lines of code in the GitHub web interface or in Slack.
+ When satisfied, they approve or comment on the pull request that it's ready to merge.
+ Rebase interactively. Squash commits like "Fix whitespace" into one or a small number of valuable commit(s). Edit commit messages to reveal intent.
+ View a list of new commits. View changed files. Merge branch into master.
+ Delete your remote feature branch.
+ Delete your local feature branch.

Test-Driven Development moves code failure earlier in the development process. It's better to have a failing test on your development machine than in production. It also allows you to have tighter feedback cycles.

Code reviews that happen right before code goes into master offer similar benefits:

+ The whole team learns about new code as it is written.
+ Mistakes are caught earlier.
+ Coding standards are more likely to be established, discussed, and followed.
+ Feedback from this style of code review is far more likely to be applied.
+ No one forgets context ("Why did we write this?") since it's fresh in the author's mind.