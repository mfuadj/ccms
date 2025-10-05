---
layout: page
title: "FAQ & Guide"
icon: fas fa-question-circle
order: 3
---

# FAQ & Guide

This section contains frequently asked questions and helpful guides for using the CCMS documentation system.

{% if site.pages.size > 0 %}
  {% assign faq_pages = site.pages | where_exp: "page", "page.path contains 'faq'" | sort: "title" %}
  {% if faq_pages.size > 0 %}
    {% for page in faq_pages %}
      <div class="faq-item">
        <h3><a href="{{ page.url | relative_url }}">{{ page.title }}</a></h3>
        {% if page.description %}
          <p>{{ page.description }}</p>
        {% endif %}
        {% if page.tags %}
          <div class="tags">
            {% for tag in page.tags %}
              <span class="tag">{{ tag }}</span>
            {% endfor %}
          </div>
        {% endif %}
      </div>
      <hr>
    {% endfor %}
  {% else %}
    <p>No FAQ pages available yet. Check back soon for helpful guides and frequently asked questions.</p>
  {% endif %}
{% else %}
  <div class="faq-placeholder">
    <h3>📋 Coming Soon</h3>
    <p>This section will contain:</p>
    <ul>
      <li>Frequently Asked Questions</li>
      <li>How-to guides for using CCMS</li>
      <li>Troubleshooting tips</li>
      <li>Best practices for medical documentation</li>
    </ul>
    <p>Check back soon as we add more helpful content!</p>
  </div>
{% endif %}

## Quick Links

<div class="quick-links">
  <div class="link-card">
    <h4>📚 <a href="{{ '/protocols/' | relative_url }}">Clinical Protocols</a></h4>
    <p>Access standardized clinical protocols and procedures</p>
  </div>
  
  <div class="link-card">
    <h4>📋 <a href="{{ '/guidelines/' | relative_url }}">Practice Guidelines</a></h4>
    <p>Review practice guidelines and standards</p>
  </div>
  
  <div class="link-card">
    <h
