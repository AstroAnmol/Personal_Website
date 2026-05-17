---
layout: page
title: Research
permalink: /research/
description: Research, mission design, and engineering projects.
nav: true
nav_order: 3
display_categories: ["Planetary Regolith Mechanics", "Small Sat Engineering & Operations", "Mission Formulation", "Broader Impacts & Outreach"]
horizontal: false
---

## Research Overview

My research centers on **understanding the behavior of granular materials on low-gravity celestial bodies**, particularly asteroids with remnant magnetic fields. Using **Discrete Element Method (DEM) simulations** and computational frameworks like **LIGGGHTS**, I investigate how magnetic cohesion influences regolith dynamics—a critical factor for safe and efficient exploration of metallic asteroids like NASA's Psyche mission.

This work sits at the intersection of computational modeling, experimental validation, and planetary science, with direct applications to mission planning and spacecraft operations on asteroid surfaces.

---

<div class="category-buttons">
  {% for category in page.display_categories %}
    <a class="btn category-btn" href=".#{{ category }}">{{ category }}</a>
  {% endfor %}
</div>

<!-- pages/projects.md -->
<div class="projects">
{% if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized projects -->
  {% for category in page.display_categories %}
  <a id="{{ category }}" href=".#{{ category }}">
    <h2 class="category">{{ category }}</h2>
  </a>
  {% assign categorized_projects = site.projects | where_exp: "project", "project.category contains category" %}
  <!-- {% assign categorized_projects = site.projects | where: "category", category %} -->
  {% assign sorted_projects = categorized_projects | sort: "importance" %}
  <!-- Generate cards for each project -->
  {% if page.horizontal %}
  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
    {% for project in sorted_projects %}
      {% include projects_horizontal.liquid %}
    {% endfor %}
    </div>
  </div>
  {% else %}
  <div class="row row-cols-1 row-cols-md-3">
    {% for project in sorted_projects %}
      {% include projects.liquid %}
    {% endfor %}
  </div>
  {% endif %}
  {% endfor %}

{% else %}

<!-- Display projects without categories -->

{% assign sorted_projects = site.projects | sort: "importance" %}

  <!-- Generate cards for each project -->

{% if page.horizontal %}

  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
    {% for project in sorted_projects %}
      {% include projects_horizontal.liquid %}
    {% endfor %}
    </div>
  </div>
  {% else %}
  <div class="row row-cols-1 row-cols-md-3">
    {% for project in sorted_projects %}
      {% include projects.liquid %}
    {% endfor %}
  </div>
  {% endif %}
{% endif %}
</div>
