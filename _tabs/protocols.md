---
layout: page
title: Protocols
icon: fas fa-file-medical-alt
order: 5
---

# Clinical Protocols

<div class="protocol-grid">
{% for protocol in site.protocols %}
  {% assign specialty = site.data.specialties[protocol.specialty_key] %}
  <div class="protocol-card">
    <div class="specialty-badge" style="border-left: 4px solid {{ specialty.color }};">
      <i class="{{ specialty.icon }}"></i> {{ specialty.name }}
    </div>
    <h3><a href="{{ protocol.url | relative_url }}">{{ protocol.title }}</a></h3>
    <p class="protocol-meta">
      <strong>Last Updated:</strong> {{ protocol.last_updated | date: "%B %d, %Y" }}<br>
      <strong>Urgency:</strong> {{ protocol.urgency | capitalize }}
    </p>
    <p>{{ protocol.description }}</p>
    <div class="tags">
      {% for tag in protocol.tags %}
        <span class="tag">{{ tag }}</span>
      {% endfor %}
    </div>
  </div>
  <hr>
{% endfor %}
</div>
