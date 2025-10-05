---
layout: page
title: Tags
icon: fas fa-tags
order: 7
---

# Tags

<div class="tag-cloud">
  {% assign tags = site.tags | sort %}
  {% for tag in tags %}
    <a href="{{ '/tags/' | append: tag[0] | relative_url }}" class="tag-link">
      {{ tag[0] | replace: '-', ' ' }}
      <span class="tag-count">({{ tag[1].size }})</span>
    </a>
  {% endfor %}
</div>

## All Tags

{% assign sorted_tags = site.tags | sort %}
{% for tag in sorted_tags %}
<div class="tag-section">
  <h3 id="{{ tag[0] | slugify }}">
    <a href="{{ '/tags/' | append: tag[0] | relative_url }}">{{ tag[0] | replace: '-', ' ' | title }}</a>
    <span class="tag-count">({{ tag[1].size }})</span>
  </h3>
  <ul>
    {% for post in tag[1] %}
      <li>
        <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
        <span class="post-date">{{ post.date | date: "%B %d, %Y" }}</span>
      </li>
    {% endfor %}
  </ul>
</div>
{% endfor %}
