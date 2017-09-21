---
layout: page
permalink: /portfolio/
title: portfolio
---

<ul class="post-list">
{% for portfolio_event in site.portfolio reversed %}
    <li>
        <h2><a class="portfolio_event-title" href="https://github.com/annelledejager/reisagent">
        reisagent - ionic mobile app</a></h2>

      </li>
{% endfor %}
</ul>
