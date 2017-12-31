+++
title = "SSL Certificates"
+++

We want to ensure that our user's data is encrypted during transit and that the data they may provide is sent securely. The HTTPS-Only Standard provides a great, and much more detailed, description of the reasoning behind this.

This has become much easier with Let's Encrypt, which provides a free to use, automatic and secure certificate authority. It's integrated with Heroku, which allows us to use their Automated Certificate Management feature.

When we need wildcard certificates (e.g.: when we want to use the same certificate across www., staging., etc.), or those with advanced features, we use DNSimple.

