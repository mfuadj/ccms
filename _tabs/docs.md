---
layout: page
title: Docs
icon: fas fa-book
order: 1
---

# Docs

{% assign docs = site.pages | where_exp: "p", "p.path contains 'pages/'" %}
<ul>
{% for p in docs %}
  <li><a href="{{ p.url | relative_url }}">{{ p.title }}</a></li>
{% endfor %}
</ul>
