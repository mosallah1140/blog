---
author: mdo
date: "2019-11-26T00:00:00Z"
title: Bootstrap 4.4.0
video: P5ZJui3aPoQ
---

Bootstrap 4 has a new update with a handful of feature changes. We’ve had quite the lengthy pull request to add responsive containers—big thanks to the developers who contribute to Bootstrap for sticking with it and helping us along the way. Nearly all new features will be carried forward into Bootstrap 5, so feel free to start using them now.

## Highlights

Here's what you need to know about v4.4.0. Remember that with every minor and major release of Bootstrap, we ship a new URL for our hosted docs to ensure URLs continue to work.

- **New responsive containers!** Over a year in the making, fluid up to a particular breakpoint, available for all responsive tiers.
- **New responsive `.row-cols` classes** for quickly specifying the number of columns across breakpoints. This one is huge for those of you who have asked for responsive card decks.
- **New `escape-svg()` function** for simplifying our embedded `background-image` SVGs for forms and more.
- **New `add()` and `subtract()` functions** for avoiding errors and zero values from CSS’s built in `calc` feature.
- **New `make-col-auto()` mixin** to make our `.col-auto` class available with custom HTML.
- Fixed an issue with Microsoft Edge not picking up `:disabled` styles by moving selectors to `[disabled]`.
- **Deprecated:** `bg-variant()`, `nav-divider()`, and `form-control-focus()` mixins are now deprecated as they're going away in v5.
- Updated our spacing and alignment for modal footer elements like buttons to automatically wrap when space is constrained.
- More flexible form control validation styles thanks to fewer chained selectors. Also updated the `:invalid` validation icon to be an alert instead of an `&times;` to avoid confusion with browser functionality for clearing the form field value.
- Fixed a couple dozen CSS and JS bugs.
- Moved to GitHub Actions for CI/CD! Expect more updates to our CI setup over time here while Actions evolves.
- Updated documentation to fix links and typos, improved landmarks for secondary navigation, and a new security doc for guidelines on reporting potential vulnerabilities.

We've shipped a lot more in this release, so be sure to check out the [v4.4.0 ship list of closed issues and merged pull requests](https://github.com/twbs/bootstrap/issues?q=project%3Atwbs%2Fbootstrap%2F18+is%3Aclosed+sort%3Aupdated-desc) for more details.

[Head to to the v4.4.0 docs](https://getbootstrap.com/docs/4.4/) to see the latest in action. The full release has been published to npm and will soon appear on the BootstrapCDN and Rubygems.

## Support the team

Visit our [Open Collective page]({{< param "opencollective" >}}) or our [team members](https://github.com/orgs/twbs/people)' GitHub profiles to help support the maintainers contributing to Bootstrap.
