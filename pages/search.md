---
layout: page
title: Search Documentation
permalink: /search/
---

<div class="search-filters">
  <button onclick="filterBySpecialty('all')">All</button>
  <button onclick="filterBySpecialty('Cardiology')">Cardiology</button>
  <button onclick="filterBySpecialty('Endocrinology')">Endocrinology</button>
</div>

<div id="search-results">
  {% for collection in site.collections %}
    {% unless collection.label == 'posts' or collection.label == 'tabs' %}
      {% for document in collection.docs %}
        <div class="search-item" data-specialty="{{ document.specialty }}">
          <h3><a href="{{ document.url | relative_url }}">{{ document.title }}</a></h3>
          <p>Collection: {{ collection.label | capitalize }}</p>
          <p>Specialty: {{ document.specialty }}</p>
        </div>
      {% endfor %}
    {% endunless %}
  {% endfor %}
</div>
