---
layout: page
title: "FAQ & Guide"        # <-- & must be quoted in YAML
icon: fas fa-question-circle
order: 3
---

{% assign items = site.pages
  | where_exp: "p", "p.path contains 'pages/faq-guide/' and p.name != 'index.md'"
  | sort: "nav_order" | sort: "title" %}
<ul>
{% for p in items %}
  <li><a href="{{ p.url | relative_url }}">{{ p.title }}</a></li>
{% endfor %}
</ul>
