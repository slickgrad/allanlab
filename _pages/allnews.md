---
title: "News"
layout: textlay
excerpt: "TERM Lab at the University at Buffalo."
sitemap: false
permalink: /allnews.html
---

# News

{% for article in site.data.news %}
<p>{{ article.date }} <br>
<em>{{ article.headline }}</em></p>
{% if article.image %}
<img src="{{ article.image | relative_url }}" class="img-responsive" style="max-width: 192px" />
{% endif %}
{% endfor %}
