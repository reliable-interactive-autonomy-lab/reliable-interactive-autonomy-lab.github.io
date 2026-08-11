---
title: "RIA Lab - News"
layout: textlay
excerpt: "News from the Reliable Interactive Autonomy Lab."
sitemap: false
permalink: /allnews.html
---

# News

{% for article in site.data.news %}
<p><em>{{ article.date }}</em> <br> {{ article.headline | markdownify | remove: '<p>' | remove: '</p>' | strip }}</p>
{% endfor %}
