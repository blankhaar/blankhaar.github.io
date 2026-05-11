---
layout: default
description: >-
  Personal site of Boy Lankhaar — Marie Skłodowska-Curie postdoctoral fellow
  at the Institute of Theoretical Astrophysics, University of Oslo, studying
  cosmic magnetic fields with molecular spectral lines.
---

<section class="hero">
  <img class="hero-photo" src="{{ '/assets/img/profile.jpg' | relative_url }}" alt="Boy Lankhaar">
  <div>
    <h1>Boy Lankhaar</h1>
    <p class="role">MSCA Postdoctoral Fellow · Institute of Theoretical Astrophysics, University of Oslo</p>
    <p>I study cosmic magnetic fields by using molecules as messengers — combining theory, quantum chemistry, and radio observations of star-forming regions, evolved stars, and galaxies.</p>
    <div class="hero-links">
      {% include email.html %}
      <a href="https://orcid.org/{{ site.author.orcid }}">ORCID</a>
      <a href="https://scholar.google.com/citations?user={{ site.author.scholar }}">Scholar</a>
      <a href="https://www.linkedin.com/in/{{ site.author.linkedin }}/">LinkedIn</a>
      <a href="https://github.com/{{ site.author.github }}">GitHub</a>
    </div>
  </div>
</section>

<section>
  <div class="section-title"><h2>About</h2></div>
  <p>I am a postdoctoral researcher at the Institute of Theoretical Astrophysics at the University of Oslo, working as an MSCA Fellow within the DSTrain programme. My research interests sit at the intersection of theoretical chemistry, radiative transfer, and radio astronomy: I want to understand the role of magnetic fields in shaping astrophysical systems, from the disks where planets form to the centres of galaxies.</p>
  <p>Before Oslo, I was a postdoctoral researcher at Leiden Observatory and at Chalmers University of Technology (Onsala Space Observatory), supported by a Swedish Research Council grant. My PhD thesis, <a href="https://research.chalmers.se/publication/522154/file/522154_Fulltext.pdf"><em>Tracing Cosmic Magnetic Fields Using Molecules</em></a>, developed quantum-chemical and modelling tools to interpret polarized molecular line emission.</p>
</section>

<section>
  <div class="section-title">
    <h2>Featured papers</h2>
    <a href="{{ '/papers/' | relative_url }}">All papers →</a>
  </div>
  <ul class="paper-cards">
    {% assign featured = site.papers | where: 'featured', true | sort: 'date' | reverse %}
    {% for paper in featured %}
    <li class="paper-card">
      <h3><a href="{{ paper.url | relative_url }}">{{ paper.title }}</a></h3>
      <p class="meta">{{ paper.authors }} · <em>{{ paper.journal }}</em> ({{ paper.year }})</p>
      <p class="summary">{{ paper.summary }}</p>
    </li>
    {% endfor %}
  </ul>
</section>

<section>
  <div class="section-title"><h2>News</h2></div>
  <ul class="news-list">
    {% for item in site.data.news %}
    <li>
      <time datetime="{{ item.date | date: '%Y-%m-%d' }}">{{ item.date | date: "%b %Y" }}</time>
      <span>{{ item.text | markdownify | remove: '<p>' | remove: '</p>' }}</span>
    </li>
    {% endfor %}
  </ul>
</section>
