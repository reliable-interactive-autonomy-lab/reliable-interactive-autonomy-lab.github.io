---
title: "Photos"
description: "Photos from the Reliable Interactive Autonomy (RIA) Lab at Indiana University Bloomington."
layout: gridlay
permalink: /photos/
---

# Photos

{% if site.data.photos %}

Lab life, conferences, demos, and the occasional robot behaving unexpectedly.

<div id="picid">
{% assign number_printed = 0 %}
{% for pic in site.data.photos %}

{% assign even_odd = number_printed | modulo: 3 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-4">
  <img src="{{ site.url }}{{ site.baseurl }}/images/picpic/{{ pic.file }}" class="img-responsive" alt="{{ pic.caption }}" />
  {% if pic.caption %}<figcaption>{{ pic.caption }}</figcaption>{% endif %}
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 2 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 3 %}
{% if even_odd != 0 %}
</div>
{% endif %}
</div>

{% else %}

Photos from the lab will be posted here.

<!--
  To add photos: drop the image files into images/picpic/ and list them in
  _data/photos.yml, e.g.

    - file: lab_kickoff.jpg
      caption: First lab meeting, Fall 2026

  They will render in a three-across grid automatically.
-->

{% endif %}
