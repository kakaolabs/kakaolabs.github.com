+++
title = "Continuous Integration"
+++

Martin Fowler has an extensive description of Continuous Integration. The basics are:

+ We have a test suite that each developer runs on their own machine.
+ When they commit their code to a shared version control repository, the tests are run again, "integrated" with code from other developers.

This helps ensure there's nothing specific to the developer's machine making the tests pass. The code in version control needs to run cleanly in production later so before the code is allowed to be deployed to production, it is run on a CI server or service.

When a build fails, we get alerts in Slack and via email. Click the alert and we see a backtrace that gives us a hint of how to "fix the build."

When we write the fix and commit to version control again, we'll get a "passing build" alert in Slack and via email. Click the alert and we see the passing build.

Green is good.

A solid test suite is an absolute requirement for a web application. However, one major problem with test suites is that they get slow as they get large.

CI can ease the pain by distributing the test runs in parallel. We've had 45 minute test suites cut down to 2 minutes using this technique.

We've used CruiseControl, Integrity, Jenkins, and other CI libraries that we manage ourselves. This resulted in many hours of expensive attention.

Now, we use a combination of CircleCI and Travis CI because of their great UIs, simple configuration and close integration with GitHub.

CI test runs are triggered when we push to Github and can be seen as part of the status checks of pull requests. We also use Hound to help us follow our style guide and keep review comments focused on improving the code quality.