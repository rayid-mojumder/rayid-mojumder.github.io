---
layout: page
title: Projects
permalink: /projects/
description: Selected research projects in photonic interconnects, semiconductor packaging, device fabrication, first-principles materials modeling, and machine learning.
nav: true
nav_order: 2
horizontal: false
---

My current Ph.D. research is listed first, followed by selected projects from my previous work in semiconductor devices, computational materials science, and machine learning.

<!-- pages/projects.md -->
<div class="projects">
  {%- assign sorted_projects = site.projects | sort: "importance" -%}

  {% if page.horizontal -%}
  <div class="container">
    <div class="row row-cols-2">
      {%- for project in sorted_projects -%}
        {% include projects_horizontal.html %}
      {%- endfor %}
    </div>
  </div>
  {%- else -%}
  <div class="grid">
    {%- for project in sorted_projects -%}
      {% include projects.html %}
    {%- endfor %}
  </div>
  {%- endif -%}
</div>
