---
layout: page
title: "Eventi"
subtitle: "Concerti e appuntamenti"
permalink: /eventi/
---

{% assign upcoming = site.data.events | where: "status", "upcoming" | sort: "date" %}
{% assign past = site.data.events | where: "status", "past" | sort: "date" | reverse %}

{% if upcoming.size > 0 %}
<div class="events-section">
  <h2 class="events-section-title">Prossimi eventi</h2>
  <div class="event-list">
    {% for event in upcoming %}
    <div class="event-item">
      <div class="event-main">
        <div class="event-date-block">
          <span class="event-day">{{ event.date | date: "%-d" }}</span>
          <span class="event-month">{{ event.date | date: "%B %Y" }}</span>
        </div>
        <div class="event-info">
          {% if event.url %}
          <h3 class="event-title"><a href="{{ event.url }}">{{ event.title }}</a></h3>
          {% else %}
          <h3 class="event-title">{{ event.title }}</h3>
          {% endif %}
          <p class="event-venue">{{ event.location }}</p>
          {% if event.time %}<p class="event-venue">Ore {{ event.time }}</p>{% endif %}
          {% if event.description %}<p class="event-description">{{ event.description }}</p>{% endif %}
        </div>
      </div>
      {% if event.locandina %}
      <div class="event-locandina-col">
        <img class="event-locandina" src="{{ event.locandina | relative_url }}" alt="Locandina {{ event.title }}">
      </div>
      {% endif %}
    </div>
    {% endfor %}
  </div>
</div>
{% endif %}

{% if past.size > 0 %}
<div class="events-section">
  <h2 class="events-section-title">Eventi passati</h2>
  <div class="event-list">
    {% for event in past %}
    <div class="event-item">
      <div class="event-main">
        <div class="event-date-block">
          <span class="event-day">{{ event.date | date: "%-d" }}</span>
          <span class="event-month">{{ event.date | date: "%B %Y" }}</span>
        </div>
        <div class="event-info">
          {% if event.url %}
          <h3 class="event-title"><a href="{{ event.url }}">{{ event.title }}</a></h3>
          {% else %}
          <h3 class="event-title">{{ event.title }}</h3>
          {% endif %}
          <p class="event-venue">{{ event.location }}</p>
          {% if event.time %}<p class="event-venue">Ore {{ event.time }}</p>{% endif %}
          {% if event.description %}<p class="event-description">{{ event.description }}</p>{% endif %}
        </div>
      </div>
      {% if event.locandina %}
      <div class="event-locandina-col">
        <img class="event-locandina" src="{{ event.locandina | relative_url }}" alt="Locandina {{ event.title }}">
      </div>
      {% endif %}
    </div>
    {% endfor %}
  </div>
</div>
{% endif %}
