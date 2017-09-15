---
layout: page
permalink: /portfolio/
title: portfolio
---

<ul class="post-list">
{% for portfolio_event in site.portfolio reversed %}
    <li>
        <h2><a class="portfolio_event-title" href="{{ portfolio_event.url | prepend: site.baseurl }}">{{ portfolio_event.title }}</a></h2>
<!--         <p class="post-meta">{{ portfolio_event.date | date: '%B %-d, %Y — %H:%M' }}</p> -->
      </li>
{% endfor %}
</ul>
