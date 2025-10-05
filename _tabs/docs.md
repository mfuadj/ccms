---
layout: page
title: Docs
icon: fas fa-book
order: 2
---

{% assign items = site.documents
  | where: "collection", "pages"
  | where_exp: "p", "p.relative_path contains 'pages/docs/' and p.relative_path != 'pages/docs/index.md'"
  | sort: "nav_order"
  | sort: "title" %}
<ul>
{% for p in items %}
  <li><a href="{{ p.url | relative_url }}">{{ p.title | default: p.data.title | default: p.url }}</a></li>
{% endfor %}
</ul>
