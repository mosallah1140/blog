---
author: mdo
date: "2018-12-13T00:00:00Z"
title: Bootstrap 3.4.0
video: 8WEtxJ4-sh4
---

That's not a typo—today we're shipping Bootstrap 3.4.0, a long overdue update to address some quality of life issues, XSS fixes, and build tooling updates to make it easier for us, and you, to develop.

While we'd planned for ages to do a fresh v3.x update, we lost steam as energy was focused on all the work in v4. Early this year, [one issue in particular](https://github.com/twbs/bootstrap/issues/25679) gained a ton of momentum from the community and the core team decided to do a huge push to pull together a solid release. I regret the time it took to pull this release together, especially given the security fixes, but with the improvements under the hood, v3 has never been easier to develop and maintain. Thanks for your continued support along the way!

Keep reading for what's changed and a look ahead at what's coming in v4.2.0.

## What's new

While we haven't publicly worked on v3.x in years, we've heard from all of you during that time that we needed to do a new release to address

- **New:** Added a `.row-no-gutters` class.
- **New:** Added docs searching via Algolia.
- **Fixed:** Resolved an XSS issue in Alert, Carousel, Collapse, Dropdown, Modal, and Tab components. See <https://snyk.io/vuln/npm:bootstrap:20160627> for details.
- **Fixed:** Added padding to `.navbar-fixed-*` on modal open
- **Fixed:** Removed the double border on `<abbr>` elements.
- Removed Gist creation in web-based Customizer since anonymous gists were disabled long ago by GitHub.
- Removed drag and drop support from Customizer since it didn't work anymore.

Our documentation and tooling saw massive updates as well to make it easier to work on v3.x, for ourselves and for you.

- Added a dropdown to the docs nav for newer and previous versions.
- Update the docs to use a new `baseurl`, `/docs/3.4/`, to version the v3.x documentation like we do with v4.
- Reorganized the v3 docs CSS to use Less.
- Switched to BrowserStack for tests.
- Updated links to always use https and fix broken URLs.
- Replaced ZeroClipboard with clipboard.js

[Head to the Bootstrap 3.4 docs]({{< param "main" >}}/docs/3.4/) to see the latest in action. [Check out the v3.4.0 pull request](https://github.com/twbs/bootstrap/pull/27288) for even more context on what's changed.

## Upgrading

Upgrade your Bootstrap 3 projects to v3.4.0 with `npm i bootstrap@previous` or `npm i bootstrap@3.4.0`. This release won't be available via Bower to start given the package manager was deprecated and has largely been unused by us in v4 for well over a year. Stay tuned for CDN and Rubygem updates.

## Open Collective

Also new with our v3.4 is the creation of an [Open Collective page]({{< param "opencollective" >}}) to help support the maintainers contributing to Bootstrap. The team has been very excited about this as a way to be transparent about maintainer costs (both time and money), as well as recognition of efforts.

## v4.2 and beyond

We've been working on a [huge v4.2 update](https://github.com/twbs/bootstrap/projects/6?fullscreen=true) for several months now. Our attention has largely been on advancing the project and simplifying it's dependencies, namely by removing our jQuery dependency. That work has sparked a keen interest in a moderately scoped v5 release, so we've been taking our sweet time with v4.2 to sneak in as many new features as we can.

After we ship v4.2, we'll plan for point releases to address any bugs and improvements as y'all start to use the new version. From there, we'll start to share more plans on v5 to remove jQuery, drop support for older browsers, and clear up some cruft. This won't be a sweeping rewrite, but rather an iterative improvement on v4. Stay tuned!
