---
title: "Vidyavriksh Research Group - Projects"
layout: gridlay
excerpt: "Projects by the members of the group."
sitemap: false
permalink: /projects/
---
# Projects

### Coming soon!

{% assign number_printed = 0 %}
{% for project in site.data.projects %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if project.highlight == 1 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
 <div class="well">
  <pubtit>{{ project.title }}</pubtit>
  <img src="{{ site.url }}{{ site.baseurl }}/images/projectpic/{{ project.image }}" class="img-responsive" width="300%" style="float: middle" />
  <p>{{ project.description }}</p>
  <p><em>{{ project.people }}</em></p>
  <p><strong><a href="{{ project.link.url }}">{{ project.link.display }}</a></strong></p>
  <p><strong> {{ project.reference1 }}</strong></p>
  <p> {{ project.reference2 }}</p>
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