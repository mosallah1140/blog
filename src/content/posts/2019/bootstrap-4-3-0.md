---
author: mdo
date: "2019-02-11T00:00:00Z"
title: Bootstrap 4.3.0
video: htgr3pvBr-I
---

Bootstrap v4.3 has landed with over 120 combined closed issues and merged pull requests. This release brings improvements to our utilities, some prep work for moving on to v5's development, and the standard bug fixes and documentation updates.

During our last release, we shared a small preview of where we're taking the project next. That's getting clearer in the coming weeks as our attention turns towards embracing Hugo for ultra fast docs development, removing jQuery in favor of regular JavaScript, and addressing our growing code base.

Keep reading for v4.3 highlights, and see you soon with more details on v5!

## Highlights

We've added some new utilities and deprecated some unused code. Here are the key changes in v4.3, broken down by new, improved, fixed, and deprecated.

- **New:** Added `.stretched-link` utility to make any anchor the size of it's nearest `position: relative` parent, perfect for entirely clickable cards!
- **New:** Added `.text-break` utility for applying `word-break: break-word`
- **New:** Added `.rounded-sm` and `.rounded-lg` for small and large `border-radius`.
- **New:** Added `.modal-dialog-scrollable` modifier class for scrolling content _within_ a modal.
- **New:** Added responsive `.list-group-horizontal` modifier classes for displaying list groups as a horizontal row.
- **Improved:** Reduced our compiled CSS by using `null` for variables that by default inherit their values from other elements (e.g., `$headings-color` was `inherit` and is now `null` until you modifier it in your custom CSS).
- **Improved:** Badge focus styles now match their `background-color` like our buttons.
- **Fixed:** Silenced bad selectors in our JS plugins for the `href` HTML attribute to avoid JavaScript errors. Please try to use [valid selectors](https://www.w3.org/TR/CSS21/syndata.html#value-def-identifier) or the `data-target` HTML attribute/`target` option where available.
- **Fixed:** Reverted v4.2.1's change to the breakpoint and grid container Sass maps that blocked folks from upgrading when modifying those default variables.
- **Fixed:** Restored `white-space: nowrap` to `.dropdown-toggle` (before v4.2.1 it was on all `.btn`s) so carets don't wrap to new lines.
- **Deprecated:** `img-retina`, `invisible`, `float`, and `size` mixins are now deprecated and will be removed in v5.

Checkout the full [v4.3.0 ship list](https://github.com/twbs/bootstrap/issues/27893) and [GitHub project](https://github.com/twbs/bootstrap/projects/16) for the full details.

[Head to to the v4.3.x docs]({{< param "main" >}}/docs/4.3/) to see the latest in action. The full release has been published to npm and will soon appear on the Bootstrap CDN and Rubygems.

## Introducing responsive font sizes

![Responsive font-sizes](/assets/img/2019/02/rfs.png)

Our biggest new addition to Bootstrap in v4.3 is responsive font sizes, a [new project in the Bootstrap GitHub org](https://github.com/twbs/rfs) to automate calculate an appropriate `font-size` based on the dimensions of a visitor's device or browser viewport. Here's how it works:

- All `font-size` properties have been switched to the `@include font-size()` mixin. Our Stylelint configuration now prevents the usage of `font-size` property.

- Disabled by default, you can opt into this new behavior by toggling the `$enable-responsive-font-sizes` boolean variable.

- `font-size`s are entirely configurable via Sass. Be sure to read the docs for how to modify the scales, variables, and more.

While responsive font-sizes are disabled by default, we've enabled them in the custom CSS that powers our docs starting with v4.3. Please share feedback with us via GitHub issues or on Twitter. We've added some light guidance to [our Typography docs]({{< param "main" >}}/docs/4.3/content/typography/#responsive-font-sizes) to explain the feature. You can also learn more by [reading the rfs project documentation](https://github.com/twbs/rfs).

## Open Collective

Last December we launched our [Open Collective page]({{< param "opencollective" >}}) with our [v3.4 release]({{< relref "/posts/2018/bootstrap-3-4-0" >}}) to help support the maintainers contributing to Bootstrap. The team has been very excited about this as a way to be transparent about maintainer costs (both time and money), as well as recognition of efforts.

## Branches, Hugo, and jQuery

Right after shipping v4.3, we'll be tackling a few key changes on our road to active v5 development. These are larger changes to how we maintain and develop Bootstrap and are considered foundational for v5.

- **Improving our branches for development.** `master` will become our new `v3-dev` branch. `v4-dev` will stay as-is, but we'll cut a new `master` branch from there to develop v5.

- **We're moving to Hugo!** Jekyll has been great, but it's starting to slow us down in local development. We'll be making changes to our dependencies to support this move, and there's already a pull request in progress and near completion for the change. [Follow along](https://github.com/twbs/bootstrap/pull/28014) to see what's changing.

- **We're dropping jQuery for regular JavaScript.** The cat is out of the bag—we're dropping our largest client-side dependency for regular JavaScript. Similar to the Hugo move, we've been working on this for a long time and have a [pull request in progress](https://github.com/twbs/bootstrap/pull/23586) and near completion.

We'll have even more to share soon around v5's plans after we tackle these bigger items. In the meantime, keep the feedback coming on GitHub and Twitter!
