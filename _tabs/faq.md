---
layout: page
title: "FAQ & Guide"
icon: fas fa-question-circle
order: 3
---

{% assign items = site.documents
  | where: "collection", "pages"
  | where_exp: "p", "p.relative_path contains 'pages/faq-guide/' and p.relative_path != 'pages/faq-guide/index.md'"
  | sort: "nav_order"
  | sort: "title" %}
<ul>
{% for p in items %}
  <li><a href="{{ p.url | relative_url }}">{{ p.title | default: p.data.title | default: p.url }}</a></li>
{% endfor %}
</ul>
