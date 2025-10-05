---
layout: page
title: Docs
icon: fas fa-book
order: 2
---

# CCMS Documentation

Welcome to the CCMS (Clinical Content Management System) documentation. This comprehensive medical documentation system is designed for healthcare professionals to access standardized protocols, guidelines, and procedures.

## Documentation Collections

<div class="docs-grid">
  <div class="docs-card">
    <h3>📋 <a href="{{ '/protocols/' | relative_url }}">Clinical Protocols</a></h3>
    <p>Evidence-based clinical protocols for common conditions and treatments</p>
    <div class="collection-stats">
      <span class="stat">{{ site.protocols.size }} protocols available</span>
    </div>
  </div>

  <div class="docs-card">
    <h3>📄 <a href="{{ '/guidelines/' | relative_url }}">Practice Guidelines</a></h3>
    <p>Standardized practice guidelines and quality improvement standards</p>
    <div class="collection-stats">
      <span class="stat">{{ site.guidelines.size }} guidelines available</span>
    </div>
  </div>

  <div class="docs-card">
    <h3>⚕️ <a href="{{ '/procedures/' | relative_url }}">Procedures</a></h3>
    <p>Step-by-step medical procedures and clinical techniques</p>
    <div class="collection-stats">
      <span class="stat">{{ site.procedures.size }} procedures available</span>
    </div>
  </div>

  <div class="docs-card">
    <h3>💊 <a href="{{ '/medications/' | relative_url }}">Medications</a></h3>
    <p>Drug information, dosing guidelines, and prescribing protocols</p>
    <div class="collection-stats">
      <span class="stat">{{ site.medications.size }} medications available</span>
    </div>
  </div>

  <div class="docs-card">
    <h3>📚 <a href="{{ '/references/' | relative_url }}">References</a></h3>
    <p>Clinical references, guidelines, and evidence-based resources</p>
    <div class="collection-stats">
      <span class="stat">{{ site.references.size }} references available</span>
    </div>
  </div>
</div>

## Recent Updates

<div class="recent-updates">
  {% assign all_docs = site.protocols | concat: site.guidelines | concat: site.procedures | concat: site.medications | concat: site.references %}
  {% assign recent_docs = all_docs | sort: 'last_updated' | reverse | limit: 5 %}
  
  {% for doc in recent_docs %}
    <div class="update-item">
      <h4><a href="{{ doc.url | relative_url }}">{{ doc.title }}</a></h4>
      <p class="update-meta">
        <span class="collection-type">{{ doc.collection | capitalize }}</span> • 
        <span class="update-date">Updated {{ doc.last_updated | date: "%B %d, %Y" }}</span>
      </p>
      {% if doc.description %}
        <p class="update-description">{{ doc.description }}</p>
      {% endif %}
    </div>
  {% endfor %}
</div>

## How to Use This Documentation

### Navigation
- Use the **sidebar menu** to browse different documentation types
- Use the **search function** to find specific topics
- Browse by **tags** to find related content

### Content Organization
- **Protocols**: For clinical decision-making and patient care
- **Guidelines**: For practice standards and quality measures
- **Procedures**: For step-by-step clinical techniques
- **Medications**: For prescribing and drug information
- **References**: For supporting evidence and external resources

### Getting Started
1. Browse the **Clinical Protocols** for common conditions
2. Review **Practice Guidelines** for quality standards
3. Check **Procedures** for clinical techniques
4. Reference **Medications** for prescribing information

---

*Last updated: {{ site.time | date: "%B %d, %Y" }}*
