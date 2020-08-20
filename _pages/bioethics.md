---
title: "The Bioethics Forum"
layout: textlay
excerpt: "The Bioethics Forum"
sitemap: false
permalink: /bioethics.html
---



## Highlights

<!--(For a full list see [below](#full-list) or go to [Google Scholar](https://scholar.google.ch/citations?user=TqxYWZsAAAAJ), [ResearcherID](https://www.researcherid.com/rid/D-7763-2012)) -->

{% assign number_printed = 0 %}
{% for bioe in site.data.bioethics %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if bioe.highlight == 1 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
 <div class="well">
  <biotit>{{ bioe.title }}</biotit>
  <img src="{{ site.url }}{{ site.baseurl }}/images/bioethics/{{ bioe.image }}" class="img-responsive" width="40%" style="float: left" />
  <p>{{ bioe.description }}</p>
  <p><em>{{ bioe.authors }}</em></p>
  <p><strong><a href="{{ bioe.link.url }}">{{ bioe.link.display }}</a></strong></p>
  <p class="text-danger"><strong> {{ bioe.news1 }}</strong></p>
  <p> {{ bioe.news2 }}</p>
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
