---
title: "RIA Lab - HRI Reading Group"
layout: textlay
excerpt: "Human-Robot Interaction reading group at Indiana University."
sitemap: false
permalink: /reading-group/
---

# HRI Reading Group

The HRI Reading Group at Indiana University is an open, weekly discussion of recent work in human-robot interaction, interactive machine learning, and human-AI collaboration. We read one paper a week — a mix of new conference papers, older work worth revisiting, and the occasional paper from outside robotics that reframes a problem we care about.

**Everyone is welcome**, inside and outside the lab, and at any level. You do not need a robotics background, and you do not need to have finished the paper to come.

### Logistics

When
: Thursdays, 3:00pm-4:00pm Eastern Time Zone

Where
: Luddy AI Conference Room 2053 - BLLU 3053

Format
: The HRI Reading Group uses a variety of formats to encourage discussion and engagement with current research. For standard paper discussions, one person leads a ~30-minute walkthrough of a selected paper, followed by an open group discussion. We also host invited speakers who share and discuss their recent work, as well as conference retrospectives highlighting interesting papers, talks, and emerging themes from recent HRI-related conferences.
{: .lab-facts}

<!-- To re-add the mailing list row, paste these two lines directly above the
     `{: .lab-facts}` marker (the marker must stay on the line right after the
     last entry, or the whole block loses its styling):

Mailing list
: Email [{{ site.email }}](mailto:{{ site.email }}) to be added
-->

### Schedule

{% if site.data.reading_group %}

| Date | Paper | Led by |
| --- | --- | --- |
{% for item in site.data.reading_group %}| {{ item.date }} | {% if item.link %}[{{ item.title }}]({{ item.link }}){% else %}{{ item.title }}{% endif %}{% if item.venue %} <br><em>{{ item.venue }}</em>{% endif %} | {{ item.leader }} |
{% endfor %}

{% else %}

The schedule for the coming semester will be posted here. Email [{{ site.email }}](mailto:{{ site.email }}) to join the mailing list and get the weekly announcement.

{% endif %}
