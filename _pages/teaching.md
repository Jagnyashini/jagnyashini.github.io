---
title: "Teaching"
layout: page
permalink: /teaching/
---


{% if site.data.teaching.size > 0 %}
<div class="section-card-container3">
<div class="section-card">
<h2>Teaching</h2>
<ul class="teaching-list">
{% for course in site.data.teaching %}
<li>
<strong>{{ course.course }}</strong>{% if course.title %}: {{ course.title }}{% endif %}{% if course.term %} ({{ course.term }}){% endif %}{% if course.role %}, {{ course.role }}{% endif %}{% if course.url %} &middot; <a href="{{ course.url }}">Link</a>{% endif %}
{% if course.description %}<br><span class="text-muted">{{ course.description }}</span>{% endif %}
</li>
{% endfor %}
</ul>
</div>
{% else %}
<p class="text-muted">No courses listed yet. Add entries to <code>_data/teaching.yml</code>.</p>
{% endif %}
<div class="section-card">
<h2>Summary</h2>
<p class="teaching-summary">
  Teaching across <strong>2 theory courses</strong> and
  <strong>4 laboratory courses</strong>, reaching over
  <strong>500+ UG and PG students</strong> since
  <strong>July 2025</strong>.
</p>
</div>
</div>
