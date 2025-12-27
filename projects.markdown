---
layout: page
title: Projets
permalink: /projects/
---

Découvrez les projets du makerspace :

{% for project in site.projects %}
  <div>
    <h3><a href="{{ project.url | relative_url }}">{{ project.title }}</a></h3>
  </div>
{% endfor %}