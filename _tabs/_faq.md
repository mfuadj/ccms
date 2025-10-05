---
layout: page
title: FAQ & Guide
icon: fas fa-question-circle
order: 2
---
{% assign items = site.pages
  | where_exp: "p", "p.path contains 'pages/faq-guide/' and p.name != 'index.md'"
  | sort: "title" %}
<ul>
{% for p in items %}
  <li><a href="{{ p.url | relative_url }}">{{ p.title }}</a></li>
{% endfor %}
</ul>
