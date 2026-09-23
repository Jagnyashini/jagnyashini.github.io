---
title: "Home"
layout: homelay
permalink: /
---

<h1 class="home-hero">{{ site.name }}</h1>
<p class="home-hero-sub">{{ site.title }},<br> {{ site.institution }} </p>

<div class="research-intro">
  <p>
   My research focuses on designing <strong>efficient communication protocols</strong> for ultra-low-power IoT–edge networks, with particular emphasis on <strong>distributed intelligence and real-time system coordination</strong>. I develop lightweight distributed machine-learning techniques that enable intelligent computation across resource-constrained edge devices. My work also encompasses the design of robust <strong>dynamic IoT–edge networks</strong> and <strong>synchronisation frameworks for digital-twin environments</strong>. This includes adaptive data-collection strategies, distributed resource management, and intelligent protocol design, with the objective of delivering reliable, scalable, energy-efficient, and high-performance solutions for emerging and next-generation IoT applications.
  </p>
</div>

<!-- <div class="callout callout-success" markdown="0">
<div class="callout-title">{% include icon.html name="award" class="callout-icon" %} Nobel Prize in Physics, 1965</div>
<p>We connect systems so that intelligence can emerge.</p>
</div> -->





<!-- <div class="banner-frame" markdown="0">
<img src="{{ '/images/banner.webp' | relative_url }}" alt="Feynman diagrams" width="1400" height="449" loading="lazy">
<div class="banner-caption">Examples of Feynman diagrams. Feynman R., <em>The theory of positrons. Phys. Rev.</em> (1949)</div>
</div> -->


<!-- {% capture selected %}{% bibliography --query @*[selected=true] %}{% endcapture %}
{% if selected contains "pub-entry" %}
## Recent publications

<div class="section-card selected-pubs" markdown="0">
{{ selected }}
<p style="margin: var(--space-4) 0 0;"><a href="{{ '/publications' | relative_url }}">All publications &rarr;</a></p>
</div>

## News

<div class="section-card selected-pubs" markdown="0">
{{ selected }}
<p style="margin: var(--space-4) 0 0;"><a href="{{ '/publications' | relative_url }}">All publications &rarr;</a></p>
</div>


{% endif %} -->

<div class="research-tagline" markdown="0">
  <div class="research-tagline-label">
    {% include icon.html name="sparkles" class="tagline-icon" %}
    Research Vision 
  </div>

  <div class="research-tagline-text">
  "Connecting systems to create collective intelligence."
    </div>

  <div class="chip-container" markdown="0">
<a href="{{ '/research' | relative_url }}" class="chip">Low Power IoT-Communication</a>
<a href="{{ '/research' | relative_url }}" class="chip">Distributed ML and Edge Intelligence</a>
<a href="{{ '/research' | relative_url }}" class="chip">Distributed UAV Swarm Network</a>
<a href="{{ '/research' | relative_url }}" class="chip">Digital Twins for IoT Network</a>
<a href="{{ '/research' | relative_url }}" class="chip">Smart IoT Applications</a>
</div>

</div>