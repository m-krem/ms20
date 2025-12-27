---
layout: page
title: Membres
permalink: /members/
---

Vous trouverez ci-dessous les membres organisés par **promotion**, (année du Bac) :

<div class="members-wrapper">

{% assign sorted_members = site.members | sort: "year" | reverse %}
{% assign current_year = "" %}

{% for member in sorted_members %}
  {% if member.year != current_year %}
    {% assign current_year = member.year %}
    <h2>BAC {{ current_year }}</h2>
  {% endif %}

  <div class="member-card" {% if member.has_page %} onclick="location.href='{{ member.url }}'" {% endif %}>
    <h3>{{ member.title }}</h3>
    <p>
      {% if member.message %}{{ member.message }}<br>{% endif %}
      {% if member.projects %}<strong>{{ member.projects }}</strong>{% endif %}
    </p>
    <ul class="social-media-list">
      {% if member.linkedin %}
      <li>
        <a href="https://www.linkedin.com/in/{{ member.linkedin | cgi_escape | escape }}">
          <svg class="svg-icon"><use xlink:href="{{ '/assets/linkedin.svg' | relative_url }}"></use></svg>
          <span class="username">{{ member.linkedin | escape }}</span>
        </a>
      </li>
      {% endif %}
    </ul>
  </div>
{% endfor %}

</div>