---
title: "RIA Lab - Publications"
layout: gridlay
excerpt: "RIA Lab -- Publications."
sitemap: false
permalink: /publications/
---


# Publications

**A full and continuously updated list is available on [Google Scholar](https://scholar.google.com/citations?user=Gu4eXZwAAAAJ&hl=en). The [complete list](#full-list-of-publications) is also at the bottom of this page.**

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
  <p><strong><a href="{{ publi.link.url }}">{{ publi.link.display }}</a></strong></p>
  {% else %}
  <p><strong>{{ publi.link.display }}</strong></p>
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

{% for publi in site.data.publist %}

  {{ publi.title }} <br />
  <em>{{ publi.authors }}</em><br />
  {% if publi.link.url %}<a href="{{ publi.link.url }}">{{ publi.link.display }}</a>{% else %}{{ publi.link.display }}{% endif %}

{% endfor %}

<p> &nbsp; </p>

<em>* denotes equal contribution.</em>
