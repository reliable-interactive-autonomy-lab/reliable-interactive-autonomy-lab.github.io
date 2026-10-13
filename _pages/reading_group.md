---
title: "HRI Reading Group"
description: "The Human-Robot Interaction reading group at Indiana University Bloomington, hosted by the Reliable Interactive Autonomy (RIA) Lab: weekly discussion of recent work in HRI, interactive machine learning, and human-AI collaboration."
layout: textlay
permalink: /reading-group/
---

# HRI Reading Group

The HRI Reading Group at Indiana University is an open, weekly discussion of recent work in human-robot interaction, interactive machine learning, and human-AI collaboration. 


### Logistics

When
: Fridays, 10:00am-11:00am Eastern Time Zone

Where
: Luddy AI Center, Conference Room 3053

Format
: The HRI Reading Group uses a variety of formats to encourage discussion and engagement with current research. For standard paper discussions, one person leads a ~30-minute walkthrough of a selected paper, followed by an open group discussion. We also host invited speakers who share and discuss their recent work, as well as conference retrospectives highlighting interesting papers, talks, and emerging themes from recent HRI-related conferences.

Mailing list
: Email [Sunny Qiao](mailto:qiao@iu.edu) to be added
{: .lab-facts}

### Schedule

The full, live schedule is in the [reading group spreadsheet]({{ site.data.reading_group.sheet }}).

{% assign next = site.data.reading_group.upcoming | first %}
{% if next %}

#### Next up

<div class="well">
  <p><strong>{% if next.link %}<a href="{{ next.link }}">{{ next.title }}</a>{% else %}{{ next.title }}{% endif %}</strong>{% if next.venue %} &middot; <em>{{ next.venue }}</em>{% endif %}</p>
  <p>{{ next.date }} &middot; led by {{ next.leader }}</p>
</div>

{% endif %}

{% if site.data.reading_group.past %}

#### Past papers

{% for sem in site.data.reading_group.past %}
<details>
<summary markdown="span"><strong>{{ sem.semester }}</strong></summary>
<table class="table">
  <thead><tr><th>Date</th><th>Paper</th><th>Led by</th></tr></thead>
  <tbody>
  {% for item in sem.sessions %}
    <tr>
      <td>{{ item.date }}</td>
      <td>{% if item.link %}<a href="{{ item.link }}">{{ item.title }}</a>{% else %}{{ item.title }}{% endif %}{% if item.venue %} <br /><em>{{ item.venue }}</em>{% endif %}</td>
      <td>{{ item.leader }}</td>
    </tr>
  {% endfor %}
  </tbody>
</table>
</details>
{% endfor %}

{% endif %}
