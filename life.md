---
layout: page
title: life
permalink: /life/
description: short stories, experiences and tips from my life
---

{% for story in site.life %}

<div class="story ">
<div class="thumbnail">
    <a href="{{ site.baseurl }}{{ story.url }}">
    {% if story.img %}
        <img class="thumbnail" src="{{ story.img }}"/>
    {% else %}
        <div class="thumbnail blankbox"></div>
    {% endif %}    
    <span>
        <h1>{{ story.title }}</h1>
    </span>
    </a>
</div>
</div>

{% endfor %}
