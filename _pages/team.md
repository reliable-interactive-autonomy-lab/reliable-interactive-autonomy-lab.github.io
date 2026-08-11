---
title: "RIA Lab - Team"
layout: gridlay
excerpt: "RIA Lab: Team members"
sitemap: false
permalink: /team/
---

# Team

**We are looking for PhD students, Master's students, and undergraduates to join the lab** [(see how to join)]({{ site.url }}{{ site.baseurl }}/join/) **!**

Jump to [faculty](#faculty), [PhD students](#phd-students), [Master's and undergraduate students](#master-and-undergraduate-students).

## Faculty
{% assign number_printed = 0 %}
{% for member in site.data.team_members %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  {% if member.photo %}
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="team-photo" alt="{{ member.name }}" style="float: left" />
  {% endif %}
  <div class="member-meta">
  <h4>{{ member.name }}</h4>
  <i>{{ member.info }}</i>
  {% if member.email %}<br><i>{{ member.email }}</i>{% endif %}
  {% if member.links %}<br>{{ member.links }}{% endif %}
  </div>
  <ul style="overflow: hidden">

  {% if member.number_educ >= 1 %}
  <li> {{ member.education1 | markdownify | remove: '<p>' | remove: '</p>' }} </li>
  {% endif %}

  {% if member.number_educ >= 2 %}
  <li> {{ member.education2 | markdownify | remove: '<p>' | remove: '</p>' }} </li>
  {% endif %}

  {% if member.number_educ >= 3 %}
  <li> {{ member.education3 | markdownify | remove: '<p>' | remove: '</p>' }} </li>
  {% endif %}

  {% if member.number_educ >= 4 %}
  <li> {{ member.education4 | markdownify | remove: '<p>' | remove: '</p>' }} </li>
  {% endif %}

  {% if member.number_educ >= 5 %}
  <li> {{ member.education5 | markdownify | remove: '<p>' | remove: '</p>' }} </li>
  {% endif %}

  </ul>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}


## PhD Students

{% if site.data.phd_students %}
{% assign number_printed = 0 %}
{% for member in site.data.phd_students %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  {% if member.photo %}
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="team-photo" alt="{{ member.name }}" style="float: left" />
  {% endif %}
  <div class="member-meta">
  <h4>{{ member.name }}</h4>
  <i>{{ member.info }}</i>
  {% if member.email %}<br><i>{{ member.email }}</i>{% endif %}
  {% if member.links %}<br>{{ member.links }}{% endif %}
  {% if member.bio %}<p style="margin-top: 8px">{{ member.bio }}</p>{% endif %}
  </div>
  <ul style="overflow: hidden">
  {% if member.number_educ >= 1 %}<li> {{ member.education1 | markdownify | remove: '<p>' | remove: '</p>' }} </li>{% endif %}
  {% if member.number_educ >= 2 %}<li> {{ member.education2 | markdownify | remove: '<p>' | remove: '</p>' }} </li>{% endif %}
  {% if member.number_educ >= 3 %}<li> {{ member.education3 | markdownify | remove: '<p>' | remove: '</p>' }} </li>{% endif %}
  </ul>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}
{% else %}
The lab is actively recruiting. If that could be you, please [get in touch]({{ site.url }}{{ site.baseurl }}/join/).
{% endif %}


## Master and Undergraduate Students

{% if site.data.students %}
{% assign number_printed = 0 %}
{% for member in site.data.students %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <h4>{{ member.name }}</h4>
  <i>{{ member.info }}</i>
  <ul style="overflow: hidden">
  {% if member.number_educ >= 1 %}<li> {{ member.education1 }} </li>{% endif %}
  {% if member.number_educ >= 2 %}<li> {{ member.education2 }} </li>{% endif %}
  </ul>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}
{% else %}
Openings for Master's and undergraduate researchers are described on the [join page]({{ site.url }}{{ site.baseurl }}/join/).
{% endif %}


<!-- Alumni section — commented out until there are alumni. Uncomment the
     block below (and re-add the #alumni jump link above) to bring it back.

## Alumni

{% if site.data.alumni_members %}
{% assign number_printed = 0 %}
{% for member in site.data.alumni_members %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  {% if member.photo %}
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="team-photo" alt="{{ member.name }}" style="float: left" />
  {% endif %}
  <h4>{{ member.name }}</h4>
  <i>{{ member.duration }} <br> Role: {{ member.info }}</i>
  <ul style="overflow: hidden">
  </ul>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}
{% else %}
No alumni yet — the lab was founded in 2026.
{% endif %}

-->

