---
title: Get-Started
layout: default
---

# Get-Started

All notable user-facing changes to this project are documented in this file.

{: .highlight }
The project underwent a major maintenance shift in March 2022.

## HEAD

{: .note }
This website is built from the `HEAD` of the `main` branch of the theme repository.

Code changes to `main` that are *not* in the latest release:

- N/A

Docs changes made since the latest release:

- N/A

## Release v0.10.0

Hi folks! This minor release adds one of our most-requested features: unlimited multi-level navigation (also known as recursive navigation). Huge thanks to [@pdmosses] for his wonderful work in implementing this feature!

This release should be a straightforward upgrade for all users of Just the Docs. Thank you for your continued support!

### Using Release `v0.10.0`

Users who have not pinned the theme version will be **automatically upgraded to `v0.9.0` the next time they build their site**.

To use this release explicitly as a remote theme:

```yml
remote_theme: just-the-docs/just-the-docs@v0.10.0
```

To use this version explicitly as a gem-based theme, pin the version in your `Gemfile` and re-run `bundle install` or `bundle update just-the-docs`:

```ruby
gem "just-the-docs", "0.10.0"
```

To use and pin a previous version of the theme, replace the `0.10.0` with the desired release tag.

### New Features

- Added: Allow unlimited multi-level navigation by [@pdmosses] in [#1431]

### Documentation

- Added: Allow unlimited multi-level navigation by [@pdmosses] in [#1440]
- Added: sitemap (via `jekyll-sitemap` plugin) by [@mattxwang] in [#1530]
- Fixed: (non-systemic) accessibility issues flagged by aXe by [@mattxwang] in [#1531]

[#1431]: https://github.com/just-the-docs/just-the-docs/pull/1431
[#1440]: https://github.com/just-the-docs/just-the-docs/pull/1440
[#1530]: https://github.com/just-the-docs/just-the-docs/pull/1530
[#1530]: https://github.com/just-the-docs/just-the-docs/pull/1531

## Release v0.9.0

Hi folks! This minor release adds a `nav_enabled` set of variables to enable/disable the navigation at a site, layout, and page level --- and uses that to add search and auxilary links to the `minimal` layout. In addition, it fixes `search-data.json` corruption with default layouts and some minor CSS/SCSS issues.

This release should be a straightforward upgrade for all users of Just the Docs. Thank you for your continued support!

### Using Release `v0.9.0`

Users who have not pinned the theme version will be **automatically upgraded to `v0.9.0` the next time they build their site**.

To use this release explicitly as a remote theme:

```yml
remote_theme: just-the-docs/just-the-docs@v0.9.0
```

To use this version explicitly as a gem-based theme, pin the version in your `Gemfile` and re-run `bundle install` or `bundle update just-the-docs`:

```ruby
gem "just-the-docs", "0.9.0"
```

To use and pin a previous version of the theme, replace the `0.9.0` with the desired release tag.

### New Features

- Added: `nav_enabled` site, layout, and page-level variable to selectively show or hide the side/mobile menu by [@kevinlin1] in [#1441]
- Added: site-wide search bar and auxiliary links to the `minimal` layout by [@kevinlin1] in [#1441]

### Bugfixes

- Fixed: protect `search-data.json` file from front matter default for layout by [@mattxwang] in [#1468]
- Fixed: Sass mixed declarations by [@bobvandevijver] in [#1495]
- Fixed: redundant `monospace` in `pre`, `code`, `kbd`, `samp` reset by [@mattxwang] in [#1508]

### Documentation

- Docs: Explained the `nav_enabled` variables as an alternative to using the minimal layout [@kevinlin1] in [#1441].

### New Contributors

- [@bobvandevijver] made their first contribution in [#1495]

[@bobvandevijver]: https://github.com/bobvandevijver

[#1441]: https://github.com/just-the-docs/just-the-docs/pull/1441
[#1468]: https://github.com/just-the-docs/just-the-docs/pull/1468
[#1495]: https://github.com/just-the-docs/just-the-docs/pull/1495
[#1508]: https://github.com/just-the-docs/just-the-docs/pull/1508

## Release v0.8.2

Hi everyone! This patch release fixes a bug where a default layout with unrestricted `scope` (`path: ""`) breaks JavaScript functionality. Users who do not use a default layout with unrestricted `scope` should not be affected. This should be a straightforward upgrade for all users. Thank you to [@pdmosses] for triaging and fixing the bug!

### Bugfixes

- Fixed: Protect theme JS file from front matter default for layout by [@pdmosses] in [#1447]

[#1447]: https://github.com/just-the-docs/just-the-docs/pull/1447

## Release v0.8.1

Hi folks! This patch release fixes a bug introduced in `0.8.0` that affects users who build their sites in strict mode. It is a straightforward upgrade that should require no manual migration changes. Thank you to [@Zarthus] for quickly catching and fixing this bug!

### Bugfixes

- Fixed: Liquid filter typo in breadcrumb component (`strip` instead of `trim`) by [@Zarthus] in [#1434]

### Documentation

- Build docs site using strict mode and `strict_filters` by [@Zarthus] in [#1435]

### New Contributors

- [@Zarthus] made their first contribution in [#1434]

[@Zarthus]: https://github.com/Zarthus

[#1434]: https://github.com/just-the-docs/just-the-docs/pull/1434
[#1435]: https://github.com/just-the-docs/just-the-docs/pull/1435

## Release v0.8.0

Hi folks! This first minor release of 2024 has a short number of changes: a large improvement of build times for large sites, a new keyboard shortcut to focus the search bar, and sidebar navigation bugfixes for "pretty" URLs (with `.html` omitted) and the clickable area on Safari. This release has no explicit breaking changes and should be a straightforward upgrade for most (if not all) users.

### Using Release `v0.8.0`

Users who have not pinned the theme version will be **automatically upgraded to `v0.8.0` the next time they build their site**.

To use this release explicitly as a remote theme:

```yml
remote_theme: just-the-docs/just-the-docs@v0.8.0
```

To use this version explicitly as a gem-based theme, pin the version in your `Gemfile` and re-run `bundle install` or `bundle update just-the-docs`:

```ruby
gem "just-the-docs", "0.8.0"
```

To use and pin a previous version of the theme, replace the `0.8.0` with the desired release tag.

### New Features

- Added: configurable keyboard shortcut to focus search input by [@kcromanpl-bajra] in [#1411]

### Bugfixes

- Fixed: quicker build by [@pdmosses] in [#1397]
- Fixed: incorrect navigation when `.html` omitted from URL by [@pdmosses] in [#1374]
- Fixed: incorrect positioning of clickable area for navigation links on Safari by [@mattxwang] in [#1403]

### Documentation

- Add documentation to "Navigation Structure" on grouping pages with collections by [@mitchnemirov] in [#1390]

### New Contributors

- [@mitchnemirov] made their first contribution in [#1390]
- [@kcromanpl-bajra] made their first contribution in [#1411]

[@mitchnemirov]: https://github.com/mitchnemirov
[@kcromanpl-bajra]: https://github.com/kcromanpl-bajra

[#1374]: https://github.com/just-the-docs/just-the-docs/pull/1374
[#1390]: https://github.com/just-the-docs/just-the-docs/pull/1390
[#1397]: https://github.com/just-the-docs/just-the-docs/pull/1397
[#1403]: https://github.com/just-the-docs/just-the-docs/pull/1403
[#1411]: https://github.com/just-the-docs/just-the-docs/pull/1411

## Release v0.7.0

Hi folks! This is a minor release that adds a new configuration option for opening external links in a new tab and provides many bugfixes (in both correctness and performance) for Just the Docs users with large sites. We anticipate that for most users, this is a straightforward upgrade. However, it introduces some potentially-breaking *internal* changes to undocumented features of the theme.

### Migrating to `v0.7.0`

**Migration**: users will need to migrate if:

- they overrode `_includes/nav.html`, which has moved to `_includes/components/nav.html`
- they have an element with the IDs `jtd-nav-activation` or `jtd-head-nav-stylesheet`

For more, refer to the [migration guide](https://just-the-docs.com/MIGRATION/).

