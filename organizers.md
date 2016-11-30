---
layout: page
title: organizers 
permalink: /organizers/
---

{% for organizer in site.organizers %}

{% if organizer.redirect %}
<div class="project">
    <div class="thumbnail">
        <a href="{{ organizer.redirect }}" target="_blank">
        {% if organizer.img %}
        <img class="thumbnail resize-img" src="{{ site.baseurl }}/{{ organizer.img }}"/>
        {% else %}
        <div class="thumbnail blankbox"></div>
        {% endif %}
        <span>
            <h1>{{ organizer.title }}</h1>
            <br/>
            <p>{{ organizer.description }}</p>
        </span>
        </a>
    </div>
</div>
{% else %}
<div class="project ">
    <div class="thumbnail">
        <a href="{{ site.baseurl }}{{ organizer.url }}">
        {% if organizer.img %}
        <img class="thumbnail resize-img" src="{{ site.baseurl }}{{ organizer.img }}"/>
        {% else %}
        <div class="thumbnail blankbox"></div>
        {% endif %}
        <span>
            <h1>{{ organizer.title }}</h1>
            <br/>
            <p>{{ organizer.description }}</p>
        </span>
        </a>
    </div>
</div>

{% endif %}

{% endfor %}
