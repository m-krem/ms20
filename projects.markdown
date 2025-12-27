---
layout: page
title: Projets
permalink: /projects/
---

Découvrez les projets du makerspace :

<div class="projects-wrapper">

{% for project in site.projects %}
  <div class="site-card">
    <h3><a href="{{ project.url | relative_url }}">{{ project.title }}</a></h3>
  </div>
{% endfor %}

</div>
