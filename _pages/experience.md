---
title: "Experience"
layout: single
permalink: /experience/
author_profile: true
---

{% assign li_link = site.author.links | where: "label", "LinkedIn" | first %}
<a class="page-cta" href="{{ li_link.url }}" target="_blank" rel="noopener">{% if li_link.icon %}<i class="{{ li_link.icon }}" aria-hidden="true"></i>{% endif %} View full experience on LinkedIn</a>

<div class="experience-timeline">
  {% for company in site.data.experience %}
  <div class="experience-company">
    {% if company.logo %}
    <div class="experience-badge experience-badge--logo"><img src="{{ company.logo | relative_url }}" alt="{{ company.company }} logo"></div>
    {% else %}
    <div class="experience-badge">{{ company.initials }}</div>
    {% endif %}
    <div class="experience-company-body">
      <div class="experience-company-head">
        <h2>{{ company.company }}</h2>
        {% if company.total %}<span class="experience-total">{{ company.total }}</span>{% endif %}
      </div>
      <div class="experience-roles">
        {% for role in company.roles %}
        <div class="experience-role">
          <div class="experience-role-head">
            <h3>{{ role.title }}</h3>
            <span class="experience-dates">{{ role.start }} &ndash; {{ role.end }}</span>
          </div>
          {% if role.location %}<div class="experience-location">{{ role.location }}</div>{% endif %}
        </div>
        {% endfor %}
      </div>
    </div>
  </div>
  {% endfor %}
</div>
