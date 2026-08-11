---
title: "About this website"
layout: textlay
excerpt: "About this website."
sitemap: false
permalink: /aboutwebsite.html
---

# About this website

This site is built with [Jekyll](https://jekyllrb.com), styled with [Bootstrap](https://getbootstrap.com) and [Bootswatch](https://bootswatch.com), and hosted on [GitHub Pages](https://pages.github.com). It is adapted from the [Allan Lab academic group template](https://github.com/allanlab/allanlab), released under the MIT License.

### How to update it

Most routine updates only require editing a plain-text file in `_data/`:

| What | Where |
| --- | --- |
| News items (home page + `/allnews.html`) | `_data/news.yml` |
| Publications | `_data/publist.yml` |
| Faculty | `_data/team_members.yml` |
| PhD students | `_data/phd_students.yml` |
| Master's and undergraduate students | `_data/students.yml` |
| Alumni | `_data/alumni_members.yml` |

Page prose lives in `_pages/`. YAML is whitespace-sensitive, so match the indentation of the surrounding entries exactly and check the build after each change.

A few conventions specific to this site:

- In `publist.yml`, setting `highlight: 1` promotes an entry to the **Selected work** grid on the publications page. Adding `image: something.png` (placed in `images/pubpic/`) shows a thumbnail; entries without an image render fine.
- The nine most recent entries in `news.yml` appear in the home-page sidebar; the rest are on `/allnews.html`.
- Team members without a `photo:` field render without an image, so people can be added before headshots exist. Headshots go in `images/teampic/` and are square-cropped from the top by CSS, so any portrait aspect ratio works.
- A rotating image banner is available on the home page — drop images into `images/slider7001400/` and uncomment the carousel block in `_pages/home.md`.

### Theme

Colors and fonts live in `_sass/_ria-variables.scss`, imported ahead of the Bootstrap variables so its values win. The palette is Indiana University crimson (`#990000`), and type is set in Palatino with fallbacks for Windows, Linux, and Georgia. Layout tweaks that aren't simple variable changes go in `css/main.scss`.

### Running it locally

```
bundle install
bundle exec jekyll serve
```

Then open <http://localhost:4000>.
