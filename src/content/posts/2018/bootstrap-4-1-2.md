---
author: mdo
date: "2018-07-12T00:00:00Z"
title: Bootstrap 4.1.2
video: qHDy_b33cCQ
---

We've been busy these last couple months since launching v4.1.1, but we're back with another bug fix and some sweeping changes to how we build and publish our docs after the issues stemming from our v4.1.x launches.

When we launched v4.1, we ran into unexpected issues with having to rearrange asset paths after deploying, resulting in broken image URLs, a busted service worker, and more. Since then, we're ironed out most of the kinks and introduced a new docs directory structure inside the repo. Nothing should change for anyone using our docs, but those contributing to the project and developing locally may need to rebase their changes or update their branches accordingly.

Beyond the file structure changes, here are the highlights for v4.1.2:

- Fixed an XSS vulnerability in tooltip, collapse, and scrollspy plugins
- Improved how we query elements in our JavaScript plugins
- Inline SVGs now have the same vertical alignment as images
- Fixed issues with double transitions on carousels
- Added Edge and IE10-11 fallbacks to our floating labels example
- Various improvements to form controls, including disabled states on file inputs and unified focus styles for selects
- Miscellaneous build tool improvements and documentation fixes

Checkout the full [v4.1.2 ship list](https://github.com/twbs/bootstrap/issues/26423) and [GitHub project](https://github.com/twbs/bootstrap/projects/14) for the full details. Up next will either be [v4.1.3](https://github.com/twbs/bootstrap/projects/15) or [v4.2](https://github.com/twbs/bootstrap/projects/6) depending on how smoothly this release goes and how well we can keep up with reviewing and merging pull requests.

Head to the v4.1.x docs to see the latest in action. The full release has been published to npm and will soon appear on the Bootstrap CDN and Rubygems.
