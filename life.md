---
layout: page
title: life
permalink: /life/
description: Short stories, experiences and tips from my life.
---

{% for story in site.life %}

{% if story.redirect %}
<div class="story">
    <div class="thumbnail">
        <a href="{{ story.redirect }}" target="_blank">
        {% if story.img %}
        <img class="thumbnail" src="{{ story.img }}"
        {% else %}
        <div class="thumbnail blankbox"></div>
        {% endif %}    
        <span>
            <h1>{{ story.title }}</h1>
            <br/>
            <p>{{ story.description }}</p>
        </span>
        </a>
    </div>
</div>
{% else %}

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
            <br/>
            <p>{{ story.description }}</p>
            <br/>
            <p>{{ story.date }}</p>
        </span>
        </a>
    </div>
</div>

{% endif %}

{% endfor %}
