---
title: "News"
description: "News and announcements from the Reliable Interactive Autonomy (RIA) Lab at Indiana University Bloomington."
layout: textlay
permalink: /allnews.html
---

# News

{% for article in site.data.news %}
<p><em>{{ article.date }}</em> <br> {{ article.headline | markdownify | remove: '<p>' | remove: '</p>' | strip }}</p>
{% endfor %}
