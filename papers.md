---
layout: page
title: Papers
subtitle: Plain-language summaries of selected work. The full publication list lives on Google Scholar.
permalink: /papers/
---

<p style="font-size:0.95rem;">For the complete, up-to-date list see my <a href="https://scholar.google.com/citations?user={{ site.author.scholar }}">Google Scholar</a> profile or <a href="https://orcid.org/{{ site.author.orcid }}">ORCID</a>.</p>

<ul class="paper-cards">
  {% assign all = site.papers | sort: 'date' | reverse %}
  {% for paper in all %}
  <li class="paper-card">
    <h3><a href="{{ paper.url | relative_url }}">{{ paper.title }}</a></h3>
    <p class="meta">{{ paper.authors }} · <em>{{ paper.journal }}</em> ({{ paper.year }})</p>
    <p class="summary">{{ paper.summary }}</p>
  </li>
  {% endfor %}
</ul>
