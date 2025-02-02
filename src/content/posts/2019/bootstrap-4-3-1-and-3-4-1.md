---
author: mdo
date: "2019-02-13T00:00:00Z"
title: Bootstrap 3.4.1 and 4.3.1
---

Today we're shipping [Bootstrap v4.3.1](https://github.com/twbs/bootstrap/releases/tag/v4.3.1) and [v3.4.1](https://github.com/twbs/bootstrap/releases/tag/v3.4.1) to patch an XSS vulnerability, CVE-2019-8331. Also included in v4.3.1 is a small fix to some RFS (responsive font sizes) mixins that were added in v4.3.0.

Earlier this week a developer reported an XSS issue similar to the `data-target` vulnerability that was fixed in v4.1.2 and v3.4.0: the `data-template` attribute for our tooltip and popover plugins lacked proper XSS sanitization of the HTML that can be passed into the attribute's value.

To resolve the issue, we've implemented a new JavaScript sanitizer to only allow whitelisted HTML elements in data attribute. You may modify our sanitization implementation to customize the HTML element whitelist, totally disable the sanitization, or pass your own sanitize function (useful if you use your own library). However, for added protection, there is no way to modify the sanitization via data attributes—you must modify these plugin options via the JavaScript API.

Those who have modified the default templates, please [read the new v4.3 sanitizer docs]({{< param "main" >}}/docs/4.3/getting-started/javascript/#sanitizer) or the [new v3.4 sanitizer docs]({{< param "main" >}}/docs/3.4/javascript/#js-sanitizer).

In light of this vulnerability, we're also auditing our security reporting workflows to ensure they're up to date. This will include steps like adding a `SECURITY.md` file to our repository and ensuring our private channels and processes are up to date and documented with the team.

Thank you to [poiu](https://www.drupal.org/u/poiu) for reporting the vulnerability to the [Bootstrap Drupal project](https://www.drupal.org/project/bootstrap) and [Mark Carver](https://www.drupal.org/u/markcarver) from the [Bootstrap Drupal project](https://www.drupal.org/project/bootstrap) for responsibly disclosing the issue to us. Also a massive thank you to [@Johann-S](https://github.com/johann-s), [@Xhmikosr](https://github.com/xhmikosr), and [@bardiharborow](https://github.com/bardiharborow) on our team for the fast turnaround on today's releases.
