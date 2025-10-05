---
layout: page
title: Documentation
icon: fas fa-book
order: 1
---
{% assign items = site.pages
  | where_exp: "p", "p.path contains 'pages/docs/' and p.name != 'index.md'"
  | sort: "title" %}
<ul>
{% for p in items %}
  <li><a href="{{ p.url | relative_url }}">{{ p.title }}</a></li>
{% endfor %}
</ul>
