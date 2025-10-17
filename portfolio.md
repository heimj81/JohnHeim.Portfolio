---
layout: page
title: Portfolio
permalink: /portfolio
---

<p>Below are representative samples. Each entry includes a brief and a download link.</p>

<div class="grid">
  {% for p in site.data.projects %}
  <article class="card">
    <h3>{{ p.title }}</h3>
    <p>{{ p.blurb }}</p>
    <p>
      <a href="{{ p.file | relative_url }}" download>Download</a>
      {% if p.file contains 'http' %}<!-- external links still work -->
      {% endif %}
    </p>
    {% if p.tags %}
      <p class="tags">
        {% for t in p.tags %}<span class="tag">{{ t }}</span>{% endfor %}
      </p>
    {% endif %}
  </article>
  {% endfor %}
</div>
