---
title: "About this website"
description: "How the Reliable Interactive Autonomy (RIA) Lab website is built and maintained."
sitemap: false
layout: textlay
permalink: /aboutwebsite.html
noindex: true
---

# About this website

This site is built with [Jekyll](https://jekyllrb.com), styled with [Bootstrap](https://getbootstrap.com) and [Bootswatch](https://bootswatch.com), and hosted on [GitHub Pages](https://pages.github.com). It is adapted from the [Allan Lab academic group template](https://github.com/allanlab/allanlab), released under the MIT License.

### How to update it

Most routine updates only require editing a plain-text file in `_data/`:

| What | Where |
| --- | --- |
| News items (home page + `/allnews.html`) | `_data/news.yml` |
| Publications | `_data/publist.yml` |
| PhD students | `_data/phd_students.yml` |
| Master's and undergraduate students | `_data/students.yml` |
| Alumni | `_data/alumni_members.yml` |

Page prose lives in `_pages/`. YAML is whitespace-sensitive, so match the indentation of the surrounding entries exactly and check the build after each change.

A few conventions specific to this site:

- In `publist.yml`, setting `highlight: 1` promotes an entry to the **Selected work** grid on the publications page. Adding `image: something.png` (placed in `images/pubpic/`) shows a thumbnail; entries without an image render fine.
- The nine most recent entries in `news.yml` appear in the home-page sidebar; the rest are on `/allnews.html`.
- Team members without a `photo:` field render without an image, so people can be added before headshots exist. Headshots go in `images/teampic/` and are square-cropped from the top by CSS, so any portrait aspect ratio works.
- A rotating image banner is available on the home page — drop images into `images/slider7001400/` and uncomment the carousel block in `_pages/home.md`.

### Search visibility

The site's identity — how it describes itself to Google and to anyone sharing a
link — is configured in one place, `_config.yml`:

| What | Where |
| --- | --- |
| Lab name, description, canonical URL | top of `_config.yml` |
| Department / school / university names and links | `institution:`, `school:`, `department:` |
| Director's name, title, and scholarly identifiers | `director:` |
| Research topics used in metadata | `research_areas:` |

Those values feed three things automatically: the `<title>`, description, and
social-preview tags in `_includes/head.html`; the schema.org structured data in
`_includes/structured-data.html`, which tells search engines that the RIA Lab is
part of Indiana University and is directed by Michelle Zhao; and the identity
block rendered by `_includes/director-card.html` on the home and team pages.

Two per-page front-matter keys are available:

- `description:` — the meta description for that page. Write one per page; it is
  often what Google shows underneath the link.
- `seo_title:` — overrides the `<title>` completely. Without it, the title is
  built as `<page title> | RIA Lab, Indiana University Bloomington`.

`sitemap: false` keeps a page out of `sitemap.xml`, and `noindex: true` asks
search engines not to index it; both are set on the 404 and this page. Everything
else is listed in `sitemap.xml`, which is generated on every build and pointed to
from `robots.txt`.

### Theme

Colors and fonts live in `_sass/_ria-variables.scss`, imported ahead of the Bootstrap variables so its values win. The palette is Indiana University crimson (`#990000`), and type is set in Palatino with fallbacks for Windows, Linux, and Georgia. Layout tweaks that aren't simple variable changes go in `css/main.scss`.

### Running it locally

```
bundle install
bundle exec jekyll serve
```

Then open <http://localhost:4000>.
