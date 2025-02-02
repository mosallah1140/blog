---
author: mdo
date: "2018-04-09T00:00:00Z"
title: Bootstrap 4.1
video: 3wxyN3z9PL4
---

Two months ago we shipped the [first major release of Bootstrap 4]({{< relref "/posts/2018/bootstrap-4" >}}) and we're thrilled y'all love the latest release and [our brand new themes]({{< relref "/posts/2018/new-bootstrap-themes" >}}) so much. Today we're shipping our first minor release, v4.1! This release comes later than expected and some of the fixes we intended, but there's still a boatload of fixes, docs updates, build tool changes, and even a few small new features.

## Updated docs URL

With the release of v4 stable, we moved to a versioned docs setup, meaning each minor release would bring with it a new hosted version of our docs. This allows folks who haven't yet upgraded stick to the docs they know and love and avoids breaking URLs across the web. With today's release, our we'll have a new URL for this release's documentation, `getbootstrap.com/docs/4.1/`. The previous URL, `getbootstrap.com/docs/4.0/` will still work as y'all would imagine.

## Highlights

Here's what's new in addition to our bug fixes and docs updates:

- Added new custom range form control.
- Added new `.carousel-fade` modifier to switch carousel from horizontal sliding to crossfade.
- Added new `.dropdown-item-text` for plaintext dropdown items.
- Added new `.flex-fill`, `.flex-grow-*`, and `.flex-shrink-*` utilities.
- Added new `.table-borderless` variant for tables.
- Added new `.text-monospace` utility.
- Added new `.text-body` (default body color), `.text-black-50` (50% opacity black), and `.text-white-50` (50% opacity white) utilities.
- Added new `.shadow-*` utilities for quickly adding `box-shadow`s.
- Added ability to disable Popper's positioning in dropdowns.
- Updated our Theming docs to confirm you _cannot_ use CSS variables in media queries (sorry folks!).
- Fixed longstanding issue with Chrome rendering CSS columns incorrectly for cards.
- Deprecated `.text-hide`—you'll see a warning during compilation—as it's a dated and undocumented feature.
- Fixed up Dashboard and Offcanvas examples across Firefox and IE.
- Breadcrumbs can now use non-string values as dividers.

Be sure to look at the [ship list](https://github.com/twbs/bootstrap/issues/25375) and [project board](https://github.com/twbs/bootstrap/projects/5) for more details on all our fixes. Also, as a small heads up, we've split our issue template on GitHub into two separate templates, one for feature requests and one for bug reports. Please let us know if you have any feedback on the change.

## Next release

Next up, we're looking at a [v4.1.1 release](https://github.com/twbs/bootstrap/projects/13). There are some bug fixes for input groups, form fields, and more that I know we need to tackle sooner than later. These were supposed to be in v4.1, but we couldn't make it happen in time.
