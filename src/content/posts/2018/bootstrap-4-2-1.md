---
author: mdo
date: "2018-12-21T00:00:00Z"
title: Bootstrap 4.2.1
video: 4N1iwQxiHrs
---

Look out world, we're shipping Bootstrap v4.2.1 with a slew of new features, bug fixes, and docs updates. On the new features side, we have spinners, toasts, switches, and (finally!) touch support in the carousel. That's just the tip of the iceberg though.

**Heads up!** v4.2.0 was incorrectly published to npm, so we've had to immediately turnaround a v4.2.1 release. `npm i bootstrap@latest` should now return `4.2.1`. Apologies for the inconvenience!

We've crammed months of work into v4.2.1 with over 400 commits since our last v4.1.3 release. As mentioned in our v3.4.0 release last week, we're working to decouple our releases from my direct involvement to improve the shipping cadence. Expect more improvements there in 2019.

Keep reading for highlights and some insight into how we're getting to v4.3 quickly, and then into v5 (woo!).

## What's new

Here are the highlights of what's new and updated in v4.2.1.

![Bootstrap toasts](/assets/img/2018/12/toasts.png)

- **New:** Added a new [spinner loading component]({{< param "main" >}}/docs/4.2/components/spinners/).
- **New:** Added new [toast component]({{< param "main" >}}/docs/4.2/components/toasts/) for displaying notifications.
- **New:** Added a new [iOS style switch]({{< param "main" >}}/docs/4.2/components/forms/#switches) (a modifier class to our custom checkboxes).
- **New:** Added touch support in our carousel component.
- **New:** Added `.font-weight-lighter` and `.font-weight-bolder` utilities.
- **New:** Added `.text-decoration-none` utility class.
- **New:** Added `.modal-xl` modifier class for our modals.
- **New:** Added new negative margin utility classes (e.g., `.mb-n3`). These rad new classes not only allow you more control over your general spacing needs, but also allow you to create responsive grid gutters at each breakpoint.
- **New:** Validated form fields now have feedback icons on `:invalid` and `:valid` fields. Disable them with the `$enable-validation-icons` boolean Sass variable (defaults to `true`).
- **New:** Added a new [versions page]({{< param "main" >}}/docs/versions/) to our docs.
- **New:** Tooltips/Popovers work with Shadow DOM.
- **Updated:** Redesigned the custom checkboxes and radios for more obvious states.
- **Updated:** `bootstrap-grid.css` now includes our `margin` and `padding` utilities for full control of our grid system.
- **Updated:** Changed auto columns (e.g., `.col-auto`) from `max-width: none` to `max-width: 100%` to prevent content from causing a column to overflow the parent.
- **Updated:** Improved rendering of custom selects, ranges, file input, and more.

Checkout the full [v4.2.0 ship list](https://github.com/twbs/bootstrap/issues/26952) and [GitHub project](https://github.com/twbs/bootstrap/projects/6) for the full details. Up next is [v4.3](https://github.com/twbs/bootstrap/projects/16) with some bugfixes, a few new modifier classes and variables, and some new utilities.

[Head to the v4.2 docs]({{< param "main" >}}/docs/4.2/) to see the latest in action. The full release has been published to npm and will soon appear on the Bootstrap CDN and Rubygems.

## What's next

We have [v4.3](https://github.com/twbs/bootstrap/projects/16) already planned, so that's our immediate focus. However, while we're developing that in the `v4-dev` branch, we'll be getting our plans in order for a v5 release.

Bootstrap 5 will not feature drastic changes to the codebase. While I tweeted about the earnestness to move to PostCSS years ago, we'll still be on Sass for v5. Instead, we'll focus our efforts on removing cruft, improving existing components, and dropping old browsers and our jQuery dependency. There are also some updates to our v4.x components we cannot make without causing breaking changes, so v5 feels like it's coming at the right time for us.

Stay tuned for a preview of the plans for v5 in the new year. We'll share via an issue, ask for feedback, and then settle in to development mode.

Happy holidays, and happy new year to everyone! Thanks for continuing to make Bootstrap an amazing project and community.
