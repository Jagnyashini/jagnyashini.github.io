---
title: "About"
layout: page
permalink: /about/
---

# About

<div class="section-card-container3">
<div class="section-card">
<div class="pi-card">
<img src="{{ site.photo | prepend: '/images/' | relative_url }}" class="pi-photo" alt="{{ site.name }}" width="160" height="160">
<div>
<h2 class="pi-name">{{ site.name }}</h2>
<p style="font-style: italic; color: var(--text-secondary);">
  {{ site.title }}<br>
  {{ site.institution }}
</p>
</div>
</div>
</div>
<div class="section-card facts-card">
<h2>Beyond Research</h2>
<div class="facts-slideshow">
<div class="fact-slide active">
<span class="fact-icon">🌍</span>
<p>Exploring new places keeps her curiosity alive.</p>
</div>
<div class="fact-slide">
<span class="fact-icon">🎨</span>
<p>Painting gives colour to her quietest thoughts.</p>
</div>
<div class="fact-slide">
<span class="fact-icon">🌿</span>
<p>She finds happiness in peaceful places and simple moments.</p>
</div>
<div class="fact-slide">
<span class="fact-icon">✨</span>
<p>Her most dependable companion is her own determination.</p>
</div>
<div class="fact-slide">
<span class="fact-icon">🚀</span>
<p>From telecom systems to edge intelligence—a journey of reinvention.</p>
</div>
<div class="fact-slide">
<span class="fact-icon">🌿</span>
<p>She finds happiness in peaceful places and simple moments.</p>
</div>
</div>
<div class="fact-dots" aria-label="Select a fact">
<button class="fact-dot active" aria-label="Fact 1"></button>
<button class="fact-dot" aria-label="Fact 2"></button>
<button class="fact-dot" aria-label="Fact 3"></button>
<button class="fact-dot" aria-label="Fact 4"></button>
<button class="fact-dot" aria-label="Fact 5"></button>
<button class="fact-dot" aria-label="Fact 6"></button>
</div>
</div>
</div>

<!-- <div class="section-card">
<div class="pi-card">
<img src="{{ site.photo | prepend: '/images/' | relative_url }}" class="pi-photo" alt="{{ site.name }}" width="160" height="160">
<div>
<h2 class="pi-name">{{ site.name }}</h2>
<p style="font-style: italic; color: var(--text-secondary);">
  {{ site.title }}<br>
  {{ site.institution }}
</p><!-- <div class="pi-links">
{% if site.email %}<a href="mailto:{{ site.email }}" class="icon-link" title="Email" aria-label="Email">{% include icon.html name="envelope" %}</a>{% endif %}
{% if site.links.cv and site.links.cv != "" %}<a href="{{ site.links.cv | prepend: '/' | relative_url }}" class="icon-link" title="CV" aria-label="CV">{% include icon.html name="cv" %}</a>{% endif %}
{% if site.links.google_scholar and site.links.google_scholar != "" %}<a href="{{ site.links.google_scholar }}" class="icon-link" title="Google Scholar" aria-label="Google Scholar">{% include icon.html name="google-scholar" %}</a>{% endif %}
{% if site.links.github and site.links.github != "" %}<a href="{{ site.links.github }}" class="icon-link" title="GitHub" aria-label="GitHub">{% include icon.html name="github" %}</a>{% endif %}
{% if site.links.researchgate and site.links.researchgate != "" %}<a href="{{ site.links.researchgate }}" class="icon-link" title="ResearchGate" aria-label="ResearchGate">{% include icon.html name="researchgate" %}</a>{% endif %}
</div> -->
<!--</div>
</div>
</div> -->
{% if site.data.pi[0].education %}
<div class="section-card">
<h3>A Journey of Learning & Discovery</h3>
<div class="education-timeline">
{% for education in site.data.pi[0].education %}
<div class="education-item">
<div class="education-node">
<div class="education-node-inner"></div>
</div>
<div class="education-card">
<div class="education-icon">
{% case forloop.index %}
{% when 1 %}
<svg class="icon" aria-hidden="true">
<use href="#icon-gradhat"></use>
</svg>
{% when 2 %}
<svg class="icon" aria-hidden="true">
<use href="#icon-briefcase"></use>
</svg>
{% when 3 %}
<svg class="icon" aria-hidden="true">
<use href="#icon-gradhat"></use>
</svg>
{% when 4 %}
<svg class="icon" aria-hidden="true">
<use href="#icon-gradhat"></use>
</svg>
{% when 5 %}
<svg class="icon" aria-hidden="true">
<use href="#icon-institute1"></use>
</svg>
{% when 6 %}
<svg class="icon" aria-hidden="true">
<use href="#icon-institute1"></use>
</svg>
{% endcase %}
</div>
<div class="education-year">
  {{ education | split: ")" | first | remove_first: "(" }}
</div>
<div class="education-text">
  {% assign education_text = education | split: ")" | last | strip %}
  {% assign education_parts = education_text | split: "," %}
  {% for part in education_parts %}
  {{ part | strip | replace: "-", "&#8211;" }}{% unless forloop.last %}<br>{% endunless %}
  {% endfor %}
</div>
</div>
</div>
{% endfor %}
</div>
</div>
{% endif %}
{% if site.data.grants %}
<div class="section-card">
<h3>Grants</h3>
<ul>
{% for grant in site.data.grants %}
<li>{{ grant.name }}</li>
{% endfor %}
</ul>
</div>
{% endif %}

<div class="section-card-container4">
{% if site.data.awards %}
<div class="section-card">
<h3>Honours & Distinctions</h3>
<ul>
{% for award in site.data.awards %}
<li>{{ award.name | replace: "-","&#8211;" }}</li>
{% endfor %}
</ul>
</div>
{% endif %}
<div class="section-card">
<h3>Professional Services</h3>
<ul>
<li>Reviewer, IEEE Transactions on Network and Service Management</li>
<li>Reviewer, IEEE Transactions on Sensor Networks</li>
<li>Reviewer, IEEE Transactions on Vehicular Technology</li>
<li>Reviewer, IEEE ANTS 2026</li>
</ul>
</div>
</div>

{% if site.data.funders %}
<div class="section-card">
<h4>Sponsors</h4>
<div class="sponsor-logos" style="display: flex; flex-wrap: wrap; align-items: center; justify-content: center; gap: var(--space-6);">
{% for funder in site.data.funders %}
<a href="{{ funder.url }}" target="_blank"><img src="{{ funder.image | prepend: '/images/' | relative_url }}" alt="Funder logo" style="max-height: 80px; max-width: 200px; border-radius: 0;" loading="lazy"></a>
{% endfor %}
</div>
</div>
{% endif %}


<script>
  document.addEventListener("DOMContentLoaded", function () {
    const slides = document.querySelectorAll(".fact-slide");
    const dots = document.querySelectorAll(".fact-dot");

    if (!slides.length) return;

    let currentSlide = 0;
    let slideshowTimer;

    function showSlide(index) {
      slides.forEach((slide, slideIndex) => {
        slide.classList.toggle("active", slideIndex === index);
      });

      dots.forEach((dot, dotIndex) => {
        dot.classList.toggle("active", dotIndex === index);
      });

      currentSlide = index;
    }

    function startSlideshow() {
      slideshowTimer = setInterval(() => {
        const nextSlide = (currentSlide + 1) % slides.length;
        showSlide(nextSlide);
      }, 4000);
    }

    dots.forEach((dot, index) => {
      dot.addEventListener("click", () => {
        clearInterval(slideshowTimer);
        showSlide(index);
        startSlideshow();
      });
    });

    showSlide(0);
    startSlideshow();
  });
</script>