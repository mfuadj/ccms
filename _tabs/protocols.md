---
layout: page
title: Protocols
permalink: /protocols/
order: 2
---

<h2>Clinical Protocols</h2>
<p>Evidence-based clinical protocols for common conditions and procedures.</p>

{% for protocol in site.protocols %}
<div class="protocol-item">
  <h3><a href="{{ protocol.url | relative_url }}">{{ protocol.title }}</a></h3>
  <p><strong>Specialty:</strong> {{ protocol.specialty }}</p>
  <p><strong>Last Updated:</strong> {{ protocol.last_updated | date: "%B %d, %Y" }}</p>
  <p>{{ protocol.excerpt | strip_html }}</p>
  <div class="tags">
    {% for tag in protocol.tags %}
      <span class="tag">{{ tag }}</span>
    {% endfor %}
  </div>
</div>
<hr>
{% endfor %}
