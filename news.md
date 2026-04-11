---
layout: page
title: "News"
subtitle: "Updates and news"
permalink: /news/
---

<!-- 
  ISTRUZIONI PER TE (Alessio):
  Questa pagina mostra automaticamente tutte le news che scrivi.
  Tu non devi modificare QUESTO file per aggiungere news.
  
  Per aggiungere una nuova news, crei un FILE NUOVO nella cartella _posts/
  Il file deve chiamarsi: ANNO-MESE-GIORNO-titolo.md
  Per esempio: 2026-04-08-nuovo-concerto.md
  
  Guarda i file di esempio nella cartella _posts/ per capire il formato.
-->

<div class="news-list">
  {% for post in site.posts %}
  <article class="news-item">
    <time class="news-date" datetime="{{ post.date | date_to_xmlschema }}">
      {{ post.date | date: "%d/%m/%Y" }}
    </time>
    <h3 class="news-title">
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    </h3>
    {% if post.excerpt %}
    <p class="news-excerpt">{{ post.excerpt | strip_html | truncatewords: 30 }}</p>
    {% endif %}
  </article>
  {% endfor %}
</div>
