+++
title = "Performance Monitoring"
+++

We use NewRelic to monitor performance of production applications.

Debugging performance might be the best part of a developer's job. There's a clear, numeric problem. When we fix it, that number improves. We can say things like "We made this 175% better."

There's many established techniques for fixing performance problems. A number of them come "for free" with Rails + Heroku:

+ Amazon server clusters
+ gzipping
+ Asset pipeline
+ SQL query caching

A number of them require developer thought:

+ Database indexing
+ Eager loading
+ HTTP caching

Page caching is the heaviest handed technique we have, but if we can cache an entire page and push it into a CDN, that will be the fastest option.