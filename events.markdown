---
layout: page
title: Événements
permalink: /events/
---

Le MS20 participe activement à des événements :

<div class="events-wrapper">

{% for event in site.events %}
  <div class="event-card">
    <h3><a href="{{ event.url }}">{{ event.title }}</a></h3>
    <p>{{ event.excerpt }}</p>

    <ul class="social-media-list">
      <li>
        <svg class="svg-emoji"><use xlink:href="{{ '/assets/emojis/calendar.svg' | relative_url }}"></use></svg>
        {{ event.mois }}
      </li>
      <li>
        <svg class="svg-emoji"><use xlink:href="{{ '/assets/emojis/repeat.svg' | relative_url }}"></use></svg>
        {{ event.periodicite }}
      </li>
      <li>
        <svg class="svg-emoji"><use xlink:href="{{ '/assets/emojis/location.svg' | relative_url }}"></use></svg>
        {{ event.lieu }}
      </li>
      {% if event.site %}
      <li>
        <svg class="svg-emoji"><use xlink:href="{{ '/assets/emojis/web.svg' | relative_url }}"></use></svg>
        <a href="{{ event.site }}" target="_blank" rel="noopener">Site officiel</a>
      </li>
      {% endif %}
    </ul>
  </div>
{% endfor %}

</div>
