---
layout: page
permalink: /teaching/
title: teaching
description: Materials for courses you taught. Replace this text with your description.
nav: true
nav_order: 5
---

<!-- _pages/teaching.md -->
<div class="teaching">
{% if site.data.teaching %}
  {% for year in site.data.teaching %}
  <h2 class="year">{{ year }}</h2>
  {% assign sorted_courses = site.data.teaching[year] | sort: "importance" %}
  <!-- Generate cards for each course -->
  <div class="grid">
	{% for course in sorted_courses %}
	  {% include course.html %}
	{% endfor %}
  </div>
  {% endfor %}
{% endif %}
</div>

---