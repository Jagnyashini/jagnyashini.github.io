---
title: "News"
layout: page
permalink: /allnews.html
---

# News

<div class="section-card" markdown="0">
<!-- <div class="news-timeline">
{% for article in site.data.news %}
<div class="news-item">
<span class="news-date">{{ article.date }}</span>
<span class="news-headline">{{ article.headline }}</span>
</div>
{% endfor %}
</div> -->
<div class="news-timeline">
      {% for article in site.data.news%}
        <div class="news-item">
          <div class="news-date2">[{{ article.date }}]</div>
          <div class="news-headline2">{{ article.headline }}</div>
        </div>
      {% endfor %}
</div>

</div>
