---
author: mdo
date: "2018-01-18T00:00:00Z"
title: Bootstrap 4
video: VcjzHMhBtf0
---

It's literally taken us years to do it, but Bootstrap 4 has finally arrived! Words cannot begin to describe the elation the entire team and I have for this release, but I'll do my best. Thank you to everyone, especially to the team, and to everyone who's contributed code in a pull request or opened an issue. **Thank you.**

Since our last beta, we've been hard at work stabilizing a few key pieces of our CSS, polishing our documentation, adding some extra surprises, and planning for our follow-up releases. We still have some kinks to iron out, but nothing's going to stop us from shipping a stable release.

**Anxious to jump right in? [Head over to our documentation site]({{< param "main" >}}/) and explore.** Be sure to check out our [new Examples]({{< param "main" >}}/docs/4.0/examples/) and the [migration docs page]({{< param "main" >}}/docs/4.0/migration/)!

Want to know more before hitting the docs? Great, let's dive in!

## What's new

There are no breaking changes since our last beta, but we have made some key improvements and resolved some tricky bugs.

- Print styles and utility classes have been updated. We've improved how printed pages are rendered to ensure pages are reasonably sized instead of rendering them as mobile devices. Print display utilities also include a whole slew of new `display` values to match our standard display utilities.

- Additive border utilities have been added (e.g., `.border-top`) and default to a solid 1px light gray border. Now it's easier to quickly add all borders or a subset of borders to your components.

- Our `$spacers` and `$sizes` Sass maps have been updated to allow more customization the same way our color maps work. You can now add, remove, or replace all your key-value pairs consistently across our CSS. [Head to our Theming docs]({{< param "main" >}}/docs/4.0/getting-started/theming/) for more information and examples.

