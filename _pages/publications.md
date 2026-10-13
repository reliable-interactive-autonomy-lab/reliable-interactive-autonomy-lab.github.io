---
title: "Publications"
description: "Publications from the Reliable Interactive Autonomy (RIA) Lab at Indiana University Bloomington, on robot learning, human-robot interaction, conformal prediction, and human-AI collaboration."
layout: gridlay
permalink: /publications/
---


# Publications

A more complete list is available on [Google Scholar](https://scholar.google.com/citations?user=Gu4eXZwAAAAJ&hl=en).

## Selected work

{% assign number_printed = 0 %}
{% for publi in site.data.publist %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if publi.highlight == 1 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
 <div class="well">
  <pubtit>{{ publi.title }}</pubtit>
  {% if publi.image %}
  <img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ publi.image }}" class="img-responsive" width="33%" style="float: left" />
  {% endif %}
  <p>{{ publi.description }}</p>
  <p><em>{{ publi.authors }}</em></p>
  {% if publi.link.url %}
  <p><strong><a href="{{ publi.link.url }}">{{ publi.link.display }}</a></strong>{% if publi.pdf %} &middot; <a href="{{ site.url }}{{ site.baseurl }}/downloads/{{ publi.pdf }}">[PDF]</a>{% endif %}</p>
  {% else %}
  <p><strong>{{ publi.link.display }}</strong>{% if publi.pdf %} &middot; <a href="{{ site.url }}{{ site.baseurl }}/downloads/{{ publi.pdf }}">[PDF]</a>{% endif %}</p>
  {% endif %}
  {% if publi.news1 %}<p class="text-danger"><strong>{{ publi.news1 }}</strong></p>{% endif %}
  {% if publi.news2 %}<p>{{ publi.news2 }}</p>{% endif %}
 </div>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endif %}
{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

<p> &nbsp; </p>


## Full list of publications

<details>
<summary markdown="span"><strong>Click to expand the full publication list</strong></summary>

{% for publi in site.data.publist %}
<p>
  {{ publi.title }} <br />
  <em>{{ publi.authors }}</em><br />
  {% if publi.link.url %}<a href="{{ publi.link.url }}">{{ publi.link.display }}</a>{% else %}{{ publi.link.display }}{% endif %}{% if publi.pdf %} &middot; <a href="{{ site.url }}{{ site.baseurl }}/downloads/{{ publi.pdf }}">[PDF]</a>{% endif %}
</p>
{% endfor %}

<p><em>* denotes equal contribution.</em></p>

</details>

<p> &nbsp; </p>
