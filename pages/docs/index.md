---
title: CCMS Documentation
layout: page
permalink: /docs/
nav_order: 1
---

{% assign items = site.collections['pages'].docs
  | where_exp: "p", "p.path contains 'pages/docs/' and p.name != 'index.md'"
  | sort: "nav_order" | sort: "title" %}
<ul>
{% for p in items %}
  <li><a href="{{ p.url | relative_url }}">{{ p.title }}</a></li>
{% endfor %}
</ul>
