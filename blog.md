---
layout: page
title: Notes
subtitle: Occasional writing on the craft of doing science — radiative transfer, code, methods, and asides.
permalink: /blog/
---

<ul class="simple-list">
  {% for post in site.posts %}
  <li>
    <a href="{{ post.url | relative_url }}"><strong>{{ post.title }}</strong></a><br>
    <span class="meta">{{ post.date | date: "%-d %B %Y" }}{% if post.summary %} · {{ post.summary }}{% endif %}</span>
  </li>
  {% else %}
  <li><em>No notes yet — first post coming soon.</em></li>
  {% endfor %}
</ul>
