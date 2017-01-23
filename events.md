---
layout: page
title: events
permalink: /events/
---


{% for event in site.events %}

{% if event.redirect %}
<div class="project">
    <div class="thumbnail">
        <a href="{{ event.redirect }}" target="_blank">
            {% if event.img %}
            <img class="thumbnail resize-img" src="{{ site.baseurl }}/{{ event.img }}"/>
            {% else %}
            <div class="thumbnail blankbox"></div>
            {% endif %}
                <h1>{{ event.title }}</h1>
                <br/>
                {% if event.attendees != 0 %}
                    <p>{{ event.attendees }} attendees</p>         
                {% endif %}
      
            </a>
    </div>
</div>
{% endif %}

{% endfor %}



