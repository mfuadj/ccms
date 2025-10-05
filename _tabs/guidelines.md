---
layout: page
title: Guidelines
icon: fas fa-clipboard-list
order: 6
---

# Practice Guidelines

{% for guideline in site.guidelines %}
  {% assign specialty = site.data.specialties[guideline.specialty_key] %}
  <div class="guideline-item">
    <div class="specialty-badge" style="border-left: 4px solid {{ specialty.color }};">
      <i class="{{ specialty.icon }}"></i> {{ specialty.name }}
    </div>
    <h3><a href="{{ guideline.url | relative_url }}">{{ guideline.title }}</a></h3>
    <p class="guideline-meta">
      <strong>Last Updated:</strong> {{ guideline.last_updated | date: "%B %d, %Y" }}<br>
      <strong>Urgency:</strong> {{ guideline.urgency | capitalize }}
    </p>
    <p>{{ guideline.description }}</p>
    <div class="tags">
      {% for tag in guideline.tags %}
        <span class="tag">{{ tag }}</span>
      {% endfor %}
    </div>
  </div>
  <hr>
{% endfor %}