- Added documentation to our Theming docs for using our provided [CSS variables]({{< param "main" >}}/docs/4.0/getting-started/theming/#css-variables) for those are living on the edge and don't want to use Sass.

- Added responsive `.order-0` and `.order-last` classes for more control over the flexbox grid.

In addition, we've made plenty of improvements to reusing and extending variables and general code cleanup. But, that's still not everything.

## New examples

Nearly every example has been overhauled for our stable v4 release. We've removed a couple outdated examples, added brand new ones, and really overhauled a few others.

[![Bootstrap examples](/assets/img/2018/01/examples.png)]({{< param "main" >}}/docs/4.0/examples/)

Here's the rundown of changes to each:

- You've likely already seen our [Album example]({{< param "main" >}}/docs/4.0/examples/album/), but it's been updated for this release to include more content in our photo cards and improved mobile rendering.

- [Pricing]({{< param "main" >}}/docs/4.0/examples/pricing/) is brand new with this release and is a fully custom page built with our utilities and card components. It's responsive and easily extended.

- [Checkout]({{< param "main" >}}/docs/4.0/examples/checkout/) is a brand new, extensive form example featuring all the best parts of our form layouts, validation styles, grid, and more.

- [Product]({{< param "main" >}}/docs/4.0/examples/product/) is also new and is a cheeky riff on Apple-style marketing pages, largely built with only our utility classes. Don't take it too seriously!

- [Blog]({{< param "main" >}}/docs/4.0/examples/blog/) has been rewritten from the ground up. Gone is the two column blue header layout. We've built a snarky magazine-style layout with featured posts and responsive navigation.

- [Dashboard]({{< param "main" >}}/docs/4.0/examples/dashboard/) has been overhauled as well to feature a live ChartJS example, includes a refreshed sidebar with [Feather icons](https://feathericons.com/), and is semi-responsive.

- [Floating labels]({{< param "main" >}}/docs/4.0/examples/floating-labels/) is brand new and builds on our sign-in example to provide a CSS-only implementation of the floating input label. This one's experimental and may see major changes before we bring it to Bootstrap proper.

- Finally, [Offcanvas]({{< param "main" >}}/docs/4.0/examples/offcanvas/) has been rewritten from the ground up to show off a navbar-built drawer, horizontal scrolling navigation, and some custom lists built on [media object]({{< param "main" >}}/docs/4.0/layout/media-object/) and utilities.

[Cover]({{< param "main" >}}/docs/4.0/examples/cover/), [Carousel]({{< param "main" >}}/docs/4.0/examples/carousel/), [Sign-in]({{< param "main" >}}/docs/4.0/examples/sign-in/), and our [framework examples]({{< param "main" >}}/docs/4.0/examples/#framework) only saw minor updates to improve code quality and fix a few smaller bugs. Overall this was a huge update for our examples and I'm excited to iterate on these and add more in future releases.

## Documenting our approach

New with v4 stable is a brief overview of some of the guiding principles behind why we do the things we do in Bootstrap. Our intent is to distill and document all the things we keep in our heads while writing code, building linters, and debugging. Much of this is focused on concepts and strategies for writing responsive CSS, using simple selectors, and limiting how much JavaScript one needs to write.

[Check out the new Approach page]({{< param "main" >}}/docs/4.0/extend/approach/), and be sure to open an issue or pull request with feedback and suggestions on what else to cover.

## Known issues

No release fixes every bug, and the same can be said for our v4 stable release. Here's some of the things that we're looking to tackle first in either a minor release (v4.1) or a patch release (v4.0.1) as time and scope allow.

- [Input groups, validation, and rounded corners.](https://github.com/twbs/bootstrap/issues/25110) I rewrote this for Beta 3 and I thought nailed it, but I was mistaken. We have some rounded corner issues and the only way we can fix them with CSS without breaking backward compatibility is by limiting how extensible the component can be made. We may need a modifier class to avoid some gnarly CSS and satisfy all the key functionality. Check out the issue and cross-linked PR for more details.

- Table variants, in particular `.table-active`, have a weird selector we've unintentionally left linger since prior releases. The bug results in [double application of an `rgba()` background color](https://github.com/twbs/bootstrap/issues/24529)—once for the `<tr>` and once for any `<td>`/`<th>` elements within.

There are a few more issues not yet confirmed or slated for our first patch release, but expect a handful of fixes coming your way before we hit the next minor release. We'll likely also package up the default branch change for our repository in this next patch release. We didn't have time to fit in testing a merge of a hugely divergent code base without nuking the entire Git history of v3. Again, more on that soon.

## Next releases

Speaking of releases, we're excited about the momentum we have going for us. Our [GitHub project boards](https://github.com/twbs/bootstrap/projects) are mostly up to date on upcoming releases, so feel free to jump in and take a look. Our next release will be v4.1 (pending any bugfix patches) and will focus on a slew of small new features, utilities, responsive font sizes, and more. From there we have a couple more minor releases that rally around another group of features.

We aim to make RTL part of an upcoming minor release depending on overall scope. It's taken us far too long to commit to this, but we're on it. Our current plan is focused on implementing this into our build tools and components so you conditionally serve, for example, `bootstrap.min.css` or `bootstrap-rtl.min.css`. Weigh in on the open issue please with any feedback; when we're ready, we'll tee up a fresh pull request with help from the community.

It's worth reiterating that each minor release will bring a new hosted version of our documentation. Right now, we have `getbootstrap.com/docs/4.0/` and come v4.1's release, we'll have that plus `getbootstrap.com/docs/4.1/`. Prior releases will continue to be linked from our navigation as is already the case for v3.x and the last v4 alpha.

## Themes update

[Bootstrap Themes]({{< param "themes" >}}) are getting a major update this year! We've been absolutely thrilled with the response since we originally launched Bootstrap Themes and we're finally ready to share our plans for what's next.

For the past few months, we've been working with some amazing theme creators to bring their awesome work to the Official Bootstrap Themes store. We couldn't be more excited to announce we're expanding Bootstrap Themes to include ten brand new themes. We're currently targeting a first quarter launch with themes all built on Bootstrap 4 (sorry, no v3 for these). Depending on final reviews, we might even get them to y'all in the coming weeks.

So much of Bootstrap's reach and usefulness comes directly from designers, developers, and creators all over the world building businesses with and on top of Bootstrap. We want to use our platform to give these creators an even larger audience and provide y'all with the best Bootstrap team-approved themes.

Stay tuned for more information as we get ready to launch.

## Thank you

Finally, one last thank you to everyone who's contributed to Bootstrap 4. It's been a crazy journey and I'm personally relieved, thrilled, and anxious to call it stable. There have been roughly 6,000 commits to v4 since we first starting working on it back in 2015. We've gone every which direction and rewrote far too many things far too many times, but I'm so very happy and fortunate with where we landed.

Cheers once again to everyone who's contributed to and built with Bootstrap. It's an honor to be building these kind of tools alongside and for all of you.
