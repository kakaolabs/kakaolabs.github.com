+++
title = "Production Checklist"
+++

We have found that a short checklist is valuable when setting up a new production environment or preparing for a launch:

+ Are we on the latest Heroku stack?
+ Are we using a concurrent web server? See how to deploy with Puma.
+ Are long-running processes such as email delivery being run in background jobs? See how to set up Delayed Job.
+ Are there redundant (at least two) web and background processes running?
+ Are we using SSL? See "SSL Certificates" section below.
+ Are API requests being made via a separate subdomain (api.example.com)? Even if the same app, this gives us architectural flexibility in the future.
+ Is the latest Ruby defined in the Gemfile? See how to set it up.
+ Is config stored in environment variables?
+ Are deploys done manually at a scheduled time when teammates are fresh and available if something goes wrong?
+ Do deploys follow a well-documented script?
+ Are we sending logs to a remote logging service? See "Log Collection" section below.
+ Are we using a Heroku "Standard" database or higher? See Heroku production databases.
+ Are we backing up our production database? See Heroku PGBackups.
+ Are we monitoring performance and uptime? See "Performance Monitoring" section below.
+ Are we tracking errors? See "Error Tracking" section below.
