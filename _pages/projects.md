---
layout: page
title: Projects/Competitions
permalink: /projects/
nav: true
horizontal: false
---

<div class="projects">
  {% assign sorted_projects = site.projects | sort: "importance" %}
  <div class="single-column">
    {% for project in sorted_projects %}
      {% include projects.html %}
    {% endfor %}
  </div>
</div>
