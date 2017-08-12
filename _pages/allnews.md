---
title: "Group News"
layout: textlay
excerpt: "News from the Vidyavriksh Research Lab."
sitemap: false
permalink: /allnews.html
---

# News

{% for article in site.data.news %}
<p>{{ article.date }} <br>
<em>{{ article.headline }}</em></p>
{% endfor %}
