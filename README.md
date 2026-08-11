# Reliable Interactive Autonomy (RIA) Lab

Website for the Reliable Interactive Autonomy Lab, led by [Michelle Zhao](https://michellezhao.net/) in the Luddy School of Informatics, Computing, and Engineering at Indiana University Bloomington.

Published at <https://reliable-interactive-autonomy-lab.github.io/>.

## Editing

Most updates are one-line edits to a data file in `_data/`:

| What | Where |
| --- | --- |
| News | `_data/news.yml` |
| Publications | `_data/publist.yml` |
| Faculty | `_data/team_members.yml` |
| PhD students | `_data/phd_students.yml` |
| Master's / undergraduate students | `_data/students.yml` |
| Alumni | `_data/alumni_members.yml` |

Page prose lives in `_pages/`. Colors and fonts are in `_sass/_ria-variables.scss`; other style overrides are in `css/main.scss`. Headshots go in `images/teampic/` — any portrait aspect ratio works, since CSS square-crops them from the top.

See [`_pages/aboutwebsite.md`](_pages/aboutwebsite.md) for the longer version.

## Running locally

```
bundle install
bundle exec jekyll serve
```

Then open <http://localhost:4000>.

## Credits

Built with [Jekyll](https://jekyllrb.com), [Bootstrap](https://getbootstrap.com), and [Bootswatch](https://bootswatch.com), adapted from the [Allan Lab group template](https://github.com/allanlab/allanlab). Code released under the MIT License.
