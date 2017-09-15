---
layout: page
permalink: /life/
title: life
description: Short stories, experiences and tips from my life.
---

<ul class="post-list">
{% for life_event in site.life reversed %}
    <li>
        <h2><a class="life_event-title" href="{{ life_event.url | prepend: site.baseurl }}">{{ life_event.title }}</a></h2>
        <p class="post-meta">{{ life_event.date | date: '%B %-d, %Y — %H:%M' }}</p>
      </li>
{% endfor %}
</ul>
