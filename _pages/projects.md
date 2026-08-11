---
title: "Projects"
layout: single
permalink: /projects/
author_profile: true
---

<p class="page-subheading">Here are a few of my professional and personal projects:</p>

<div class="projects-grid">
  {% for project in site.data.projects %}
  <a class="project-card" href="{{ project.link }}" target="_blank" rel="noopener">
    <span class="project-tag project-tag--{{ project.type }}">{{ project.type }}</span>
    <h3>{{ project.title }}</h3>
    <p>{{ project.blurb }}</p>
  </a>
  {% endfor %}
</div>
